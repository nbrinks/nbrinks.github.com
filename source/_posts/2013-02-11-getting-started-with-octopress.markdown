---
layout: post
title: "Getting started with Octopress"
date: 2013-02-11 21:29
comments: true
categories:
---

I just recently started using Octopress to manage this blog, so I think it makes sense that my first post is about Octopress itself.

Several years ago I deployed a Drupal website but have since decided Drupal provided much more than I was looking for. Since Octopress doesn't require a database the added benefit of migrating to Octopress means I can drop my paid hosting plan and instead deploy this website to [GitHub Pages](http://pages.github.com/).

Now, to the point.

For the most part I was able to follow the setup instructions available at [Octopress.org](http://octopress.org/docs/setup/). Octopress.org also provides instructions and tools to [deploy to GitHub Pages](http://octopress.org/docs/deploying/github/).

One thing that wasn't completely clear at first was how to get changes made to the configuration to take effect on the public facing website. Basically, the commands I was missing...
```
rake generate
rake deploy
```
Essentially, <code>rake generate</code> builds the public files and <code>rake deploy</code> pushes the changes to the master branch, which is then served up to vistors navigating your website. The repository where this website is hosted can be found on [my GitHub account](https://github.com/nbrinks/nbrinks.github.com).

Another incredibly useful command,
```
rake preview
```
Running this task starts a web server on your localhost. The web server is accessible by navigating to <code>http://localhost:4000</code>. A handy feature of the preview task is the ability to automatically regenerate the public files as you make changes to the code base. I have been using this feature exclusively while editing <code>.../octopress/sass/custom/_colors.scss</code> and creating this blog post.
