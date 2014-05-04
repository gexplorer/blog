---
layout: post
title: Host your personal site in GitHub
description: "Create a personal site and host it in GitHub."
category: articles
tags: [howto, tutorial, host]
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

So you want to create a personal website but you don't want to use any big and fancy service like Wordpress. If you know what **GitHub** is and you are not afraid of source code, this is your howto. If you didn't understand the previous sentence or just end up here by accident you can leave whenever you want, but to make the visit worth, heres a picture that I never get tired of:

<figure>
	<img src="http://awesomelyluvvie.com/wp-content/uploads/2012/12/Lenny-Kravitz-Giant-Scarf.jpeg">
	<figcaption>Lenny Kravitz with a big ass scarf.</figcaption>
</figure>

# Ingredients

* A GitHub account
* A basic knowledge of git
* A will to have a personal page in HTML

# Howto

If you made it pass the introduction, the odds are that you already have your own GitHub account. Let me introduce you to [GitHub Pages](https://pages.github.com/). As it turns out it is possible to host one static site per GitHub account and organization, and unlimited project sites. Project sites are what it sounds, pages for GitHub hosted projects. What we are going to create is a user page.

> Hosted directly from your [GitHub repository](https://github.com/). Just edit, push, and your changes are live.

First of all you need to go to your GitHub account and create a repository with the following name **username.github.io** where **username** is your GitHub username. This is very important, if it is not exactly your username, the page won't work.

Clone your new repository into your machine:
{% highlight bash %}
~$ git clone https://github.com/username/username.github.io myblog
{% endhighlight %}

Now you are ready to start publishing your own GitHub page. Whatever you push into the repository (in the **master** branch), will be published in the url correponding to the name of the repository **username.github.io**. The main limitation of this hosting is that the pages will have to be static HTML, with no server side scripting.

If you want to give it a try, create an **index.html** in the root of your repository, with some example code:
{% highlight html %}
<html>
	<head>
		<title>Hello world!</title>
	</head>
	<body>
		<p>Hello World!</p>
	</body>
</html>
{% endhighlight %}

Now to publish it into your GitHub page you only have to push it into your repository **commit** and **push** it to the master branch. The first time you do it it might take some time to publish the site. Now check out the results in your **username.github.io** site.