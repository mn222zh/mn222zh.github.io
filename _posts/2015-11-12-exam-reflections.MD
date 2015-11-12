---
layout: post
title:  "exam reflections"
date:   2015-11-12 10:30:00
categories: education
comments: true
---

### What do you think of pre-compiling your CSS?

I have only limited previous experiance of CSS, but the advantages of pre-compiling CSS are quite obvious. The use of variables makes updates and maintenance of the CSS-config a lot easier. Nesting the config-statements – like HTML – makes the code friendlier to read and understand. Imports makes it possible to split the CSS-config in smaller parts and you increase the readability.

The basic template that came with the Jekyll-installation contained everything needed to get started. As this assignment was supposed to be “minor”, I decided not to rewrite the config from scratch. Instead I reused the initial scss file structure / config and only updated a few variables and added/removed smaller chunks of code until the new layout of the site was ok.

There are a few disadvantages. First, you need some tool to do the pre-compiling for you. This tool could be more of less complicated to get up and running.
Second, the debugging might get harder as line-numbers don’t match.


### What do you think of static site generators?

After creating a small web-site in course 1ME321, and having to edit the same HTML-code (headers, footers, menus etc) for every page, SSG seems like a gift from god. Jekyll as SSG offers functionality to use templates, merging parts like headers, footers, menus and text-contents into a static HTML-file. Jekyll also allows use of variables and scripting inside the documents, so that more advanced structures automatically can be generated.

There are many advantages with the SSG-concept;
A site can be maintained with minimal of effort.
A web-server for static pages are a lot more secure than a server running a database.
A web-server for static pages are a lot faster compared to dynamic pages that are built “on request”.

SSG’s are commonly used for blogs. But the concept is suitable for projects where you need high performance, scalability and stability. Maybe a frontend to a some large corporation, government etc. Rumors say that Obama used Jekyll during his election campaign in 2012..


### What is robots.txt and how have you configure it for your site?

Robots.txt is a file in the root of a website that gives instructions to robots from search-engines  which pages to index. The configuration for my site tells robots from Google that they are welcome to index the entire site, and that all other robots are not wanted.

{% highlight ruby %}
User-agent: Google
Disallow:

User-agent: *
Disallow: /
{% endhighlight %}



### What is humans.txt and how have you configure it for your site?

Humans.txt is a file in the root of a website where the owner of a site can write credits to people involved in the site, general information etc.

{% highlight ruby %}
/* TEAM */

    Developer: Magnus
    Mail: mn222zh(at)student.lnu.se
    From: Kalmar, Sweden

    Design???: Magnus
    Mail: mn222zh(at)student.lnu.se
    From: Kalmar, Sweden

/* SUPPORT */

    Support: Staff at LNU
    From: Kalmar, Sweden

    Support: Bea - my pet hedgehog, for keeping me company during late nights
    From: Box in the corner, Kalmar, Sweden


/* SITE */
    Language: English
    Standards: HTML5, CSS3
    Components: Jekyll, GitHub
    Software: WebStorm, Vagrant, Illustrator

{% endhighlight %}


### How did you implements comments to blog posts

I chose Disqus as platform for comments. Implementation was straight forward. A new disqus-account was created, and the suggested “universal code” was cut from disqus homepage and pasted into a new html-file in the _includes-directory called disqus.html.

An instruction to include the disqus.html-file was added to the _layouts/post.html  so that each post can be commented.


### What is Open Graph and how do you make use of it?

Open Graph is a protocol that enables a webpage to become a rich object by using metadata in the head of the webpage. This is usefull if you want to link a page into a facebook-post, as the site you link to will be displayed with a picture and other information.
