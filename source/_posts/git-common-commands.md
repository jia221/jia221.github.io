---
title: Git 常用命令速查表
date: 2026-09-20 17:00:00
tags:
  - Git
  - 速查表
categories:
  - 技术
cover: https://picsum.photos/800/450
---

日常开发中 Git 是最常用的工具之一，本文整理了常用 Git 命令速查表。

## 基础配置

```bash
# 设置用户名和邮箱
git config --global user.name "jia221"
git config --global user.email "jia221@jia-aa.top"

# 查看配置
git config --list
```

## 仓库操作

```bash
# 克隆仓库
git clone <url>

# 初始化新仓库
git init

# 添加远程仓库
git remote add origin <url>
```

## 日常操作

```bash
# 查看状态
git status

# 添加文件到暂存区
git add .
git add <file>

# 提交
git commit -m "commit message"

# 推送
git push origin main

# 拉取
git pull origin main
```

## 分支管理

```bash
# 查看分支
git branch

# 创建并切换分支
git checkout -b <branch-name>

# 切换分支
git checkout <branch-name>

# 合并分支
git merge <branch-name>

# 删除分支
git branch -d <branch-name>
```

## 回退操作

```bash
# 撤销工作区修改
git checkout -- <file>

# 撤销暂存区
git reset HEAD <file>

# 回退到上一个版本
git reset --hard HEAD^

# 查看提交历史
git log --oneline
```

## 标签管理

```bash
# 打标签
git tag v1.0.0

# 推送标签
git push origin v1.0.0

# 删除标签
git tag -d v1.0.0
```

## 总结

| 命令 | 用途 |
|------|------|
| `git status` | 查看状态 |
| `git add .` | 添加所有更改 |
| `git commit -m` | 提交更改 |
| `git push` | 推送到远程 |
| `git pull` | 拉取远程更新 |
| `git log` | 查看历史 |

熟练掌握这些命令，日常 Git 使用就足够了！
