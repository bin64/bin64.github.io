---
date: 2022-06-20 13:31:50+08:00
layout: post
title: SolidWorks 的 ViewZoomTo2 缩放命令
categories: 技术心得
tags: SolidWorks CAD 开发
---
在开发 SolidWorks 第三方工具的时候，常常发现程序在创建点或者线的命令会出错，要么无法从定义的点开始作图，要么从错误的地方开始作图。对于要选区的点的定义已经非常明确了，为什么还会出错了？

后来发现SolidWorks 在选取点的时候如果两个点因为缩放不够而离得很近，SolidWorks 就有概率无法选择这个点。这感觉就像两个点离得很近，在我们人眼中就变成了一个点一样。

解决这个问题的方法很简单，就是缩放视图就好了，用`ViewZoomTo2`这个命令，在合适的地方放大要选取的点，这样 SolidWorks 在操作的时候就不会出现无法选取或者选取错误的情况了。