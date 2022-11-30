---
title: xUnit, complex types as parameters? Memberdata!
author: andreas_gustafsson
date: 2022-11-21 03:51:00 +0200
categories: [Development, Coding, Testing]
tags: [xunit, .net, unittest, testing, ]
---

### TLDR; 

Go to the code example: [`code`](#example-code).
 
<br>

This is a feature in [Xunit](https://xunit.net/){:target="blank"} that I think people arent using enough. There are many times that you can get away with having a few parameters into a test with the attribute `InlineData`, and it will look something like this: 

```csharp

[Theory]
[InlineData("")]
[InlineData("  ")]
[InlineData(null)]
public void Given_Something_Should_Throw_Exception(string name)
{
        var act = () =>
        {
            //Do seomthing with name
        };

        act.Should().Throw<ArgumentException>("*name*");
}

```

A parameterized test is common as above, but when it comes to the fact that you would like to have a collection of some sort as a parameter, I dont see people use `MemberData` attribute together with `TheoryData`.

How it works is quite simple; foreach item in your `TheoryData` is one test case. For example, let's say you want to test a method that takes in a string as a parameter to not be null, empty or only spaces.
You could create a source of data with 3 items, and reference that as your `MemberData` for your `Theory` like below:

## Example code 


```csharp

public class TestData
{
    public static TheoryData<string> StringNullEmptyAndWhiteSpace =>
            new TheoryData<string>()
            {
                { "" },
                { null },
                { "  " },
            };
}

public class FubarTests
{
    [Theory]
    [MemberData(nameof(TestData.StringNullEmptyAndWhiteSpace), MemberType = typeof(TestData))]
    public void Given_Something_Should_Throw_Exception(string name)
    {
        var act = () =>
        {
            //Do seomthing with name
        };

        act.Should().Throw<ArgumentException>("*name*");
    }
}

```

_The assertion above is written with [FluentAssertions](https://fluentassertions.com/introduction){:target="_blank"}, one of my favourite libraries for assertions!_

Small note here for the attribute, the propert `MemberType` is only required if you have "TestData" outside the class you want to use it in. If you would create a property in the same class as your test, you dont need to set this property. 

## More Complex parameters? 
As `TheoryData` is generic you can basically add whatever model you want to have, so you could also have a parameter that is a list, for ex:

```csharp
public static TheoryData<IEnumerable<string>> ListAsParameter =>
            new TheoryData<IEnumerable<string>>()
            {
                new [] { "" , null, "  " ,}
            };
```

This way you can with ease have more complex parameters to your `Theory` lists for example, that `InlineData` dosent support!

Frankly I dont know, why I dont see this small feature used more often, also, I see people use this with `objects` instead of actually classes.
