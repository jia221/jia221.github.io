---
title: 使用 Hexo + GitHub Pages 搭建个人博客
date: 2026-09-20 16:30:00
tags:
  - Hexo
  - GitHub Pages
  - 教程
categories:
  - 技术
cover: https://picsum.photos/800/450
---

本文记录了本博客从零搭建的完整过程，包括 Hexo 安装、主题配置、GitHub Pages 部署和自定义域名设置。

## 环境准备

搭建 Hexo 博客需要以下环境：

```bash
# 检查环境
node --version   # Node.js >= 14
npm --version
git --version
```

## 安装 Hexo

```bash
# 全局安装 Hexo CLI
npm install -g hexo-cli

# 初始化博客
hexo init my-blog
cd my-blog
npm install
```

## 安装 Butterfly 主题

```bash
npm install hexo-theme-butterfly hexo-renderer-stylus hexo-renderer-pug --save
```

在 `_config.yml` 中设置主题：

```yaml
theme: butterfly
```

## 创建文章

```bash
# 创建新文章
hexo new "我的第一篇文章"

# 创建关于页面
hexo new page about
```

## 本地预览

```bash
hexo server
```

浏览器访问 `http://localhost:4000` 即可预览。

## 部署到 GitHub Pages

1. 在 GitHub 创建仓库（用户名.github.io 或自定义名称）
2. 配置 GitHub Actions 自动部署
3. 在仓库 Settings → Pages 中设置源为 GitHub Actions
4. 添加 CNAME 文件绑定自定义域名

## 自定义域名

在 `source/` 目录下创建 `CNAME` 文件，写入域名：

```
jia-aa.top
```

然后在域名 DNS 中添加 CNAME 记录指向 GitHub Pages 地址。

## 总结

整个搭建过程的核心步骤：

| 步骤 | 说明 |
|------|------|
| 环境准备 | Node.js + Git |
| Hexo 安装 | npm install -g hexo-cli |
| 主题配置 | Butterfly |
| 内容创作 | Markdown |
| 自动部署 | GitHub Actions |
| 域名绑定 | CNAME + DNS |

享受写作的乐趣吧！
