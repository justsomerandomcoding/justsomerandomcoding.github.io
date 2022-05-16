---
title: Installing Jekyll on windows
author: andreas_gustafsson
date: 2022-05-08 20:37:00 +0100
categories: [Jekyll, Tutorial]
tags: [getting started, jekyll]
---

## How can not the first blog post on a tech site be, how I did it

This blog is beeing hosted on [Github pages](https://pages.github.com/){:target="_blank"} so with that said, it's quite obvious that I do have a github account and git installed. 
Github pages support [Jekyll](https://jekyllrb.com/){:target="_blank"} that transforms your [Markdown](https://en.wikipedia.org/wiki/Markdown){:target="_blank"} files to a static website (in short). There is no need for databases, updates, or stuff like that, you have your files in your repository, `Jekyll` transforms your file to a static website, this means a blogpost is simply a `markdown` file in the end. So here is how I did it. 

## Installation

### Requirements

You need `Git`, `Chocolatey`, `Ruby`, `GCC`, `G++` and `Make`
From [Jekylls](https://jekyllrb.com/docs/installation/){:target="_blank"} website I downloaded and installed `Ruby` and `RubyGems`
After that with [Chocolatey](https://chocolatey.org/){:target="_blank"} I installed the rest what I needed
- choco install make
- choco install mingw

> You can actually install ruby togehter with their devkit through chocolatey also, just run:
> `choco install ruby` and
> `choco install ruby.devkit`
{: .prompt-tip }

### Jekyll
When you have ruby installed you can install Jekyll
```console
gem install jekyll bundler
```

#### Verify you installation
Check your version on everything that you have installed to double check that all is good
 - ruby -v
 - gem -v
 - gcc --version
 - g++ --version
 - make --version
 - jekyll -v

### Creating my site

I didnt wanted to create my own theme, I was looking for something simple and did found `Chirpy` which is the theme i went with. Chirpy is a minimal, responsive and powerful Jekyll theme all open source.
So I created a new repository from their started repository [Jekyll started](https://github.com/cotes2020/chirpy-starter){:target="_blank"}, to have a personal website hosted on gitpages your repository have to correspond with your username, so logically I named my new repository `justsomerandomcode.github.io`. 

With the code locally it's just to install and bundle + get a local web server up and running with your site. 

```console
bundle install
```
Run a local server
```console
bundle exec jekyll serve --livereload
```
`Chirpy` has extended documentation on what you need to change, i did a few changes for authors, removed some posts and edit the _config.yml file and I was ready to go!

## Deploying the code to Github

The starter repo that i'm using, seems to have everything I need, so to deploy the code and run the website, it's just to follow a few more changes, go to my `.github/workflows/pages-deploy.yml.hook` and change the branch to trigger on `main` not `master`.

Go to my Github repo -> settings -> pages, select my source a the new branch that is created automatically `gh-pages` and folder to ´/root´, done and done, push my code and the site is up and running. 


## What's next? 

This blog is runnig on `markdown` files and `Chirpy` theme as mentioned above, for the time beeing (when im writing this) I dont have any data on traffic for this site. So the next step will be to follow the tutorial to setup Google Analyctics and start to monitor how many visitors this blog actually gets. 

I'v also read that I can add comments on this site by using Githubs issues themselfs via a 3rd party plugin. [`Utterences`](https://utteranc.es/){:target="_blank"} seems to be a good option, open source, free and under the MIT License.