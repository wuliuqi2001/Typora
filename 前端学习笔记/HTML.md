# 一、Web标准

web标准主要包括**结构（Structure）**、**表现（Presentation）**和**行为（Behavior）**三个方面。

* **结构标准**：对网页元素进行整理和分类，主要包括XML和XHTML两部分。
* **样式标准**：表现用于设置网页元素的版式、颜色、大小等外观样式，主要是指CSS。
* **行为标准**：指网页模型的定义及交互的编写，主要包括DOM和ECMAScript两个部分。

# 二、HTML简介

HTML：Hyper Text Markup Language，超文本标签语言

## HTML语法骨架格式：

```html
<html>
    <head>
        <title></title>
    </head>
    <body>
        ...
    </body>
</html>
```

* html：根标签
* head：用于存放title，meta，base，style，script，link
* title：标题
* body：主体部分，用于存放html标签，例如p，h，a，b，u，i，s，em，del，ins，strong，img

## 标签分类

* 双标签：有开始有结束
* 单标签：eg：结束标签`<br />`

## 标签关系

* 嵌套关系
* 并列关系

## 字符集

`<meta charset="UTF-8">`


Utf-8包含全世界所有国家需要用到的字符

* Gb2312 简单中文 包括6763个汉字

* BIG5 繁体中文 港澳台通用

* GBK 包含全部中文（简繁两类）

# 三、HTML标签

## 排版标签

### 标题标签

* h1~h6

  `<hn>...</hn>`

### 段落标签

`<p>...</p>`

### 水平线标签

`<hr />`

### 换行标签

`<br />`

### div、span标签

* div：分区。网页由多个div组成

  `<div>这是盒子</div>`
  
* span：跨度；跨距；范围

  `<span>这是另一个盒子</span>`

## 文本格式化标签

### 加粗

* `<strong>文本</strong>`
* `<b>文本</b>`

### 倾斜

* `<em>文本</em>`
* `<i>文本</i>`

### 删除线

* `<del>文本</del>`
* `<s>文本</s>`

### 下划线

* `<ins>文本</ins>`
* `<u>文本</u>`

## 标签属性

`<标签名 属性名1="属性值1" 属性名2="属性值2" …> 内容</标签名>`

## 图像标签

`<img src="图像URL" .../>`

图片属性：

* src：图片地址（URL）
* alt：图片不能显示时的替换文本（文本）
* title：鼠标悬停时显示的内容（文本）
* width：图像宽度（像素）
* height：图像高度（像素）
* border：图像边框宽度（数字）

## 链接标签

`<a href="跳转目标" target="目标窗口的弹出方式">文字或图像</a>`

链接属性：

* Href：用于指定链接目标的URL地址，为标签应用href属性时，它就具有了超链接的功能

* target：用于指定链接页面打开的方式，取值有self（默认值）和blank（在新窗口中打开）两种

  `<a target="_blank">...`

注意：

1. 外部链接需要添加 *http://*     *。*
2. 内部链接直接链接内部页面名称即可。
3. 没有确定链接目标时，href="#",表示该链接暂时为一个空链接。
4. 网页中各种元素都可以添加超链接。

## 锚点定位

* 跳转标签

  `<a href="#id">文本或图片</a>`

* 跳转到这里

  `<h id="id">...</h>`

## base标签

规定所有超链接的基础打开方式

`<base target="_blank"/>`

## 特殊字符标签

![image-20221210220146567](C:\Users\仵六七\AppData\Roaming\Typora\typora-user-images\image-20221210220146567.png)

## 注释标签

`<!- -注释部分- - >`

## 路径

* 相对路径

  1. 图像文件和HTML文件位于同一文件夹：输入文件名称即可

     如`<img src="logo.gif"/>`

  2. 图像文件位于HTML文件的下一级文件夹：文件夹名和文件名之间用“/”隔开

     如`<img src="img/img01/logo.gif"/>`

  3. 图像文件位于HTML的上一级文件夹：文件名之前加上"../"，如果是上两级，加上"../../"

     如`<img src="../logo.gif"/>`

* 绝对路径

  全写出来，**但是**换电脑就不能用了

## 列表标签

* 无序列表ul

  ```html
  <ul>
  	<li>列表项1</li>
  	<li>列表项2</li>
  </ul>
  ```

* 有序列表ol

  ```html
  <ol>
  	<li>列表项1</li>
  	<li>列表项2</li>
  </ol>
  ```

* 自定义列表

  ```html
  <dl>
  	<dt>名词1</dt>
  	<dd>名词解释1</dd>
  	<dd>名词解释2</dd>
  	<dt>名词2</dt>
  	<dd>名词解释3</dd>
  	<dd>名词解释4</dd>
  </dl>
  ```

# 四、表格

## 创建表格

* tr：行

* td：列

* tr里只能放td

  ```html
  <table width="…" height="…" border="…">
  	<tr>
  		<td>单元格内文字</td>
  	        …
  	</tr>
  	  …
  </table>
  ```

## 表格属性

* border：设置表格边框（像素值，默认为0）
* cellspacing：单元格与单元格边框之间的空白间距（像素值，默认为2）
* cellpadding：设置单元格内容与单元格边框之间的空白间距（像素值，默认为1）
* width：表格宽度（像素值）
* height：表格高度（像素值）
* align：设置表格在网页中的水平对齐方式（left、center、right） 

## 表头标签

直接用`<th>...</th>`替换`<td>...</td>`

## 表格结构

* 表头部分

  `<thead>...</thead>`

* 主体部分

  `<tbody>...</tbody>`

## 表格标题

`<caption>...</caption>`

写在table标签里面

## 合并单元格

* 跨行合并rowspan

  `<td rowspan"数字">...</td>`

  合并几行，后面被合并的td标签都要删掉

* 跨列合并colspan

  `<td colspan="数字">...</td>`

  合并几列，后面被合并的td标签都要删掉

## 表单标签

### 完整表单组成成分

* 表单控件（表单元素）

  包含具体表单功能项，如单行文本输入框、密码输入框、复选框、提交按钮。重置按钮等

* 提示信息

  说明性文字，提示用户进行填写和操作

* 表单域

## input控件

`<input/>`

### 属性

* type
  * text：单行文本输入框
  * password：密码输入框
  * radio：单选按钮
  * checkbox：复选框
  * button：普通按钮
  * submit：提交按钮
  * reset：重置按钮
  * image：图像形式的提交按钮
  * file：文件域
* type（HTML5新增）
  * email：输入邮箱格式
  * tel：输入手机号码格式
  * url：输入url格式
  * number：输入数字格式
  * search：搜索框（后面带叉号，可一键删除
  * range：自由拖动滑块
  * time：小时分钟
  * data：年月日
  * datatime：时间
  * month：月年
  * week：星期 年
* name：控件名称，name相同为一组（用户自定义
* value：默认文本值（用户自定义
* size：控件在页面中的显示宽度（正整数
* checked：默认被选中（checked
* maxlength：控件允许输入的最多字符数（正整数
* placeholder（新）：占位符，输入时消失
* autofocus（新）：自动获得焦点（刷新页面光标自动进入输入框
* multiple（新）：允许多文件上传
* autocomplete（新）：自动记录
  * 有on和off两种属性值
  * 需要提交后才可自动记录
  * 需要设置name用来保存记录类型
* required（新）：必填按钮
* accesskey（新）：定义快捷键，用户使用时需要加上Alt键

## lable标签

input元素定义标注（标签）

用于绑定一个表单元素，当点击lable标签的时候，被绑定的表单元素就会获得输入焦点

* 单个表单（直接包裹）

  `<lable>...</lable>`

* 多个表单（用for和id捆绑想聚焦的表单）

  `<lable for="two">...<input type="text" id="two"/></lable>`

## textarea控件

* 留言框之类

  `<textarea>...</textarea>`

## select控件

```html
<select>
	<option>选项1</option>
	<option>选项2</option>
	         ……
	<option>选项n</option>
</select>
```

* 做下拉菜单
* select里必须至少包含一个option
* 默认选中属性 `selected="selected"`

## 表单域

```html
	<form action="url地址" method="提交方式" name="表单名称">
	       …
	</form>
```

* method：post、get
