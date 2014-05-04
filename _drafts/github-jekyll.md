---
layout: post
title: Create a blog in GitHub with Jekyll
description: "Create a blog with Jekyll and host it in GitHub."
category: articles
tags: [howto, tutorial, blog, jekyll, github]
---

<section id="table-of-contents" class="toc">
  <header>
    <h3>Contents</h3>
  </header>
<div id="drawer" markdown="1">
*  Auto generated table of contents
{:toc}
</div>
</section><!-- /#table-of-contents -->

So you have already a personal website hosted in [GitHub Pages](https://pages.github.com/) but now you want to make something a little bit more interesting out of it. Enter [Jekyll](http://jekyllrb.com/), a simple, blog-aware, static site generator.

> Transform your plain text into static websites and blogs.

Jekyll is a file-based CMS, so we won't be needing a database to create a blog. You can create your content with Markdown and Jekyll, via Liquid templates, generates a complete, static website ready to be served by any web server. Besides, it's the engine behind GitHub Pages, which allows it's users to host websites based on GitHub repositories. And so we are going to generate a site with Jekyll and host it in GitHub.

# Ingredients

* A GitHub Page
* Ruby installed on your computer
* Something interesting (according to you) to share with the world

# How to do it

First of all let's assume you have already created the personal repository in GitHub in which you are going to host your website and that you already have it cloned in the **~/my-awesome-site** dir. If you don't, now is a great time to check out my previous post go learn **how to host a personal website in GitHub**, go on, I'll wait.

## Install jekyll

So now we have to install **Jekyll**. As Jekyll is done written in Ruby, It's pretty easy to do this with **RubyGems** package manager. So we will install Ruby with our os package manager and Jekyll with RubyGems:

{% highlight bash %}
~$ apt-get install ruby
~$ gem install jekyll
{% endhighlight %}



{% highlight bash %}
~$ jekyll new my-awesome-site
~$ cd my-awesome-site
~/my-awesome-site$ jekyll serve
{% endhighlight %}

Now open your favorite browser and access **http://localhost:4000**.