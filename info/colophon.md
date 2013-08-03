---
layout: other
title: Colophon
---

Over the years, I have experimented with many different back ends for course websites. I very early abandoned the university Blackboard service for various DIY options. For a while I ran my course sites with a wordpress installation, but gave up on it after being hacked. (The exploit was through a third-party discussion forum plugin.) 

After that, I switched to various forms of database-less sites, including sites made with a static generator and a web app coded in python's flask framework. In the end, I've come over to the opinion that course sites are content sites, not applications. No need to overbuild them.  

For this class, I wanted the simplicity and hackerness of a static site generator, and the interactivity of a group blog. Enter the combination of [github pages](http://pages.github.com/) and [prose.io](http://prose.io). Github pages allows for the automatic publication of a site repo hosted for free at github, and using the distributed version control software git. Conceivably, everyone could participate in writing posts and building the course site from their own git repos. But, that would be crazy. There is a fairly steep learning curve to learn git, and even though this is a Digital History class, I know that the tech skills will vary in the course.

*  Enter prose.io.  

Prose.io provides a web interface for creating and editing posts for github pages sites (and other github repos). It is being developed by the [people](http://developmentseed.org) behind the new [healthcare.gov](http://healthcare.gov), which even has its own github [repo](https://github.com/CMSgov/healthcare.gov). That's a pretty amazing thing, to see such an important site run with a static site generator. This is a CMS-free system, and its web interface is provided by Prose. Prose allows the content developers for healthcare.gov, or any site hosted on github, to edit and create new content with a web interface. Posts are written in markdown, and provides a means to editing post metadata. Any collaborator on the github repo can access these files, allowing for distributed teams to author posts without upfront knowledge of git (or ruby or jekyll).  

*  Very cool. 

Github pages runs with a built-in static site generator called [jekyll](http://jekyllrb.com/), which is written in the programming language ruby. Jekyll takes files written in [Markdown](http://daringfireball.net/projects/markdown/) and converts them to HTML, which is then injected into [Liquid](http://liquidmarkup.org/) templates.


This site is built with jekyll, hosted on [github](https://github.com/history580/history580.github.io), and utilizing prose for web authoring and [disqus](http://disqus.com/) for comments. I <strike>stole</strike> forked the css and templates from [Steve Ramsay](http://stephenramsay.us). Everything I've written and tweaked for the site has been done in vim in the terminal. (Long live the geekiest version of history geeks.)    

This is, above all, an experiment. I hope that along the way, students will learn where websites come from, what metadata is, and how powerful simple text files can be in their research and academic work. 


