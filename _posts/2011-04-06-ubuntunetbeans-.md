---
date: 2011-04-06
layout: post
title: !binary |
  dWJ1bnR15LiKbmV0YmVhbnMg5bCP5bCP55qE5LyY5YyW
thread: 164
categories: 软件
tags:  ubuntu netbeans
---


主要是修改 etc/netbeans.conf 文件

**第一步**：将netbeans改成英文界面：

在netbeans_default_options项中加入 “-J-Duser.language=en”

**第二步**：抗锯齿

在netbeans_default_options项中加入 “-J-Dsun.java2d.pmoffscreen=false -J-Dapple.laf.useScreenMenuBar=true -J-Dsun.java2d.noddraw=true -J-Dawt.useSystemAAFontSettings=LCD”

**第三步**：重启netbeans在options中选择fonts&colors中选择一个适合到字体 ，我用的是courier字体


