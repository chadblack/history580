---
layout: post
title: getting started with github and prose.io
author: parzecoydigo
---

* a list for toc
{:toc}

# Up and running

As we discussed during our first meeting, participation on the class blog will be a key component of our learning process.  It will extend our discussions before and after class, and provide a platform for much of the important writing and critique that we will do together. In this post, I will provide the promised mini-tutorial on getting up and running on the class blog.  But, I would also like to write a bit about the systems that form the foundation for the site.  So, first up will be a step-by-step guide for getting GitHub and prose.io up and running, followed by some further discussion of jekyll, git, and HTML and Internet technologies. 

# Github

Our course site this semester is built on a set of free and open source technologies that evolved in response to the culture of open source software development over the course of the past few years. First and foremost among these is [GitHub](http://github.com).  As the company explains of itself, 

> GitHub is the best place to share code with friends, co-workers, classmates, and complete strangers.

We won't exactly be sharing code (though I hope by the end of the semester, a few of you will be). Instead, we'll be sharing our explorations of digital histories. Github still works really well for this, because our entire course site is built using [GitHub Pages](http://pages.github.com).  

Each of you will need a GitHub account in order to access the front end for writing our blog posts. This is as simple as signing up for any other web service. 

*Step 1.*

Sign up for a GitHub account. There, that was simple.

[![github](/images/githubsignup.png)](/images/githubsignup.png)

Ok, it's only slightly more complicated than that. Two things to think about-- what do you want your github identity to be and what do we do about passwords? You may make your ID whatever you'd like as long as your classmates know who you are. The ID name is important, because it is what you will use for the author info on your posts. Passwords are more difficult. If you use a password that is robust (ie, long and made up of a variety of types of characters, ie alphanumerics and symbols), it will be hard to remember. If you use a password that is easy to remember it likely won't be very robust. Might I suggest you consider using a password manager to generate passwords for you? If not, then at the very least do not use the same password for all of your accounts-- email, bank, gmail, github, etc. Doing that makes you more vulnerable. Onwrad, though.  

*Step 2.*

Email me your GitHub username, so that I can add it as a collaborator on the [course site repo](http://github.com/history580). That's even easier, assuming you have my email address. You do, don't you? It's up top over [there](http://dh.chadblack.net/info/syllabus/).  

---

# Prose.io

Once you have been added as a collaborator to the course repo, it will show up as one of your own repositories on your Github home page. With that, you could clone the repository onto your local machine, write your posts there, and push them back to the repository. I'm guessing that you didn't understand pretty much anything that I just wrote there, though. So, to make all of this easier on you, we are going to use a web editing interface provided through a service called [Prose.io](http://prose.io). To use prose, do the following.  

*Step 1:*

Make sure that you are logged in to your github account. 

*Step 2:*

Navigate your browser to [http://prose.io](http://prose.io). On the landing page, click on the "Authorize on Github" button.

[![prose](/images/prose.png){: width=600 }](/images/prose.png)

*Step 3*

Once you've authenticated, you will see a list of repos on your account. Unless you've gone ahead and created your own repos, the only one will be `history580.github.io`. Click on the repo, and you'll find yourself in the `_posts` folder, with access to all the previous posts written for the site and the ability to create new ones. 

[![prose folder](/images/prosefolder.png){: width=600 }](/images/prosefolder.png)

Click on the green button to create a new post.  


# Writing with Markdown

Prose.io was created by the web development team behind the government's new [healthcare.gov](http://healthcare.gov) site, which provides a portal to resources and the exchanges mandated by the Affordable Care Act. It is intended to be a web editor that provides an easy place to write text snippets that will be inserted into web page templates. Thankfully, it does not require you to write raw HTML, but rather uses a simple language syntax known as Markdown. Markdown was created by John Gruber with the intention of making it easier to write content for the web, and it has been an almost unbelievable success. There are now many favors of Markdown in the wild, but all of them share some basic syntax originally defined by Gruber. This syntax allows you to write in plain text, but signal to a processor how the text should be transformed into more semantically rich HTML. The syntax is not complicated, but does require a little bit of a learning curve. With it, you will be able to make links, embed images, write footnotes, use block quotes, produce ordered and unordered lists, and clearly define code snippets. 

You can find Gruber's original documentation on Markdown [here](http://daringfireball.net/projects/markdown/).  

I'm also writing a complete list of options for our version of Markdown [here](/info/markdown). Once it's done, you can simply print it out as a cheat sheet. 

There is also help from within prose.io by clicking on the **?**.  


# Back to creation

After clicking on the new button, you may enter your markdown-flavored text into the editor directly, or paste it in from a plain text file you wrote on your computer. If you go this route, it's important to use a text editor and **not** Word. 

Note too that you can click on `Edit` to revisit a post, or the trash can to delete it.

In any case, there are three last steps to publishing your post.  

*  Enter a title. Click on the lightly-shaded word *Untitled* and give your post a title. It should be descriptive of the content. Please don't go the lazy route of naming your post something like "Post 1" or "Print Proposal".  

*  Click on the metadata button on the right side of the screen. This will bring up a dialogue box. Fill your github username in as the author of the post. This is the name that will show up on our homepage listing of new posts, and also on the post itself.  


[![meta button](/images/meta.png){: width=600 }](/images/meta.png)

[![meta box](/images/metabox.png){: width=600 }](/images/metabox.png)

There are other metadata possibilities for that can be entered in the box, but we can leave that discussion till later.  

*  Save your changes. Really, what you're doing in saving is committing your changes to the repository, which is tracking every change made to the files on which the site is built. Each commit produces a new state. Make sure to enter a short message into the commit box documenting the changes that you made. If you don't enter anything, prose.io provides some boilerplate that will be recorded.  

[![commit dialogue](/images/commit.png){: width=600 }](/images/commit.png)

Note that the metadata that I've set to automatically generate, along with the metadata that you've entered, shows up appended to the top of your post between a set of triple dashes.

    ---
    layout: post
    published: true
    title: your title
    author: your name
    ---

That information helps `jekyll` create the site by setting important variables and choosing the appropriate template to put the new html into.  

# How it works  

I was going to end this post with a bit on the architecture of this site, and how it works so that you understand how our site is made. Instead, I think I'll encourage you to do two things: 

1. Right click on this page and choose 'View Source' and take some time to look at the html. Where did the content I wrote for this post get inserted? Where did the rest of the information come from? What does it do?  

2. Take some time to poke around the files on the course site repo, available to you through github, and see if you can intuit/figure out what each of them are doing. What do the various folders do? See what you can figure out. The [jekyll documentation](http://jekyllrb.com) might be a good source.  

Looking forward to your own first posts.  
