---
layout: post
title: "在Github Pages上使用Octopress"
date: 2013-03-15 21:05
comments: true
categories: octopress
---

本来是想折腾一个个人技术wiki的，结果不小心看上了Octopress。之前就在Lucifr的个人博客上看到他各种折腾Octopress，现在先用一段看看。  

因为在自己的Godaddy空间上折腾ruby， octopress， git之类的太麻烦，因为尝试了一下很流行的在github pages上部署octopress的方法。具体方法其实Octopress官网的文档介绍的很清楚，详见[Deploying to Github Pages](http://octopress.org/docs/deploying/github/)  
> 其实[Setup Octopress to Godaddy](http://javier.pedemonte.us/blog/2011/10/31/setup-octopress-on-godaddy/)的方法也有，但现在真心觉得godaddy太慢，不爱用。

# I. Github Pages

在Github上新建一个repository，名字就是`username.github.com`，username即Github用户名，然后保存为master branch。这样几分钟后，在浏览器访问这个域名即可。  

![](http://younggive.github.com/images/githubpage_initial.png)  

至此，Github Pages初始配置完成。

# II. Octopress

## Before You Begin

1. Install Git
2. Install Ruby 1.9.3 using either rbenv or RVM (this requires brew/Macports on Mac)

## Setup Octopress


    git clone git://github.com/imathis/octopress.git my_blog
    cd my_blog      # If you use RVM, You'll be asked if you trust the .rvmrc file (say yes)
    ruby --version  # Should report Ruby 1.9.3

其中`my_blog`文件夹即刚才创建的`username.github.com`的本地文件家。
这里直接通过git把octopress下载到博客所在文件夹的话可能引起octopress的repository信息和`username.github.com`信息冲突的问题，故可以先git clone到一个临时文件夹，然后将此临时文件夹下的内容全部拷贝到my_blog文件夹下，然后再进行`cd my_blog`等步骤。

下一步安装依赖包  

    gem install bundler
    rbenv rehash # Necessary if used rbenv
    bundle install

安装Octopress主题  

    rake install


## Deploy Octopress to Github

    rake setup_github_pages

这个命令将询问你Github Pages repository的url，按照提示信息的格式:  
"git@github.com:username/username.github.com.git"

当这个命令运行完成之后，你的github pages repo会有两个branches: master branch用于静态页面的发布("my_blog/_deploy"的内容)，source branch用于保存你的blog内容（"my_blog"目录中除了"_deploy"的其它内容）

下一步运行：

    rake generate
    rake deploy

随后，将生成博客的静态页面并被放置到`_deploy/`下面，并且完成git commit/git push命令到master branch

最后一步，由于`rake deploy`命令只是将`_deploy/`文件夹下生成的网站发布了，如果想要commit博客的source code，还需要

    git add .
    git commit -m 'your message'
    git push origin source


