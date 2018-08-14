# Perforce中streams的使用介绍
## 概述
### 为什么使用版本管理软件
* 备份、合作、检索
![Alt text](https://github.com/z530989673/P4-Stream-Intro/blob/master/Pic/whyIsVersionControlImportant.png)
### 什么是Streams
* branches with brains  
![Alt text](https://github.com/z530989673/P4-Stream-Intro/blob/master/Pic/stream.png)
### 为什么使用Streams
* 更加清晰的分支关系  
![Alt text](https://github.com/z530989673/P4-Stream-Intro/blob/master/Pic/formerBranch.png)
![Alt text](https://github.com/z530989673/P4-Stream-Intro/blob/master/Pic/stream.png)
* 创建分支、切换分支、合并分支更加清晰便捷  
  详情请参考[创建分支](#创建分支)、[切换分支](#切换分支)、[合并分支](#合并分支)

## 基本操作
### 创建分支
![Alt text](https://github.com/z530989673/P4-Stream-Intro/blob/master/Pic/createbranch.gif)
### 切换分支
```diff
-先将自己当前目录下的修改revert,checkin或者shelve,以免本地的修改丢失!!!
```
直接将小电脑拖至对应分支即可切换分支，
![Alt text](https://github.com/z530989673/P4-Stream-Intro/blob/master/Pic/switchWorkspace.gif)


推荐打开preference勾选如下内容：
![Alt text](https://github.com/z530989673/P4-Stream-Intro/blob/master/Pic/streamPreference.png)
### 合并分支
```diff
-先将父分支的修改合并至子分支，确认子分支功能正常后再copy至父分支！！
```
![Alt text](https://github.com/z530989673/P4-Stream-Intro/blob/master/Pic/mergeBranch.gif)

## 工作流程
### 分支架构
![Alt text](https://github.com/z530989673/P4-Stream-Intro/blob/master/Pic/branchStructure.png) 

![Alt text](https://github.com/z530989673/P4-Stream-Intro/blob/master/Pic/branchStructure2.png)
### 如何开发功能
* 开发人员：在对应功能开发分支（蓝色）上提交修改。
* QA：无。
### 如何验收功能
* 开发人员：
** 验收前，先将主干分支合并至对应开发分支（蓝色）。
** 验收中：及时根据QA的反馈调整修改并上传至功能开发分支（蓝色）。
* QA：先在对应功能开发分支（蓝色）上测试，验证之后在copy至主干分支（灰色），再次验证后验收功能。
### 如何发布版本
* 开发人员：无。
* QA：在trunk上验收所有当前版本需要的功能后，创建release分支、设置权限、编译版本并发布。
### 如何修复发布版本中的缺陷
* 开发人员：根据QA提供的版本在对应release分支提交修改，修复缺陷。
* QA：给相关人员权限在对应release分支（黄色）中提交修复changelist，确认修复后，merge回主干分支（灰色），有冲突请咨询相关人员。

## 注意事项
### 切换分支还是切换workspace
* 切换分支(workspace不变）  
![Alt text](https://github.com/z530989673/P4-Stream-Intro/blob/master/Pic/switchBranchOp.gif)  
* 切换workspace  
![Alt text](https://github.com/z530989673/P4-Stream-Intro/blob/master/Pic/switchWorkspaceOp.gif)
### 分支权限（谁能合并？谁能创建？）
