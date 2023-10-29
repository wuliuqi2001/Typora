# C#编程语言

## 变量/常量

### 变量

* 数据类型 变量名称

* 不以数字开头的英文字母、数字、下划线的组合
* C#明明编码规范——Camel命名法

### 常量

* `const 数据类型 常量名称=值`
* 必须在声明时初始化，不能被重新赋值
* 有意义、均大写、长度不易长

### 输入输出

* `Console.Writeline()`输出后换行

  `Console.Write()`输出后不换行

* `Console.ReadLine()`返回值String类型

* <img src="D:\Workspace\Typora\image\image-20230625192658776.png" alt="image-20230625192658776" style="zoom:50%;" />

  {0}：占位符

* <img src="D:\Workspace\Typora\image\image-20230625193850498.png" alt="image-20230625193850498" style="zoom:50%;" />

### 方法/函数

* 定义形式

  <img src="D:\Workspace\Typora\image\image-20230625194026967.png" alt="image-20230625194026967" style="zoom:50%;" />

## 流程控制

### 条件语句

*  if和Java相同

* switch对比

  <img src="D:\Workspace\Typora\image\image-20230625194329809.png" alt="image-20230625194329809" style="zoom:50%;" />

  * case中没有其他语句时不需要break

### 数组

* <img src="D:\Workspace\Typora\image\image-20230625194616348.png" alt="image-20230625194616348" style="zoom:50%;" />
* 初始值数目必须和数组长度一样

### 循环语句

* <img src="D:\Workspace\Typora\image\image-20230625194746368.png" alt="image-20230625194746368" style="zoom:50%;" />

* foreach循环

  <img src="D:\Workspace\Typora\image\image-20230625194850583.png" alt="image-20230625194850583" style="zoom:50%;" />

## 封装、继承、多态、抽象类

### 对象：

* 现实世界存在的具体实体，皆有各自的状态和行为

### 类：

* 有相似状态和行为的集合
* 是将不同类型的数据和与这些数据相关的操作封装在一起的集合体

### 类的属性

<img src="D:\Workspace\Typora\image\image-20230625200315858.png" alt="image-20230625200315858" style="zoom:50%;" />

* 自动属性

  <img src="D:\Workspace\Typora\image\image-20230625200429860.png" alt="image-20230625200429860" style="zoom:50%;" />

### 封装

<img src="D:\Workspace\Typora\image\image-20230625200506780.png" alt="image-20230625200506780" style="zoom:50%;" />

<img src="D:\Workspace\Typora\image\image-20230625200657076.png" alt="image-20230625200657076" style="zoom:50%;" />

### 方法

* 表示类和对象的行为
* 定义：参数、返回值、方法体

### 引用类型（引用值改变原值也改变）

<img src="D:\Workspace\Typora\image\image-20230625201102498.png" alt="image-20230625201102498" style="zoom:50%;" />

### 封装

* 隐藏实现细节，公开某种功能作为外界通信的通道

## S.O.I.L.D（面向对象五大原则）

* Single Responsibility Principle（单一功能原则）：对象应该仅具有一种单一功能
* Open Close Principle （开闭原则）：软件体应该是对于扩展开放的，但是对于修改封闭的
* Liskov Substitution Principle（里氏替换原则）：程序中的对象应该是可以在不改变程序正确性的前提下被它的子类所替换的
* Interface Segregation Principle（接口隔离原则）：多个特定客户端接口要好于一个宽泛 用途的接口
* Dependency Inversion Principle（依赖反转原则）：一个方法应该遵从“依赖于抽象而不是 一个实例。依赖注入是该原则的一种实现方式

## 如何学好一门编程语言