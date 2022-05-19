---
title: Adding Utterances as comment feature for jekyll
author: andreas_gustafsson
date: 2022-05-19 07:01:00 +0200
categories: [Jekyll, Tutorial]
tags: [jekyll, utterances]
img_path: /assets/img/2022-05-19/
---

## Adding [Utterances](https://utteranc.es/) as comment feature for jekyll

### tldr; 
 >  1. Install Utterances from Github Marketplace
 >  2. [Configure](https://utteranc.es/) your script tag 
 >  3. Paste your script tag in `_layouts/post.html`
 {: .prompt-tip } 

This blog is hosted on github pages powered by Jekyll, my theme that I have choosed is `Chirpy`. 

But Jekyll dosent come with comment features for your pages or blog posts, that's why we are gonna test Utterance. Utterances is an lightweight open source no ad plugin for Github that uses the issues feature for blog comments, pages and more. 

In short Utterances will match the current page based on `url`, `title` or `pathname`, and will if non issue exist, create on for you. 

### Step 1, install utterances
So head over to `Github` and install the app from marketplace, should look something like this:
![Utterances](utterances_app.png){: .normal }

__verry funny "see plan" button that leads you to__
![Utterances pricing](utterances_app_pricing.png){: .normal }

Click install for free and continue with the setup, the first option is to choose if you want to install the app for __All__ or Only one selected repository, for this tutorial; Im choosing one repository. 
![Utterances install step 1](utterances_install_step_1.png){: .normal }

Enforce the installment by entering your password once again. 
![Utterances install step 2](utterances_install_step_2.png){: .normal }

### Step 2, Configure your script tag
After this step you will get to redirected to utterances website. And more specific the install section, the steps here are detailed and explained, so the `configuration` steps, 

    1. Enter your github repo name
    2. Select how you want utterances to identify your issue for your page/post
    3. Add an label that will be automatically added to your issue when utterances is creating a new issue
    4. Select a theme. 
   
These steps will than give you a small script section that you want to hold on to: 

```html
<script src="https://utteranc.es/client.js"
        repo="justsomerandomcoding/justsomerandomcoding.github.io"
        issue-term="url"
        theme="github-dark"
        crossorigin="anonymous"
        async>
</script>
```

### Step 3, Add your script tag to your pages
You should with this script tag add it to the pages where you want to have comments, now I only want to have comments on my blog posts, so I located my `_layout/post.html` template that is the template for blog posts and pastet the script in the bottom of the file. Now I have comments on the blog
![Utterances comment seciont](/utterances_comment.png){: .normal}

