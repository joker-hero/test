---
title: 环境配置
date: 2022-01-15
tags:
 - 环境配置
categories:
 - 基于单目视觉的车辆测距
---



## 环境配置

### 一、Python 3.6.3

Python是一种解释型、面向对象、动态数据类型的高级程序设计语言。

Python为我们提供了非常完善的基础代码库，覆盖了网络、文件、GUI、数据库、文本等大量内容，被形象地称作“内置电池（batteries included）”。用Python开发，许多功能不必从零编写，直接使用现成的即可。

除了内置的库外，Python还有大量的第三方库，也就是别人开发的，供你直接使用的东西。当然，如果你开发的代码通过很好的封装，也可以作为第三方库给别人使用。

### 二、OpenCV 3.4.1.15

是一个基于BSD许可（开源）发行的跨平台计算机视觉库，可以运行在Linux、Windows、Android和Mac OS操作系统上。它轻量级而且高效——由一系列 C 函数和少量 C++ 类构成，同时提供了Python、Ruby、MATLAB等语言的接口，实现了图像处理和计算机视觉方面的很多通用算法。

OpenCV用C++语言编写，它的主要接口也是C++语言，但是依然保留了大量的C语言接口。该库也有大量的Python、Java and MATLAB/OCTAVE（版本2.5）的接口。这些语言的API接口函数可以通过在线文档获得。如今也提供对于C#、Ch、Ruby,GO的支持。

所有新的开发和算法都是用C++接口。一个使用CUDA的GPU接口也于2010年9月开始实现。

### 三、Anaconda

Anaconda指的是一个开源的python发行版本，其包含了conda、Python等180多个科学包及其依赖项。 因为包含了大量的科学包，Anaconda 的下载文件比较大（约 531 MB），如果只需要某些包，或者需要节省带宽或[存储空间](https://baike.baidu.com/item/存储空间/10657950)，也可以使用**Miniconda**这个较小的发行版（仅包含conda和 Python）。

Anaconda具有如下特点：

- 开源
- 安装过程简单
- 高性能使用Python和R语言
- 免费的社区支持

其特点的实现主要基于Anaconda拥有的：

- conda包
- 环境管理器
- 1,000+开源库

Anaconda集成了大多科学包及其依赖项，安装较为简单，在此使用Anaconda进行开发。

+ **Anaconda下载地址：**https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/

下载安装完之后点击win菜单，打开[Anaconda](https://so.csdn.net/so/search?q=Anaconda) Prompt，这个窗口和cmd窗口一样的，用命令“pip list”可以查看已安装的包。

![image-20220112164147396](/a.png)

<img src="/b.png" alt="image-20220112164637863" style="zoom:50%;" />

使用Anaconda安装opencv：

第一步：切换到Scripts路径

<img src="/c.png" alt="image-20220112165102112" style="zoom:50%;" />

第二步：安装opencv-python，这里推荐安装3.4.1.15版本，因为在3.4.2版本之后部分算法例如特征提选等已经申请了专利。所以使用3.4.1.15版本可以更好的使用opencv。

安装命令（[文档可参考该链接](https://www.jianshu.com/p/60339b9e0412)）：

+ pip install -i https://pypi.tuna.tsinghua.edu.cn/simple opencv-python==3.4.1.15

+ pip install -i https://pypi.tuna.tsinghua.edu.cn/simple opencv-contrib-python==3.4.1.15

查看版本号：

<img src="/d.png" alt="image-20220112170119541" style="zoom:50%;" />

这样就把基本的环境配置安装好了

