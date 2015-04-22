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

0x4000是基地址 0x009894d9 0x00988ba5 等是对象地址  

这些地址在crash log查看

###crash log

```
Thread 22 Crashed:
0   libobjc.A.dylib                     0x372d66ba 0x372b6000 + 132794
1   Alimei-iPhone                       0x009894d9 0x4000 + 9983193
2   Alimei-iPhone                       0x00988ba5 0x4000 + 9980837
3   Alimei-iPhone                       0x00986283 0x4000 + 9970307
4   libdispatch.dylib                   0x378272e3 0x37826000 + 4835
5   libdispatch.dylib                   0x3782f729 0x37826000 + 38697
6   libdispatch.dylib                   0x37829aad 0x37826000 + 15021
7   libdispatch.dylib                   0x37830f9f 0x37826000 + 44959
8   libdispatch.dylib                   0x378323c3 0x37826000 + 50115
9   libsystem_pthread.dylib             0x3798edc1 0x3798e000 + 3521
10  libsystem_pthread.dylib             0x3798eb14 0x3798e000 + 2836
```
