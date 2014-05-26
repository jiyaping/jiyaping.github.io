---
date: 2011-04-09
layout: post
title: !binary |
  5bCGdG90byBibG9nIOaUvuWIsGhlcm9rdeS4ig==
thread: 164
categories: 软件
tags:  git heroku toto
---

toto使用ruby编写的一个超轻量的blog引擎，只提供了基本的文章管理，没有管理员界面，没有后台数据库，评论系统用的是disqus，什么都没有为什么选用这个呢，因为这样用起来会很灵活，可以添加自己喜欢
功能，可以将toto blog 很容易放到heroku上面，本文讲介绍4个方面：

1. 安装git
2. 使用heroku
3. 将toto放到heroku上
4. 简单的使用toto


#### *第一 安装git*

git是一个越来越流行的分布式的版本控制软件，。可以很方便的管理源代码，安装可以查看[github](http://help.github.com/win-set-up-git/)
讲解的特别详细。

ubuntu上面使用命令:
>  $ sudo apt-get install git-core git-gui git-doc

如果只是为了安装toto blog 那么可以不用专门申请github帐号，并且配置git帐号
当然建议按照github上面的说明一步一步做完。
<br />

#### *第二 使用heroku*

heroku是一个专门部署ruby应用，托管ruby代码，可以免费使用，但是有限制，具体细节见官网。

到[heroku](http://www.heroku.com)注册一个帐号

安装heroku
> sudo gem install heroku

添加SSH key
> ssh-keygen

然后连着按几个空格就可以了，然后：
> heroku keys:add

之后第一次使用heroku时候会提示你输入用户名和密码

#### *第三 将toto放到heroku上面*

> git clone git://github.com/cloudhead/dorothy.git  myblog

> cd myblog

> git init

> git add .

> git commit -ma "new blog"

> heroku create

> git push heroku master

> heroku open

如果没有错误，这样你就可以在你的浏览器中看到你的blog 首页的内容


#### *第四 简单的使用toto*

写一篇文章(例如：my first toto article)的流程：
> rake new

输入文章名字my first toto article
进入articles/目录会有一个刚才生成*.txt文件编写自己的文章，然后保存
> git add articles/(文件名字)

> git commit -ma "first article"

> git push heroku

> git open


就可以看到自己的文章

具体可以参见：[git#toto](https://github.com/cloudhead/toto)

































