---
title: My favourite key shortcuts I cant live withouth 
author: andreas_gustafsson
date: 2022-11-08 03:01:00 +0200
categories: [Development]
tags: [ide, rider, visualstudio, productivity, developerlife]
---

## My favourite key shortcuts I cant live withouth

### tldr; 

>1. Resharper.Resharper_LocateInSolutionOrAssemblyExplorer
>2. Resharper.Resharper_GoToType
>3. Resharper.Resharper_GoToFile
>4. Resharper.Resharper_Generate (Context: File)
>5. Resharper.Resharper_Generate (Context: Solution Explorer)
>6. Window.NextDocumentWindowNav
>7. File.Close/Close Active Tab
>8. Edit.ToggleOutliningExpension/ToggleFolding
>9. Edit.SurroundWith
>10. Edit.FormatDocument
>11. Edit.CommentSelection
>12. Edit.UncommentSelection
>13. Debug.ToggleBreakBreakPoint

When I quit my previous job, I got a reminder just before I ended, how important it is to configure my IDE to my behaviour. As my last weeks flew by I got to learn that I wont work on the same OS anymore and therefore also switch IDE, this did made me feel exited, happy and frankly a bit scared also, as I have for the last 10 years tried to configure my IDE for my needs and how I behave, I have replicated the same key shortcuts from google chrome to match how I navigate inside Visual Studio, when I close a tab in google chrome I use `CTRL + W` so by nature I want the same in Visual Studio code. 

With the knowledge that I now need to move from Visual Studio (with Resharper) to Project Rider, I set out 2 weeks where I listed the most important key shortcuts that im using and remap them to my new IDE. 
When I say most important, the one I use on a daily basis. 

## The list I came up with was as follows: (in no specific order)

1. Resharper.Resharper_LocateInSolutionOrAssemblyExplorer - Locating curent file in solution tree
2. Resharper.Resharper_GoToType - Search by type
3. Resharper.Resharper_GoToFile - Search by filename
4. Resharper.Resharper_Generate (Context: File) - Generate code snippets, ctor etc inside file
5. Resharper.Resharper_Generate (Context: Solution Explorer/File tree) - Opens context menu to add new item, file, folder etc. 
6. Window.NextDocumentWindowNav - Navigate to next tab open in the IDE
7. File.Close - Close current active tab
8. Edit.ToggleOutliningExpension - Toggle folding scope
9. Edit.SurroundWith - Open up menu with selelection to surround the selected code with ex, try catch, while loop, if etc.
10. Edit.FormatDocument - Format document with intendation
11. Edit.CommentSelection - Comment selected section
12. Edit.UncommentSelection - Comment selected section
13. Debug.ToggleBreakBreakPoint - Toggle breakpoint on current line

## Key mapings
This is how I do the mapping:

| Command name | VS | Rider |
| ------ | ----- | ----- | 
| Resharper.Resharper_LocateInSolutionOrAssemblyExplorer | (Shift+Alt+L) | (Option+Shift+L) | 
| Resharper.Resharper_GoToType | (Ctrl+T) | (Ctrl+Shift+N) |
| Resharper.Resharper_GoToFile  | (Ctrl+Shift+T) | (Ctrl+Shift+N) |
| Resharper.Resharper_Generate (Context: File) | (Alt+Ins) | (Command+F10) |
| Resharper.Resharper_Generate (Context: Solution Explorer) | (Alt+Ins) | (Shift+F10) |
| Window.NextDocumentWindowNav | (Ctrl+Tab) | (Ctrl+Tab) |
| File.Close/Close Active Tab | (Ctrl+W) | (Command+W) |
| Edit.ToggleOutliningExpension/ToggleFolding | (Alt+1) | (Command+1) |
| Edit.SurroundWith | (Ctrl+K+S) | (Command+K+S) |
| Edit.FormatDocument | (Ctrl+K+D) | (Ctrl+Option+L) |
| Edit.CommentSelection | (Ctrl+K+C) | (Command+K+C) |
| Edit.UncommentSelection | (Ctrl+K+U) | (Command+K+C) |
| Debug.ToggleBreakBreakPoint | F9 | F9 |

## Disclosure, or something
I also came to the insight that this is something that junior developers dosent get thought, as I havent had the pleasure to work as a mentor for someone 100% almost everyone I came by the last year who's fresh out of school havent learned how to configure their IDE, to work with the keyboard for debugging, just for the reasons to become more producitve in their day to day work. 

What happened? 10 years ago I'm sure I have read blog posts about productivity and how important it is to get to learn your IDE, is that not a thing today? People just want to press `run` and click with the mouse forever?

## Postscript note
The list is obvious missing a few shortcuts as when im writing this comes to think off the following on top of my head (I dont have the actual name for the IDE's at this moment of time) I dont know how I missed these, I guess they are to essential that they are always there. 

(Windows Visual Studio)
- Jump next line (when debugging) - F11
- Jump into (when debugging) - F10 
- Run - F5
- Remove all breakpoint - CTRL + SHIFT + F9
- Stop debugging - Shift + F5
- Run test - Ctrl + R + T
- View Action list - Alt + Enter

Honeslty not sure how I missed those, and also when it comes to productivity shortcuts, I think there has to be a second blog post about just Visual Studio code, as that is an amazing tool when you get to learn it properly!