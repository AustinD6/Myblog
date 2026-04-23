---
title: Git 常用命令速查表
date: 2026-04-21 14:00:00
tags:
  - Git
  - 工具
categories:
  - 技术笔记
---

Git 是现代开发中不可或缺的版本控制工具。本文整理了我在日常开发中最常用的 Git 命令。

## 基础配置

```bash
# 设置用户名和邮箱
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# 查看配置
git config --list
```

## 仓库操作

```bash
# 初始化仓库
git init

# 克隆远程仓库
git clone https://github.com/user/repo.git

# 添加远程仓库
git remote add origin https://github.com/user/repo.git
```

## 提交操作

```bash
# 查看状态
git status

# 查看具体修改
git diff

# 添加文件到暂存区
git add filename.txt
git add .  # 添加所有文件

# 提交修改
git commit -m "commit message"

# 撤销修改
git checkout -- filename  # 丢弃工作区修改
git reset HEAD filename   # 撤销暂存区修改
```

## 分支操作

```bash
# 查看分支
git branch

# 创建分支
git branch feature-branch

# 切换分支
git checkout feature-branch
git switch feature-branch  # 新语法

# 创建并切换
git checkout -b feature-branch
git switch -c feature-branch  # 新语法

# 合并分支
git merge feature-branch

# 删除分支
git branch -d feature-branch
git branch -D feature-branch  # 强制删除
```

## 远程操作

```bash
# 拉取代码
git pull origin main

# 推送代码
git push origin main

# 查看远程仓库
git remote -v
```

## 日志查看

```bash
# 查看提交历史
git log
git log --oneline  # 简洁格式
git log --graph    # 图形化显示

# 查看指定文件的历史
git log filename
```

## 标签操作

```bash
# 创建标签
git tag v1.0.0

# 推送标签
git push origin v1.0.0

# 删除本地标签
git tag -d v1.0.0

# 删除远程标签
git push origin :refs/tags/v1.0.0
```

## 实用技巧

```bash
# 储藏当前工作
git stash
git stash pop

# 撤销最后一次提交（保留修改）
git reset --soft HEAD~1

# 查看谁修改了某行代码
git blame filename

# 清理未跟踪文件
git clean -fd
```

---

掌握这些命令可以大大提高开发效率。建议熟记常用命令，忘记时随时查阅这篇笔记！