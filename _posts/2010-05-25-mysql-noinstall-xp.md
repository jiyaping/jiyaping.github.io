---
date: 2011-05-25
layout: post
title: !binary |
  TXlTcWwtbm9pbnN0YWxsIHhw54mI55qE5a6J6KOF
thread: 164
categories: 软件
tags:  mysql database
---


利用网上查着资料，今天装了个mysql，很简单的介绍一下：
（我的步骤）
1.将下载的文件解压到e盘，重命名为mysql

2.mysql在文件夹下，新建my.ini文件,将此文件夹下的其他(*.ini)文件(我用的是my-large.ini)内容copy到my.ini里面

3.修改my.ini内容,在相应的位置[client][mysqld][mysql]后面添加相应的内容，如下
    [client]
       default-character-set = utf8

    [mysqld]
       default-character-set = utf8
       default-collation=utf8_bin
       init_connect='SET NAMES utf8'
       basedir=e:\mysql
       datadir=e:\mysql\data

    [mysql]
        default-character-set=utf8

4.从命令控制窗口进入e:\mysql\bin目录下面
 键入命令  mysqld --install mysql --defaults-file="e:\mysql\my.ini"  回车
若提示正确，就ok了

5.开启MySQL服务 
  执行命令 net start mysql

6.运行mysql -u root -p
  然后会提示输入密码就可以了，初始密码为空，直接enter就ok了！~

