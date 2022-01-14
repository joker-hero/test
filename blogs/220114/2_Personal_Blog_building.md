---
title: 基于Vuepress+vercel的个人博客
date: 2022-01-06
tags:
 - 个人博客搭建
 - Vuepress
 - vercel
categories:
 - 基于Vuepress+vercel的个人博客
---

:::tip

​		个人博客是一个展示自我的平台，自由地发布自己的文章，让大众认识自己、欣赏自己，同时也能将自己的学术、观点、思想得到推广。可以记录自己的学习经历，对自己的知识查漏补缺，堆积阅历。

:::

## Vuepress介绍

VuePress 由两部分组成：一个以 Vue 驱动的主题系统的简约静态网站生成工具，和一个为编写技术文档而优化的默认主题。它是为了支持 Vue 子项目的文档需求而创建的。

由 VuePress 生成的每个页面，都具有相应的预渲染静态 HTML，它们能提供出色的加载性能，并且对 SEO 友好。然而，页面加载之后，Vue 就会将这些静态内容，接管为完整的单页面应用程序(SPA)。当用户在浏览站点时，可以按需加载其他页面。

在此我们使用的是主题Vuepress-theme-reco@1.6.1。





## Vuepress特性

- [内置 markdown 扩展](http://caibaojian.com/vuepress/guide/markdown.html)，针对技术文档进行了优化
- [能够利用内嵌在 markdown 文件中的 Vue 代码](http://caibaojian.com/vuepress/guide/using-vue.html)
- [以 Vue 驱动的自定义主题系统](http://caibaojian.com/vuepress/guide/custom-themes.html)
- PWA 支持
- Google Analytics 集成
- 一个默认主题：
  - 响应式布局
  - 可选的主页
  - 简单、开箱即用、基于标题的搜索功能
  - 可定制的导航栏和侧边栏
  - 自动生成的 GitHub 链接和页面编辑链接





## 静态托管平台-vercel

​        服务器和域名利用vercel的免费资源。Vercel是前端团队的最佳工作平台，免费并且上手简单。类似于github page，但远比github page强大，速度也快得多得多，而且将Github授权给vercel后，可以达到最优雅的发布体验，只需将代码轻轻一推，项目就自动更新部署。





## 博客搭建

首先到官方demo仓库选择对应版本下载，这里选择1.X版本。https://github.com/vuepress-reco/vuepress-theme-reco-demo/tree/demo/1.x

进入demo仓库点击分支选择1.X版本下载压缩包。

![image-20220114085901869](/g.png)

下载解压完成之后，本地运行可以使用命令yarn dev。

![image-20220114095932293](/1.png)

![image-20220114100011912](/2.png)

运行构建完成后，会在本地的8081端口打开。

![image-20220114093038713](/i.png)

大致界面如图所示：

![image-20220114092934630](/h.png)

接下来，将下载的demo仓库与远程的Github仓库连接。

连接命令如下：

![image-20220114094327971](/j.png)

以下则表示已经push到Github仓库：

![image-20220114100505600](/3.png)



打开vercel官方网站，网站地址https://vercel.com。

使用Github登陆，创建一个项目，创建完成之后会检测到Github刚刚上传的项目。

![image-20220114095032576](/q.png)

将Github项目导入到vercel中，就可以自动在vercel上构建。

当每次修改或写完文章之后推送到Github仓库上，vercel会自动检测Github仓库更新，并自动拉取再自动构建在vercel服务器上。

自动构建好之后会发送邮件到绑定的邮箱。

![image-20220114100632349](/4.png)



现在，我们的个人博客已经成功搭建好了。我们可以使用vercel给我们提供的服务器来访问我们的个人博客。

![image-20220114100930574](/5.png)



## 博客的个性化设计

官方文档提供了较为详细的文档参考[vuepress-theme-reco (recoluan.com)](https://vuepress-theme-reco.recoluan.com/views/1.x/)

我们可以根据自己喜欢进行配置。



## 博客文章目录

通常将博客文章放在blogs目录下，注意路径下尽量不出现中文，否在容易出现乱码问题。因为浏览器在访问文件的时候利用URL传递参数这种方式是依赖与浏览器环境中的，也就是说URL及URL中包含的各个key=value格式的传递参数键值对参数是在浏览器地址栏中的处理原理处理相应编码后传递至后台进行解码的。

由于我们没有进行任何处理，此时javascript请求URL并传参数存在中文时（也就是说输入框中输入中文时），对URL的中文参数进行编码是按照浏览器机制进行编码的。此时编码存在乱码问题。

如图所示：

![image-20220114103519746](/6.png)

**相关文章：**[URL地址中的中文乱码问题的解决 - 五艺 - 博客园 (cnblogs.com)](https://www.cnblogs.com/y896926473/articles/8635406.html)



写完文章之后重新连接Github远程仓库再次上传博客即可更新。



> 参考文章：
>
> [Vuepress+vercel搭建个人博客 | 张同学 (sharesomething.cn)
>
> [[白嫖永久服务器+域名搭建个人博客_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV17Q4y1Y7LF?from=search&seid=13368834160056759923&spm_id_from=333.337.0.0)](https://www.sharesomething.cn/course/blog/blog.html#安装)
>
> [VuePress介绍 - VuePress中文网 (caibaojian.com)](http://caibaojian.com/vuepress/guide/)
>
> [关于URL编码 - 阮一峰的网络日志 (ruanyifeng.com)](http://www.ruanyifeng.com/blog/2010/02/url_encoding.html)