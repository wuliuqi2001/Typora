# 一、盒子模型

## 简介

* 浏览器在渲染网页时，会将网页中的元素看成一个个的矩形区域，我们形象的称之为盒子
* 每个标签都可以看做一个盒子
* 每个盒子由：<font  color="bro">内容区域（content）、内边距区域（padding）、边框区域（border）、外边距区域（margin）</font>构成，这就是盒子模型

## 内容的宽度和高度

* `width`和`height`默认设置盒子内容区域的大小

## 边框border

### 全包型

* `border`

* 可以当复合属性，单个取值的连写，取值之间用空格隔开

  例如：`border：10px solid red；`（先后顺序无所谓）

* 线型：实线（solid）、虚线（dashed）、点线（dotted）

### 单方向设置

* `border-方位名词`
* top/bottom/left/right

### 单个属性

* ![2022-12-15 21-24-34](D:\qycache\picture\2022-12-15 21-24-34.jpg)

## 内边距padding

* `padding`

* 可以当复合属性，

  例如：
  
  `padding: 10px 20px；`（上下，左右）
  
  `padding：10px 20px 30px；`（上，左右，下）
  
  `padding：10px 20px 30px 40px；`（上，右，下，左）

### 单方向设置

* `padding-方位名词`
* top/bottom/left/right

**💡利用内边距可以解决固定宽高盒子的字数限制问题**

## css3盒模型

* 属性名：`box-sizing`
* 属性值：boder-box
* 作用：自动内减，不用手动减少内容

## margin外边距

* `margin`

* 可以当复合属性

  `margin: 10px 20px；`（上下，左右）

  `margin：10px 20px 30px；`（上，左右，下）

  `margin：10px 20px 30px 40px；`（上，右，下，左）

### 单方向设置

* `margin-方位名词`

* 应用：

  使当前盒子向右（left）或者向下（top）移动

  使右边的盒子向右（right）移动或下边的盒子向下（bottom）移动

### margin合并现象

* 垂直布局的块级元素，上下margin会合并（取两者最大）
* 解决方法：只给一个盒子设置margin

### margin塌陷现象

* 互相嵌套的块级元素子元素的margin-top会作用在父元素上，导致父元素一起往下移动
* 解决方法：
  1. 给父元素设置border-top或者padding-top（分割父子元素的margin-top）
  2. 给父元素设置overflow：hidden
  3. 转换成行内块元素
  4. 设置浮动

## 行内margin和padding无效

* 行内元素设置margin和padding，水平方向有效，竖直方向无效。
