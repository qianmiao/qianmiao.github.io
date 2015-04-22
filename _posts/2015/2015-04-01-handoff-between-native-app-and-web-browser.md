---
layout: post
title: iphone crash log分析
categories:
- Programming
tags:
- iOS
---

###复制文件

```
xcrun atos -o Alimei-iPhone.app.dSYM/Contents/Resources/DWARF/Alimei-iPhone -arch armv7 -l 0x4000 0x009894d9 0x00988ba5 0x00986283 0x102ec74d

```

0x4000 0x009894d9的对象地址
