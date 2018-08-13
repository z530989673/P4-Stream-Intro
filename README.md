# Perforce中streams的使用介绍
## 概述
### 为什么使用版本管理软件
![Alt text](https://github.com/z530989673/P4-Stream-Intro/blob/master/Pic/whyIsVersionControlImportant.png)
### 什么是Streams
branches with brains 

![Alt text](https://github.com/z530989673/P4-Stream-Intro/blob/master/Pic/stream.png)
### 为什么使用Streams
## 基本操作
### 创建分支
![Alt text](https://github.com/z530989673/P4-Stream-Intro/blob/master/Pic/createbranch.gif)
### 切换workspace
```diff
-先将自己当前目录下的修改revert,checkin或者shelve,以免本地的修改丢失!!!
```
直接将小电脑拖至对应分支即可切换workspace，
![Alt text](https://github.com/z530989673/P4-Stream-Intro/blob/master/Pic/switchWorkspace.gif)


推荐打开preference勾选如下内容：
![Alt text](https://github.com/z530989673/P4-Stream-Intro/blob/master/Pic/streamPreference.png)
### 合并分支
```diff
-先将父分支的修改合并至子分支，确认子分支功能正常后再copy至父分支！！
```
![Alt text](https://github.com/z530989673/P4-Stream-Intro/blob/master/Pic/mergeBranch.gif)
