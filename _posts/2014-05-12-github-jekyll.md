---
layout: post
title: Create a blog in GitHub with Jekyll
description: "Create a blog with Jekyll and host it in GitHub."
category: articles
tags: [howto, tutorial, blog, jekyll, github]
image:
  feature: jekyll.jpg
---

So you have already a personal website hosted in [GitHub Pages](https://pages.github.com/) but now you want to make something a little bit more interesting out of it. Enter [Jekyll](http://jekyllrb.com/), a simple, blog-aware, static site generator.

> Transform your plain text into static websites and blogs.

Jekyll is a file-based CMS, so we won't be needing a database to create a blog. You can create your content with Markdown and Jekyll, via Liquid templates, generates a complete, static website ready to be served by any web server. Besides, it's the engine behind GitHub Pages, which allows it's users to host websites based on GitHub repositories. And so we are going to generate a site with Jekyll and host it in GitHub.

# Ingredients

* A GitHub Page
* Ruby installed on your computer
* Something interesting (at least interesting for you) to share with the world

# How to do it

First of all let's assume you have already created the personal repository in GitHub in which you are going to host your website and that you already have it cloned in the **~/my-awesome-site** dir. If you don't, now is a great time to check out my previous post about [how to host a personal website in GitHub](/articles/github-pages/), go on, I'll wait. Ok, now we can continue.

## Install jekyll

In order to be able to be able to see our page locally while we are creating the posts, we have to install **Jekyll**. As Jekyll is done written in Ruby, It's pretty easy to do this with **RubyGems** package manager. So we will install Ruby with our os package manager and Jekyll with RubyGems:

{% highlight bash %}
~$ apt-get install ruby
~$ gem install jekyll
{% endhighlight %}

## Create the blog

Now with jekyll already installed we are going to create the page in the following directory:

{% highlight bash %}
~$ jekyll new my-awesome-site
~$ cd my-awesome-site
~/my-awesome-site$ jekyll build
~/my-awesome-site$ jekyll serve
{% endhighlight %}

Open your favorite browser and access **http://localhost:4000**. Voilà, you've got your blog up and running in your local machine. This would be a great moment to personalize the title of your blog by editing the **_config.yml** configuration file. The content of this file, by default, will be quite simple:

{% highlight YAML %}
name: My awesome site
markdown: redcarpet
pygments: true
{% endhighlight %}

## Add posts

Now adding posts is as easy as creating a new file in the **_posts** directory. The filename has to be in a particular format:

{% highlight bash %}
YYY-MM-DD-short-name-of-article.extension
{% endhighlight %}

The extension depends on the markdown of the markdown you are using with jekyll, the default one is **markdown**. So after creating your new post, build and serve your blog to see the results:

{% highlight bash %}
~/my-awesome-site$ jekyll build
~/my-awesome-site$ jekyll serve
{% endhighlight %}

## Personalizing with templates

So what we have done until now is very interesting but not so exciting look-and-feel wise. Enter [jekyll themes](http://jekyllthemes.org/). All over the Internet there are many themes to use with jekyll. Usually using one of these themes is as easy as forking the theme's repository and modifing the configuration in order to meet your needs.

This very blog is based on the [HMFAYSAL V2 Theme](https://github.com/hmfaysal/Jekyll-HMFAYSAL-V2-Theme) and there are many other possibilities on the Internet.

## Publishing the blog in GitHub

So you have succesfully created a blog, prepared a couple of posts and personalized the shit out of it with a cool template. Now in order to get it published in your GutHub account you just have to commit your changes and push it to your repository. Whatever you push in the **master** branch will be automatically publish in your GitHub page.