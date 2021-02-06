---
layout: post
title: "How I build this Web Page with Github Pages 2"
date: 2021-02-06
---

I spent a day to dive into the topic of github page. And this leads me to several other topics including git and Jekyll. 

After setup a personal web page using github pages from github website. 

First, I need to find out the way to edit and server these web page locally. 

Secondly, It is time to extend to other projects with the same base url, like https://(github_userID).github.io/project_1. 

And the first thing to do is how to migrate the repo from github website to my local computer. Based on the tutorial from JONATHAN MCGLONE, I only created a folder without jeklly build up fills. In my case I use MAC to build all these with ruby installed. 

In the Terminal:

```
sudo gem i bundler jekyll 
## sudo means force to install, which is needed when alert jumps out. Then, install bundler and jekyll. This process will take a while to complete. 

## to test if installation is successful run below codes in a new folder which you could delete later. 
jekyll new my-awesome-site
## This process will create lots of fills I don't understand. That is find.

```

Now to download the repo from github just type following code

```
git clone https://github.com/(ID)/(IDname).github.io.git
```
Do some edit and go with the 

```
git add .
git commit -m "comment"
git push -u origin master
## I still on the way to figure out what the "-u" means
```

During the time I tried to understand each piece of Jeklly fill means by adding files in main folder:

- _config.yml
- index.html



- Gemfile: add code 
```
source "https://rubygems.org"
```
Then open the terminal and run code :
```
bundle exec jekyll serve 
## this leads to an alert that I need to justify gem dependency in gemifle. 
```
So go back to Gemfile and add following code and run code again. 
```
gem 'github-pages'
```

Then git push. 