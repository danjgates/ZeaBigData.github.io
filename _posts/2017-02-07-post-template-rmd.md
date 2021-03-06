---
layout: post
title: "Post Template using Rmd"
date: 2017-02-07
author: Jinliang Yang
editor: 
reviewer: 
categories: [tutorial, general]  
tags: [github, general, Rmarkdown, jekyll, rstats, servr]  
comments: true  
archive: true

---



For more details on using R Markdown see <http://rmarkdown.rstudio.com>.

We need to install R package [servr](https://github.com/yihui/servr) to convert Rmd to Markdown.


{% highlight r %}
install.packages('servr')  # stable version; use a CRAN mirror, or
install.packages('servr', repos = 'http://yihui.name/xran')  # devel version

### run the following:
library(servr)
jekyll(dir = ".", input = c(".", "_source", "_posts"), 
       output = c(".", ".", "_posts"), script = c("Makefile", "build.R"), serve = FALSE, 
       command = "jekyll build")
{% endhighlight %}


The [other steps](http://zeabigdata.org/2016/10/contribute/) are the same as using Markdown for a post.


