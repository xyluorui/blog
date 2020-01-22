---
title: Git-cheat-sheets
date: 2020-01-19 13:11:42
tags: Git
---

在本章内容中记录Git相关的命令，方便以后查询使用！

<!--more-->
# Git Cheat Sheet

{% note default %}
## 初始化仓库

### 初始化仓库

```
$ git init
```

### 初始化裸仓库

```
$ git init --bare
```

### 克隆仓库

```
$ git clone <git-repo>
```

{% endnote %}

{% note primary %}
## 配置
### 编辑配置文件

```
$ git config [--global] -e
```

### 列出配置信息

```
$ git config -l
```

### 获取相应的配置

```
$ git config --get core.editor
```

### 配置用户邮箱

```
$ git config --globle user.email <mail>
```

### 配置用户名

```
$ git config --globle user.name <name>
```

### 输出彩色信息

```
$ git config color.ui true
```

### 设置文件名大小写敏感

```
$ git config core.ignoreCase false 
```

### 设置推送策略为 simple

```
$ git config push.default simple
```

### 设置git编辑器是vim

```
$ git config --globle core.editor vim
```

### 设置命令别名

```
$ git config --globle alias.co checkout
```

{% endnote %}

{% note success %}

## 忽略文件
### 添加本项目的忽略文件

```
$ vim .gitignore
```

### 添加本项目的忽略文件并不把此文件纳入版本管理

```
$ vim .git/info/exclude
```

### 设置全局忽略文件

```
$ gti config --global core.excludesfile `/.gitignore
```

### 对已加入版本管理的文件不做更改检查

```
$ git update-index --n0-assume-unchanged<file>
```

{% endnote %}

{% note info %}

## 添加删除移动文件
### 添加所有文件到缓存区，包括未追踪文件

```
$ git add -A
```

### 更新暂存区文件

```
git add -u
```

### 交互式添加文件到暂存区

``` 
git add -p
```

### 工作区与暂存区删除文件

```
git rm <file>
```

### 仅暂存区删除文件

``` 
$ git rm --cached <file>
```

### 重命名暂存区文件

```
$ git mv <file> <filel>
```

{% endnote %}


{% note info %}

{% endnote %}

{% note default %}

{% endnote %}
default
primary
success
info
warning
danger