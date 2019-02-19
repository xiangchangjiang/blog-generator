---
title: git入门博客
date: 2019-02-19 10:50:55
tags:
---
## git init
  该命令创建一个空的Git仓库 - 基本上是创建一个具有objects，refs/head，refs/tags和模板文件的.git目录。 还创建了引用主分支的HEAD初始的一个HEAD文件。现有存储库中运行git init命令是安全的。 它不会覆盖已经存在的东西。 重新运行git init的主要原因是拾取新添加的模板(或者如果给出了--separate-git-dir，则将存储库移动到另一个地方)。

## git add
  将文件添加到**暂存区**。
  `git add 文件名` :一个一个添加
  `git add .`:一次性添加，将当前目录里所有变动都加到暂存区

## git commit
  `git commit -m “提交信息”`:提交暂存区到仓库区
  `git commit -v`:提交时显示所有diff信息



