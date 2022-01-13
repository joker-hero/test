---
title: Markdown语法介绍
date: 2022-01-10
tags:
 - Markdown
categories:
 - other
---

 ::: tip

Markdown 是一种可以使用普通文本编辑器编写的标记语言，通过简单的标记语法，它可以使普通文本内容具有一定的格式。

:::

### 一 、编辑器

---

编辑器有很多种类，可以根据自己偏好进行选择，以下为我常用的两种编辑器

1.可以使用VScode编辑器来编辑Mardown，VSCode 支持 MacOS 、Windows、Linux 平台，且包含多种主题。

VSCode 默认认集成了 Markdown 文档编辑插件，原生就支持高亮 Markdown 的语法。

VSCode（全称：Visual Studio Code）是一款由微软开发且跨平台的免费源代码编辑器。

+ **VScode 安装教程：**[https://www.runoob.com/w3cnote/vscode-tutorial.html](https://www.runoob.com/w3cnote/vscode-tutorial.html)
+ **VScode 官网地址：**[https://code.visualstudio.com/](https://code.visualstudio.com/)

2.Typora是一款轻便简洁的Markdown编辑器，支持即时渲染技术，这也是与其他Markdown编辑器最显著的区别。并且是一款十分优秀的免费Markdown编辑器。在这里我们使用Typora来编辑Markdown。

+ **Typora 官网地址：**[https://typora.en.softonic.com/](https://typora.en.softonic.com/)





### 二、语法介绍

#### 标题

Markdown 标题有两种格式。一是使用 = 和 - 标记一级和二级标题，二是使用 # 号标记。

较为常用的是使用“#”来表示1-6级标题，一级标题对应一个 **#** 号，二级标题对应两个 **#** 号，以此类推。

```
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
```

#### 分割线

使用三个或以上的“-”或者“+”或者“*”表示

“---”或者“***”

#### 斜体和粗体

使用“*”和使用“**”分别表示斜体和粗体，例如

```
*斜体文本*

**粗体文本**

***粗斜体文本***
```

#### 链接

链接使用方法如下：

```
[链接名称](链接地址)

或者

<链接地址>
```

例如：

```
这是一个链接 [菜鸟教程](https://www.runoob.com)
```

显示结果：

![image-20220112102829689](E:\vuepress-demo\vuepress-theme-reco-demo-demo-1.x\vuepress-theme-reco-demo-demo-1.x\blogs\image\image-20220112102829689.png)

#### 图片(链接和图片的写法类似，图片仅在超链接前多了一个 "!" ，一般是 [文字描述] (链接))

Markdown 图片语法格式如下：

```
![alt 属性文本](图片地址)

![alt 属性文本](图片地址 "可选标题")
```

+ 开头一个感叹号 !
+ 接着一个方括号，里面放上图片的替代文字
+ 接着一个普通括号，里面放上图片的网址，最后还可以用引号包住并加上选择性的 'title' 属性的文字。

事例：

```
![RUNOOB 图标](http://static.runoob.com/images/runoob-logo.png)

![RUNOOB 图标](http://static.runoob.com/images/runoob-logo.png "RUNOOB")
```

#### 列表

Markdown 支持有序列表和无序列表。

1.无序列表

无序列表使用星号(*****)、加号(**+**)或是减号(**-**)作为列表标记，这些标记后面要添加一个空格，然后再填写内容：

```
* 第一项
* 第二项
* 第三项

+ 第一项
+ 第二项
+ 第三项


- 第一项
- 第二项
- 第三项
```

2.有序列表

有序列表使用数字并加上 **.** 号来表示，如：

```
1. 第一项
2. 第二项
3. 第三项
```

3.嵌套列表

列表嵌套只需在子列表中的选项前面添加四个空格即可：

```
1. 第一项：
    - 第一项嵌套的第一个元素
    - 第一项嵌套的第二个元素
2. 第二项：
    - 第二项嵌套的第一个元素
    - 第二项嵌套的第二个元素
```

#### 区块

Markdown 区块引用是在段落开头使用 **>** 符号 ，然后后面紧跟一个**空格**符号：

```
> 区块引用
> 菜鸟教程
> 学的不仅是技术更是梦想
```

另外区块是可以嵌套的，一个 **>** 符号是最外层，两个 **>** 符号是第一层嵌套，以此类推：

```
> 最外层
> > 第一层嵌套
> > > 第二层嵌套
```

区块中使用列表

```
> 区块中使用列表
> 1. 第一项
> 2. 第二项
> + 第一项
> + 第二项
> + 第三项
```

#### 表格

表格建议使用段落>表格>插入表格来设置。





### 三、VuePress中的默认的扩展语法

***

VuePress内置VuePress 内置了一些比较易用的语法特性，这使得你可以更加容易地书写文章，这里简单列举下支持的语法，具体特性请前往 [VuePress Markdown 扩展语法 (opens new window)](https://v1.vuepress.vuejs.org/zh/guide/markdown.html)查看

- GitHub 风格的表格
- Table of Contents
- Emoji
- 代码块
  - 代码块语法高亮
  - 代码块中的行高亮
  - 显示行号
  - 代码段的导入

你还可以使用 `markdown-it` 插件对语法进行扩展

你甚至可以在 Markdown 中直接使用 Vue 以及 Vue 组件，就像这个主题内置的徽章Badge，更多示例请见 VuePress 官网[在 Markdown 中使用 Vue](https://vuepress.vuejs.org/zh/guide/using-vue.html)

还有一些 VuePress 插件可以提升你的 Markdown 语法，你可以参考[插件的使用](https://vuepress-theme-reco.recoluan.com/views/plugins/#插件怎么用)来添加你自己想要的插件

以下为VuePress拓展语法的使用文档

+ [[vuepress-theme-reco文档](https://vuepress-theme-reco.recoluan.com/)]

