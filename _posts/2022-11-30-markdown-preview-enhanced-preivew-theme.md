---
title: How to set preview window theme for markdown preview?
author: andreas_gustafsson
date: 2022-11-30 06:15:00 +0200
categories: [Development, Coding, VisualStudioCode]
tags: [visualstudiocode, markdown, customize, developerlife]
img_path: /assets/img/2022-11-30/
---

I'm writing markdown basically everyday. I love [Visual Studio Code](https://code.visualstudio.com/download) as an editor and i'm using [Markdown Preview Enhanced](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced) as my preview tool.
Now out of the box the preview window is white, and I prefer a darker theme and have set my VS Code to have a darker theme, more precisely `One dark pro`. 

What is most annoying is the white background on the Preveiw window, it hurts my eyes having a darker theme and a white bright preview window.
So lets fix this! Open your `settings.json` file, that holds your settings for Visual Studio, if you dont know how to do that; search for  `Open User Settings (JSON)` in your command pallet. To open your command pallet on MAC press __Command+Shift+P__ and Windows __Ctrl+Shift+P__

You will open a JSON file and here you can add a theme for Markdown Preview Enhanced Preview theme;

> "markdown-preview-enhanced.previewTheme": "one-dark.css",

You can set the theme's css to any of the installed theme's you have. For me some of the options are as image below
![Preview theme css options](preview-theme-css.png){: .normal }

And by setting this I now have a dark preview window for my markdown! 
Got damn that is neat! 