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
$ git add -u
```

### 交互式添加文件到暂存区

``` 
$ git add -p
```

### 工作区与暂存区删除文件

```
$ git rm <file>
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

## 工作区状态
### 查看工作区信息

```
$ git ststus
```

### 查看工作区信息并显示分支及追踪信息

```
$ git status -sb
```

### 查看忽略文件的信息

```
$ git status --ignored
```

### 列出忽略文件

```
$ git check-ignore *
```

{% endnote %}


{% note info %}

## 显示更改

### 显示工作区与暂存区的不同

```
$ git diff
```

### 显暂存区与本地仓库的不同

```
$ git diff --cached
```

### 显示工作区、暂存区与本地仓库的不同

```
$ git diff HEAD
```

### 仅显示改变的文件

```
$ git diff --name-only
```

### 比较两次提交的差异

```
$ git diff <commit> <commit>
```

### 显示某次commit所做的更改

```
$ git show <commit>
```

{% endnote %}

{% note info %}

## 列出文件信息

### 列出暂存区文件

```
$ git ls-files
```

### 列出忽略文件与未追踪文件

```
$ git ls-files -o
```

### 子目录中显示所在位置

```
$ git ls-files --full-name
```

{% endnote %}

{% note info %}

## 储藏与备份

### 储藏(stash)工作区相对暂存区更改的文件

```
$ git stash
```

### 储藏文件并添加描述信息

```
$ git stash save <message>
```

### 恢复最后一次储藏的文件

```
$ git stash apply
```

### 恢复最后一次储藏的文件并删除此次存储记录

```
$ git stash pop
```

### 查看储藏列表

```
$ git stash list
```

{% endnote %}


{% note info %}

## 恢复工作区

### 重置工作区某文件

```
$ git checkout --<file>
```

### 重置工作区

```
$ git checkout
```

### 列出将要清除的未追踪文件

```
$ git clean -n
```

### 清除未追踪文件

```
$ git clean -f
```

### 清除忽略文件

```
$ git clean -Xf
```

### 清除未追踪目录及文件

```
$ git clean -df
```

{% endnote %}


{% note info %}

## 回退版本

### 重置暂存区

```
$ git reset
```

### 重置工作区和暂存区

```
$ git reset --hard
```

### 恢复本分支到某次提交，重置工作区与暂存区

```
$ git reset --hard <commit-ish>
```

### 恢复本分支到某次提交

```
$ git reset --soft <commit-ish>
```

### 恢复本分支到某次提交，重置暂存区

```
$ git reset --mixed <commit-ish>
```

### 反向恢复一个提交并生成新的提交

```
$ git revert <commit>
```

{% endnote %}

{% note info %}

## 分支

### 列出本地分支

```
$ git branch
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