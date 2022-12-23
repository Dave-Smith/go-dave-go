---
title: "Hello World"
date: 2022-12-22T20:54:37-06:00
draft: true
---

## Hello, World.  Or Hugo

Is there anything like creating your own blog, instead of ya know just using one of the free sites.  I'm using Hugo this time around.  I've tried Jekyll and made some good stuff, but Hugo looks easier to use.

Because I don't know what else to write, I'm walking through setting up a Hugo site.

## Getting Started

Install Hugo
~~~ bash
brew install hugo
~~~

I'm using a Mac, so this works.  Pretty straight forward

## Create the site and add theme

~~~ bash
hugo new site quickstart
cd quickstart
git init
git submodule add https://github.com/chipzoller/hugo-clarity themes/hugo-clarity
echo "theme = 'hugo-clarity'" >> config.toml
hugo server
~~~

Checkout the site at http://localhost:1313

## Add blog post

~~~ bash
hugo new posts/my-first-post.md
~~~

This adds a new markdown file in the content directory.  The file has the appropriate front matter, set the draft flag set to true.

Edit the markdown in an editor.

## Preview the draft post

~~~bash
hugo server --buildDrafts
~~~

This is where is am right now.  

## Hosting

I created a site using Fly.io.  Next time i'll go over putting this into Github and setting up a GitHub Action to publish content changes.

