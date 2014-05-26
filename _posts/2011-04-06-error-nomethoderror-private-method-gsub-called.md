---
date: 2011-04-06
layout: post
title: "ERROR NoMethodError: private method `gsub!' called"
thread: 164
categories: 软件
tags:  ruby rails errors
---

在网上看到这个问题：
--------------------------------------------------------

<P><em>When I run Webrick, the server starts without error, the application

	runs, database connections work and I can click through the pages and
	display data.  But it does not serve any stylesheets or javascript  
	files.  What's interesting is that images are displayed.  In the log  
	file, I get a 500 error after it attempts to retrieve a stylesheet or   
	javascript.  This occurs everytime.

	Example of attempt to retrieve prototype.js (a 500 error): 
	-------------

	127.0.0.1 - - [17/Mar/2010:23:52:52 Eastern Daylight Time] "GET 
	/javascripts/pro   
	totype.js?1268882775 HTTP/1.1" 500 338 
	Referer -> /javascripts/prototype.js?1268882775
	[2010-03-17 23:52:52] ERROR NoMethodError: private method `gsub!' called  
	for #<Class:0x44ee480> </em></P>
--------------------------------------------------------

找到解决这个问题的方法，可以试试 ：安装使用mongrel代替webrick
具体有：
>   * sudo gem install mongrel（windows 下去掉前面的sudo）
>   * script/server mongrel

试试看可不可以.



