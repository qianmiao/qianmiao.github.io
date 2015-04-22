---
layout: post
title: iphone crash log分析
comments: no
categories:
- Programming
tags:
- iOS
---

###复制文件

将deriveData对应app的build目录下得xxx.app和xxx.dSYM文件拷贝到同一文件夹


###执行命令

```
xcrun atos -o Alimei-iPhone.app.dSYM/Contents/Resources/DWARF/Alimei-iPhone -arch armv7 -l 
0x4000 0x009894d9 0x00988ba5 0x00986283 0x102ec74d

```

0x4000是基地址 0x009894d9 0x00988ba5 ...是对象地址  这些地址在crash log查看
