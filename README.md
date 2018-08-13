# Perforce中stream的使用介绍
## 概述
### 为什么使用版本管理软件
### 什么是Stream
### 为什么使用Stream
## 基本操作
### 迁移depot
保留历史的迁移：p4 duplicate [from] [to]
### 创建分支
![Alt text](https://github.com/z530989673/P4-Stream-Intro/blob/master/Pic/createbranch.gif)
### 切换workspace
```diff
-先将自己当前目录下的修改revert,checkin或者shelve,以免本地的修改丢失!!!
```
### 合并分支
