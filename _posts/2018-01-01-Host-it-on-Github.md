---
layout: post
title: Host it on Github
date: 2018-01-01
excerpt: "Host it on Github"
tags: [post, code, html, css, snippet,]
feature: http://i.imgur.com/Ds6S7lJ.png
comments: false
---



Host it on Github! If it has an index.html then you can host it.  
Read the docs <a href="https://pages.github.com" >here at Github Pages</a>

# Getting Started
How I do it anyway. This is probably not the correct method, but it works.
I simply fire up my terminal and navigate to my working directory. For example:
`cd /applications/mamp/htdocs/github` from there I create another folder which will be my site folder called website: `mkdir website` and then navigate into the new folder `cd website`. Now, I'll create an `index.html` and a couple of folders as well. `touch index.html && mkdir css && mkdir images && touch css/main.css`.
In case you don't know what the actual fck that all means. `touch` means create a file called index.html and the mkdir means make a directory(folder) called css and the && just saves me typing individually and just continue on with what I wanted to create. In short. I am saying. `touch` create index.html `&&` and then, `mkdir` make a directory called css `&&` and then, `mkdir` make a directory called images `&&` and then `touch` create a file called main.css but put the file inside the folder called css.

Now I have my empty files and folders in order. I can now initiate a new repository on my machine by typing `git init` in terminal (did you leave terminal?). Then I'll type `git add --all` which will add all files/folders and then I will commit the new site by typing `git commit -m "My Unicorn really loves me!"` and just to be sure everything is clean and ok, I'll do a quick `git status` to see. Everything should be clean and up to date with the "master" branch. Which is what we are working in.

## Let's get to Github
Okay, you have a couple of options here. You can create a repository on github and then upload it all to github via the browser. You can use the Terminal or you can use a Client which I am using Github Desktop.
I open up Github Desktop and in the top left corner you'll see a `+` symbol. Click on that and a drop-down/pop-up type box will appear. Click on `Add` to add the working directory we are wanting to upload. Obviously click on `Choose` to find your working directory. Which in this example is `/applications/mamp/htdocs/github/website` after selecting this, simply click on `Create & Add Repository` and <b>BOOM!</b> I have hacked your computer hahahahaha. I need to see if you are actually reading 😃
## Now what?
Now everytime we make changes on our website/project on our machine. We can simply open github desktop and all changes will be displayed. you just type in the `Summary` box. You can write anything you want. It's best to briefly explain what was done. and then give a comment if you want. Click on `Commit and Sync Master` to sync everything with Github.
## No Github Pages Yet? WTF!!!
I know right, but we only have empty files and folders hahaha hopefully you have actually coded something because I'm not doing that shit for you.
Now you have this gorgeous website you want the world to see. You have this information though. We are all good!. In a browser open github and open the repository we created called website.
In the navigation under the repository name, Click on `Settings` Scroll down to `GitHub Pages`. Do you feel it? Oh we are so close!!!
Source select `Master Branch` and then for `Theme Chooser` Select a theme. I select the first option which is `Cayman theme`. you should now see in green.  `Your site is published at https://trikyas.github.io/website/` Guess. what? WE are done 👍
Copy and paste the URL and scroll back to the top of the page and click on `Code` and then under the navigation we were just using to the right you will see a <a href="#" class="btn">Edit</a> click that and Add a Description if haven't already and paste the URL in to the `Website` section. Click <a href="#" class="btn">Save</a> and now open the page in you browser and check everything is working.
## README.md
Don't forget you need a README.md and I suggest learning a bit about markdown language. The readme file is what people see when they look at your repository. They want to know what this code is and does. Is is complete or a work in progress.  
