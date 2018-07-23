---
title: git放弃本地所有修改
date: 2018-07-23 19:34:50
tags:
- 编程
- 工具
categories:
- 编程
---

# 放弃本地单个文件
* 未使用 git add 的文件 
  `git checkout -- filepathname`
  如果是新建的文件，untracked状态自己手动删除即可
* 使用了 git add 的文件
  ` git reset HEAD filepathname`
* 已经 git commit 的文件
 可以退回到上一次提交: `git reset --hard HEAD^ `，
 也可以退回到指定提交：`git reset --hard  commitid`
 
# 放弃本地所有修改
* `git checkout -- .` #本地所有修改的。没有的提交的，都返回到原来的状态
* `git stash` #把所有没有提交的修改暂存到stash里面。可用git stash pop回复。
* `git reset --hard HASH` #返回到某个节点，不保留修改。
* `git reset --soft HASH` #返回到某个节点。保留修改


