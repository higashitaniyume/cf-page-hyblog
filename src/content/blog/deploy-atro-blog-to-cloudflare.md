---
title: '部署Astro项目到Cloudflare Pages服务中'
description: '此文章介绍了如何将Astro项目部署到Cloudflare Pages中以实现全球访问。'
pubDate: '2026-04-09'
heroImage: '../../assets/blog-placeholder-about.jpg'
---

## 零、先决条件

1. Cloudflare 账号
2. Github 账号
3. NodeJS 环境

## 一、创建项目模板

首先cd到一个新目录，运行命令

```bash
npm create astro@latest
```

在选择模板的地方选择“Blog”模板，然后初始化Git仓库。

>**提示**：如果在安装依赖的时候显示Time out，可以不管，完成后直接运行以下命令
>
>```bash
>npm install
>```

## 二、上传到Github

首先事先在Github上面新建一个repo，记住repo的https地址，然后在终端中输入以下命令：

```bash
git add .
git commit -m "feat: init blog project"
git branch -M main
git remote add origin <你的GitHub仓库地址>
git push -u origin main
```

然后等待上传成功

## 三、上传到Cloudflare

1. 首先访问[Cloudflare官网](https://dash.cloudflare.com/)
2. 在主页右上角看到“添加”按钮
3. 点击页面
4. 点击“导入现有 Git 存储库”那一项的“开始使用”按钮
5. 按照流程绑定Github账号
6. 选择你刚刚上传的储存库
7. 等待部署完成

## 四、大功告成

现在全球各地都能访问你的博客了（通过Cloudflare给你的域名*.page.dev访问）

以后你想写自己的文章，可以在项目的`src/content/blog/`文件夹内新建一个markdown文档，Astro会自动帮你管理路由！
