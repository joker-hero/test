---

title: Opencv
date: 2022-01-15
tags:
 - 环境配置
categories:
 - 基于单目视觉的车辆测距
---

# 图像处理基础

![image-20220113215124652](/e.png)

### 图像

图像是一个由像素组成的二维矩阵，每个元素是一个RGB值。

二维矩阵的每一个像素点又0~255取值，表示该点的一个亮点。

图像这是这些亮度所构成的结果。

RGB是从颜色发光的原理来设计定的，通俗点说它的颜色混合方式就好像有红、绿、蓝三盏灯，当它们的光相互叠合的时候，色彩相混，而亮度却等于三者亮度之总和，越混合亮度越高，即加法混合。

表示RGB的二维矩阵的长和宽则表示图像的长和宽。例如图像的R，G，B都是500*400的矩阵，则图像的整体维度也是500 * 400的图像，既表示为[500,400,3] 。





### 图像的数据读取

```python
//导入cv2,plt,numpy模块
import cv2
import matplotlib.pyplot as plt
import numpy as np

//读取图像
img=cv2.imread('cat.jpg')
//输出图像
print(img)
```

在此我们导入一张猫的图像。

![image-20220113230217625](/f.png)

```
输出结果：
[[[ 50  57  82]
  [ 45  55  79]
  [ 51  61  85]
  ...
  [ 10  12  12]
  [ 12  14  14]
  [ 14  17  15]]

 [[ 31  38  63]
  [ 30  37  62]
  [ 32  42  66]
  ...
  [ 15  14  16]
  [ 16  16  16]
  [ 16  16  16]]

 [[ 29  36  56]
  [ 29  36  56]
  [ 27  35  58]
  ...
  [ 18  17  19]
  [ 16  16  16]
  [ 17  15  15]]

 ...

 [[217 206 202]
  [200 191 188]
  [187 177 177]
  ...
  [ 91  95  96]
  [106 111 110]
  [119 124 123]]

 [[208 199 195]
  [201 192 189]
  [193 185 185]
  ...
  [105 110 109]
  [117 122 121]
  [125 130 129]]

 [[215 207 200]
  [212 204 197]
  [208 199 195]
  ...
  [110 114 115]
  [123 129 128]
  [130 136 135]]]
```
