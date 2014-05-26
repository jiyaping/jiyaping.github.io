---
date: 2011-04-09
layout: post
title: !binary |
  5pCt5bu6cnVieSBvbiByYWlscyDnjq/looM=
thread: 164
categories: 软件
tags:  ruby rails howto
---

    &nbsp;&nbsp;&nbsp;&nbsp;ruby on rails 是基于ruby语言的一个MVC全栈(full stack)式框架，更多关于Rails的介绍[Wiki](http://zh.wikipedia.org/wiki/Ruby_on_Rails)

安装分为两步:

1. 安装ruby
2. 安装rails


#### *安装ruby*

windows上面直接下载安装包：[Ruby 1.9.1-p430 RubyInstaller](http://rubyforge.org/frs/download.php/72075/rubyinstaller-1.9.1-p430.exe)
安装时注意要将添加到path的选项勾选上

ubuntu上面直接输入：
>  sudo apt-get install ruby-full

默认安装的是1.8
要按安装1.9.x
>  sudo apt-get install ruby1.9.1-full


windows和ubuntu上确认是否安装成功：
>  ruby -v

显示版本号则安装成功，查看rubygem(ruby语言的软件包管理工具)是否成功安装：
>  gem -v

一般来安装ruby时都会同时安装gem如果没有安装到*[此处](https://rubyforge.org/frs/?group_id=126&release_id=45823)*下载相应系统对应的安装文件，解压到指定位置，进人
相应位置，执行下面的命令：
> ruby setup.rb

ok！～搞定gem之后，其他ruby的包就很好安装了，几个个命令就可以搞定

#### *安装rails*
搞清楚rails所必需的包之后完全可以像安装gem那样将那些必须包完全手工安装，但是有了gem之后就没有那个必要了，并且不容易出错

安装最新版本：
>  gem install rails

ubuntu上前面要加上sudo

安装历史版本(例如2.2.3):
>  gem install -v 2.2.3 rails


**当然你如果在windows学习使用rails那么下载使用[InstantRail](http://rubyforge.org/projects/instantrails/)将是最简单的，里面包含了你所有你需要的工具，包括数据库**


那么现在就可以使用创建第一rails app了:
>  $rails appTest

>  $cd appTest

>  $script/server

默认可以在127.0.0.1：3000访问，最新版本的rails有些改变:
>  $rails new appTest

>  $cd appTest

>  $rails server


访问127.0.0.1：3000就可以看到欢迎页面







