---
layout: post
title: git gitee github 使用笔记
---
# git介绍
 
 > Git 是一个开源的分布式版本控制系统，用于敏捷高效地处理任何或小或大的项目。 Git 是 Linus Torvalds 为了帮助管理 Linux 内核开发而开发的一个开放源码的版本控制软件。 Git 与常用的版本控制工具 CVS, Subversion 等不同，它采用了分布式版本库的方式，不必服务器端软件支持。

# 安装git
[Git - Downloads (git-scm.com)](https://git-scm.com/downloads)
下载,右键到文件夹打开git bash

设置下个人数据
```shell
$ git config --global user.name "你的名字"
## 邮箱
$ git config --global user.email "email@example.com"
```


总而言之,就是一个管理代码或者资源文化的仓库系统
# 命令行使用
```shell
## 创建git仓库
git init
## 此时创建文件,创建好了之后输入以下指令提交
git add .
## 版本提交信息
git commit -m "要提交的信息"

## 查看仓库状态
git status

## 查看版本信息
git log

```
![](https://micah.fun:81/mkoss/img/Roaming/picgo/20211026--14-48-31-e7fbe4.png)

如果嫌输出信息太多，看得眼花缭乱的，可以试试加上`--pretty=oneline`参数：

## 版本回退
```shell
## HEAD^为上个版本 ^^ 为上上个 100个为`HEAD~100`
git reset --hard HEAD^

## 此时想返回最新的版本也有办法,找到对应的id前几位
git reset --hard 前几位id

```

## 删除文件
```shell
git rm xx文件

## 恢复版本库中的文件到工作区中
git checkout -- 文件名
```


# 远程仓库
## gitee
注册账号,注册记住你的邮箱

### 配置密钥
```shell
## 填入你的邮箱
ssh-keygen -t ed25519 -C "xxxxx@xxxxx.com"
## 查看
cat ~/.ssh/id_ed25519.pub

```

粘贴到gitee公钥管理
[SSH公钥 - Gitee.com](https://gitee.com/profile/sshkeys)

此时配置完毕
### 创建项目
创建一个对应语言的项目,克隆下来,再进行提交,或者初始化之后在git创建空项目,然后提交上去

### 推送到远程仓库
```shell
git push origin master
```
## github
//TODO 待完成
![](https://res.u-tools.cn/assets/avatars/8237f37fee7508026cc0f137e0986c3c.jpg)

