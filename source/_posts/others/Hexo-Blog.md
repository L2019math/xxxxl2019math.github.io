---
title: Hexo-Blog
date: 2022-01-28 19:18:11
categories:
tags:
cover: 
---


# 思路

依照教程创建hexo 博客，更换主题，魔改主题

采用的是 `butterfly` 主题，背景设置全局透明渐变，本地搜索，Valine 评论系统，改了字体样式和列表格式

# 过程

## 基础篇

[入门教程](https://zhuanlan.zhihu.com/p/102592286)

[butterfly主题教程](https://butterfly.js.org/)

[发文教程](https://zhuanlan.zhihu.com/p/22632478)

[hexo+github搭建个人博客 2019.2 详细教程](https://blog.csdn.net/qq_40871466/article/details/86763540)

## 魔改篇

主题设置中发现用 hexo s 命令查看网页部署时是成功的，但是 hexo d 部署到GitHub上就不行，后来等一会就行了，可能是有延迟。

- [akilar的博客](https://akilar.top/posts/ebf20e02/)
- [colopen的博客](https://www.colopen-blog.com/)
- [guole的美化笔记](https://guole.fun/posts/butterfly-custom/)
- [hexo官方文档](https://hexo.io/docs/tag-plugins)
- [友链朋友圈](https://zfe.space/post/friend-link-circle.html)

# 细节

## Git操作

```bash
// 移除仓库，重新添加
git remote rm origin
git remote add origin git@github.com:L2019math/text.git

// 添加文件到暂存区
git add acwing.txt
// 提交到仓库中 ，引号内为描述操作
git commit -m "commit text file"
// push 到远程服务器（github）
git push origin main
```

## 常用指令
```bash
// 清除缓存
hexo clean
// 静态部署generate
hexo g
// 启动本地服务器
hexo s
// 部署到仓库deploy
hexo d
// 新建文章，"...." 引号内为文章题目
// md文档中可设置 分类，标签，图片
hexo new “....”
// hexo 一键三连
hexo cl && hexo g && hexo s
```

## 评论

采用的是 [Valine](https://valine.js.org) 作为评论系统，因为他可以匿名评论hh

设置邮箱的头像：[gravater](https://en.gravatar.com/)
