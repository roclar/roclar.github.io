---
layout: post
title: First Post!
---
This is my first post!  Yeah!

In order to get jekyll serving locally, I needed to execute it with the following command:

*bundle exec jekyll serve --drafts --watch*

As simply using *jekyll serve* results in a "Missing dependency: kramdown" error despite this library being present.

Both the [GitHub Jekyll with Pages](https://help.github.com/articles/using-jekyll-with-pages/) and [Stack Overflow](http://stackoverflow.com/questions/31417469/jekyll-ruby-kramdown-missing-dependency) recommend using *bundle exec*.
