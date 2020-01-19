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





{% note default %}

{% endnote %}
default
primary
success
info
warning
danger