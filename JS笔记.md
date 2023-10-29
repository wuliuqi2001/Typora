# JS笔记

## 互动方式

### 输出

* `document.write()`

### 警告

* `alert()`
* 弹出警告框，输出括号里的内容，并有一个确定按钮

### 确认

* `confirm（str）`
* 弹出窗口，显示str，并有确认和取消按钮
* 点击确认返回ture，点击取消返回false

### 提问

* `prompt(str1，str2)`

* str1：要显示在消息对话框的文本，不可修改

  str2：文本框中的内容，可修改

* 点击确认返回文本框中的内容，点击取消返回null

### 打开新窗口

* `window.open([URL], [窗口名称], [参数字符串])`

* * URL：可选参数，在窗口中显示网页的网址和路径。省略或者值为空，窗口不显示任何文档

  * 窗口名称：可选参数，被打开窗口的名称

    * 由字母、数字和下滑线字符组成

    * "_top"：框架网页中在上部窗口中显示目标网页

      "_self"：在当前窗口显示目标网页

      "_blank"：在新窗口中显示目标网页

    * 相同name的窗口只能创建一个

    * name不能包含空格

  * 参数字符串：可选参数，设置窗口参数，各参数用逗号隔开

    ![image-20230726131536835](D:\Workspace\Typora\image\image-20230726131536835.png)

### 关闭窗口

* `window.close()`：关闭本窗口

  `<窗口对象>.close()`：关闭指定窗口

## DOM操作

### DOM（文档对象模型，Document Object Model）

- 概念：DOM定义访问和处理HTML文档的标准方法。将HTML文档呈现为带有元素、属性和文本的树结构（节点树）。

### 通过ID获取元素

* `document.getElementById("id")`

### innerHTML属性

* 用于获取或替换HTML元素的内容
* `Object.innerHTML`
* 注意：Object是获取的元素对象，如通过document.getElementById("ID")获取的元素

### 改变HTML样式

* `Object.style.property=new style;`

### 显示和隐藏

* `Object.style.display = value`

* value取值：none：隐藏

  ​					block：显示为块级元素

### className属性

* `Object.className = classname`

* 获取元素的class属性

  为网页内某个元素指定一个css样式来改变样式外观

## 变量

### 关键字

![image-20230728223121960](D:\Workspace\Typora\image\image-20230728223121960.png)

### 保留字

![image-20230728223217702](D:\Workspace\Typora\image\image-20230728223217702.png)

### 内置函数

* parseInt("字符串"，进制)：将字符串转换成整型
* 

## 数组

### length属性

* `myarray.length;`
* 注意：JavaScript的length属性可变

## 函数

### 定义函数

* ```js
  function 函数名()
  {
  	函数体;
  }
  ```

### 函数调用

1. 直接写函数名调用

2. HTML文件中调用，例如通过点击按钮后调用

   ```javascript
   <input type="button" value="click it" onclick="add2()">  //按钮，onclick点击事件
   ```

### 带参函数

* ```js
  function 函数名(参数1，参数2)
  {
  	函数体;
  }
  ```

## 事件

* 事件是可以被JavaScript检测到的行为
* ![image-20230805183930186](D:\Workspace\Typora\image\image-20230805183930186.png)

### onclick鼠标单击事件

```js
<input name="button" type="button" value="点击提交" onclick="function()" />
```

## 对象

* JavaScript中所有事物都是对象，每个对象都有**属性**和**方法**

* 属性

  * `objectName.propertyName`

  * 反应对象某些特定的性质的

* 方法

  * `objectName.methodName()`

  * 能够在对象上执行的动作

### Date日期对象

* `var Udate=new Date();` Udata初始值为当前电脑系统时间

* 常用方法![image-20230809123404643](D:\Workspace\Typora\image\image-20230809123404643.png)

* 例：将目前日期时间推迟一小时

  ```js
  <script type="text/javascript">
    var mydate=new Date();
    document.write("当前时间："+mydate+"<br>");
    mydate.setTime(mydate.getTime() + 60 * 60 * 1000);
    document.write("推迟一小时时间：" + mydate);
  </script>
  ```

### String字符串对象

* `stringObject.length`：返回字符串长度
* `stringObject.toUpperCase()`：字符串转化为大写
* `stringObject.toLowerCase()`：字符串转化为小写
* `stringObject.charAt(index)`：返回指定位置的长度为1的字符（空格也算字符）
* `stringObject.indexOf(substring,startpos)`：返回指定字符串值在字符串中首次出现的位置（startpos：可选的整数参数，规定开始检索位置）
* `stringObject.split(separator,limit)`：将字符串分割为字符串数组并返回（separator：指定分割点，limit：可选，分割的次数）
* `stringObject.substring(startPos,stopPos)`：提取介于两个指标中间的字符
* `stringObject.substr(startPos,length)`：提取指定数目的字符串（startPos如果是负数，，指倒着数的位置）

### Math对象

* 属性
  ![image-20230809131605603](D:\Workspace\Typora\image\image-20230809131605603.png)

* 方法

  ![image-20230809131633200](D:\Workspace\Typora\image\image-20230809131633200.png)

### Array数组对象

* 方法

  ![image-20230809131927935](D:\Workspace\Typora\image\image-20230809131927935.png)

* concat()：返回新的数组
* join()：分隔符默认为逗号
* reverse：改变原有数组
* sort：参数可选，但是必须是方法函数

### 浏览器对象

1. **window对象**

   * 是DOM的核心，指当前的浏览器窗口

   * 方法：

     ![image-20230814115143644](D:\Workspace\Typora\image\image-20230814115143644.png)

2. **JavaScript计时器**

   * 一次性计时器、间隔性触发计时器
* 方法：
  
  * `setInterval(代码，交互时间)`：**代码**：要调用的函数或者要执行的代码串。**交互时间**：单位毫秒。**返回值**：一个可以传递给clearInterval()从而取消对代码的周期性执行的值
     * `clearInterval(id_of_setInterrval)`：参数是由setInterval()返回的ID值
  * `setTimeout(代码，延迟时间)`：**代码**：要调用的函数或要执行的代码串。延时时间：执行代码前需等待

## 一些语法

* 一元运算符+可以把数字字符串转换成数值

  ```js
  +"42";  //42
  ```

* 特殊for循环

  ```js
  //1
  for(let value of array){
  	//do something with value
  }
  
  //2
  for(let property in object){
  	//do somrthing with object property
  }
  ```

* 剩余参数

  ```
  function avg(...args){
  	//剩余参数操作符...args代表可以传递任意数量的参数到函数中
  }
  ```










# 速成js

## DOM和BOM

### 获取标签

* 旧的

  `document.getElementById('id名')`

  `document.getElementByTagname('标签名')`

  > 通过tagname获取到的标签列表是伪数组，有索引、长度、但是没有复杂函数

* 新的

  1. `document.querySelectorAll('选择器')`

  2. 单个元素（匹配第一个元素）：`document.querySelector('选择器')`

  3. 前后同级元素`item.previousElementSibling`

     `item.nextElementSibling`

  4. 父元素

     `item.parentNode`

  5. 子元素

     `item.children`

### 标签样式

1. 获取标签
2. 样式处理`block.style.样式 = '内容'`

### 文本处理

* `block.innerHTML = '内容'`

  *内容里可以加标签，然后生成出来 

## ES6

### 变量和常量

* `let`声明变量（局部）
* `const`声明常量

### 模板字符串

*  ![image-20231027162622790](D:\Workspace\Typora\image\image-20231027162622790.png)

  反引号里面用`${ }`来引用外部变量

### 解构赋值

* const

  ```js
  // 数组解构
  const [a, b, c] = [1, 2, 3]
  
  // 对象解构
  const { username, age: userAge, ...other} = {
    username: ' ',
    age: 18,
    gender: 'formale',
    category: 'user'
  }
  
  // age: userAge -> 起别名
  // ...other -> 剩余项匹配这个
  ```

### 数组对象扩展

1. **扩展运算符`...`**

* 数组：![image-20231027164109026](D:\Workspace\Typora\image\image-20231027164109026.png)

* 对象：

  ![image-20231027164339983](D:\Workspace\Typora\image\image-20231027164339983.png)

2. **数组方法**

* 伪数组转换成数组

  `Array.from(伪数组)`

3. **对象方法**

   > 对象是引用类型，正常赋值是无法得到对象副本的

* 浅拷贝`Object.assign()`

   `const objB = Object.assign({}, objA)`

