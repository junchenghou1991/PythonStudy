#  1 基础语法

+ https://fishc.com.cn/forum-173-1.html
+ https://www.bilibili.com/video/BV1xs411Q799?p=3&spm_id_from=pageDriver&vd_source=fe12b7e37154d592ac06fb261323de5e
+ https://app.codingrooms.com/management/courses/6387/classes/8480/assignments

## 1.0标识符

- 第一个字符必须是字母表中字母或下划线 **_** 。
- 标识符的其他的部分由字母、数字和下划线组成。
- 标识符对大小写敏感。
- 在 Python 3 中，可以用中文作为变量名，非 ASCII 标识符也是允许的了。

## 1.1 字面量

- 含义： 字面量：在代码中， 被**写下来**的固定的值， 我们叫做**字面量**

- 常见类型： string int float

- 如何完成输出 ， 使用print

a. 使用print 语句可以输出字面量

```py
print("hello world")
print(111)
print(13.14)

```

---



## 1.2注释

1. 注释的作用
    1. 负责对代码解释说明， 不会被执行， 让人看懂我们写的代码
2. 如何使用注释
    1. 单行注释: # 使用＃号中间留一个空格 隔开
    2. 多行注释：三个```号包裹起来多行注释
    3. 多行注释可以用多个 **#** 号，还有 **'''** 和 **"""**：

```py
""" 
	我是一个多行注释
    我能做很多事情
    我喜欢一个人在深夜学coding
"""

print(3.14159265)
# 这是一个pi

#!/usr/bin/python3
 
# 第一个注释
# 第二个注释
 
'''
第三注释
第四注释
'''
 
"""
第五注释
第六注释
"""
print ("Hello, Python!")
```

---



## 1.3变量

### 1.3.0什么是变量

变量 ：在程序运行时候， 能存储计算结果或能表示值的抽象概念；

接单来说就是一个用来记录数据的盒子



### 1.3.1syntax

变量名称   =    变量的值

- 每一个变量都有自己的名称： 称之为变量名，也就是变量本身
- =： 赋值， 把右边的值给左边
- 每一个变量都有自己的值

```py
money = 50
print(money)
print("i still have", money, "dollars in my wallet")
# i still have 50 dollars in my wallet

money = money -10;
money -=10;

age = 31
print(age)
# 31
```

### 1.3.3 变量特征

变量的值可以改变

### 1.3.4如何输出多分内容

```py
print(内容1， 内容2， 内容3);
```



### 1.3.5练习

```py
money = 50
print("我的初始资金", money)
money -= 10
print("买完雪糕后我还剩下", money)
money -= 5
print("买完可乐后还剩下", money)

```



## 1.4数据类型

| 类型           | 描述                                                       | 说明                                                         |
| -------------- | ---------------------------------------------------------- | ------------------------------------------------------------ |
| 数字Number     | 整数int<br />浮点数float<br />复数complex<br />布尔boolean | 整数10，-10<br />浮点数13.14，13。543<br />复数complex: 4+3j 以j结尾表示复数<br />真假boolean  true1 false0 |
| 字符窜String   | 描述文本的一种数据类型                                     | 字符窜由任意数量字符组成                                     |
| 列表List       | 有序可变序列                                               | puyhon 用的最多的一种数据类型， 可有序记录一堆数据           |
| 元组Tuple      | 有序不可变序列                                             | 可记录一对不可变的python数据集合                             |
| 集合set        | 无序不重复集合                                             | 可无序记录一对不重复的python 数据集合                        |
| 字典dictionary | 无序KEY-VALUE                                              | 可记录一对key-value 类型的python数据集合                     |

## 

### 1.4.0查看数据类型 

- 使用type

```py
print(type(14))
print(type("Juncheng Hou"))
# <class 'int'>
# <class 'str'>

```

- 我们可以用变量去接收 type 的值
    - 注意type 其实是一个class

```py
string_type = type("junchenghou")
print(string_type) #<class 'str'>
print(type(string_type)) #<class 'type'>
```

- 我们可以用变量存储， 然后用type来查看数据类型。  本质上变量没有类型， 但是变量存储的数据有类型

```py
print(type("黑马程序员"))

string_type1 = "黑马程序员"
print(type(string_type1))
```



### 1.4.1字符窜  string

- 文本，由任意数量字符，中文英文数字符号组成叫做字符窜
- 用双引号包起来

```py
print("I am a String")
```



## 1.5数据类型转换

在特定的场景下， 是可以相互转换的， 如字符窜转数字， 数字转字符窜等。

### 1.5.1 为什么要转换类型？

数据类型转换会是我们经常用到的功能

- 从文件中读取数字， 默认是字符窜， 我们需要转换成数字类型
- 后序学习的input() 默认结果是字符窜， 若需要数字也需要转换
- 将数字转换成字符窜用以书写到外部系统

| 语句       | 说明                   |
| ---------- | ---------------------- |
| int(x)     | 将x转换为一个整数      |
| float（x） | 将x 转换为一个浮点数   |
| str（x）   | 将对象x 转换为字符窜啊 |

字符窜转换成整数的时候， 必须是数字。 不然的话会报错

例子

```py
number_string = str(134) # 转换成string
print(type(number_string)) # string

num = int("123") # 转换成 num
print(num)

num2 = int("junchenghou")
print(num2)
# 报错

num3 = float("13.12")
# 转换成 小数

num3 = int(12.34)
print(num3)
# 12
# 小数->整数
```

### 1.5.2总结

1. 浮点转换小数 损失精度
2. 任何类型 都可以转换成字符窜
3. 字符窜可以随意转换成数字？ 错！！！！ 只有数字才可以

---



## 1.6标识符

标识符是给诸如类，函数，变量等实体的名称。它有助于将一个实体与另一个实体区分开。

1. 标识符可以是小写字母**（a 至 z）**或大写字母**（A 至 Z）**或数字**（0 至 9）**或下划线(_)的组合。

```py
myClass，
var_1，var_name_1,
print_this_to_screen 
#都是有效的。
```



Python 是 **区分大小写** 的语言。这意味着 Variable 和 variable 是两个不同的变量。同时，也建议大家，在实际编程中，始终命名有意义的标识符。



### 1.6.1变量的命名规范

python 中需要用*标识符* 给变量命名 ：其实标识符就是用于给程序中变量、类、方法命名的符号（简单来说，标识符就是合法的名字）。

Python 语言的标识符必须以字母、下画线（*）开头，后面可以跟任意数目的字母、数字和下画线（*）。此处的字母并不局限于 26 个英文字母，可以包含中文字符、日文字符等。

1.变量名称由数字、字母(包括大写字母和小写字母)、下划线组成。

2.变量名不能以数字开头  1variable 是无效的，但 variable1 是有效的。

3.变量名不能用python关键字，但可以包含关键字

4.变量名不能用python函数，否则函数将不能正常使用。如：print

5.变量命名严格区分大小写

6.我们不能使用像**！****。**，**@**，**#**，**$**，**％**等这样的特殊符号。

7.不能有空格

```py
abc_xyz：合法。
HelloWorld：合法。
abc：合法。
xyz #abc：不合法，标识符中不允许出现“#”号。
abc1：合法。
1abc：不合法，标识符不允许数字开头。
```

## python保留字

保留字即关键字，我们不能把它们用作任何标识符名称。Python 的标准库提供了一个 keyword 模块，可以输出当前版本的所有关键字：



```py
>>> import keyword
>>> keyword.kwlist
['False', 'None', 'True', 'and', 'as', 'assert', 'break', '
```



## 1.6.2总结

- 见名知意
- 下划线命名法
- 全部英文小写

---



## 1.7 关键字

### Python关键字

关键字是Python中的保留字。

我们不能将关键字用作 [变量名](https://www.cainiaojc.com/python/python-variables-datatypes.html)，[函数](https://www.cainiaojc.com/python/python-function.html)名或任何其他标识符。它们用于定义Python语言的语法和结构。

在Python中，关键字区分大小写。

Python 3.7中有 33 个关键字。该数字在一段时间内可能会略有变化。

所有关键字必须是小写的，其中 True，False 和 None 除外。下面列出了所有关键字。

| False  | await    | else    | import   | pass   |
| ------ | -------- | ------- | -------- | ------ |
| None   | break    | except  | in       | raise  |
| True   | class    | finally | is       | return |
| and    | continue | for     | lambda   | try    |
| as     | def      | from    | nonlocal | while  |
| assert | del      | global  | not      | with   |
| async  | elif     | if      | or       | yield  |



## 1.8运算符

### 1.8.1 算数运算符

1. division always returns float

| 运算符 | name                    |
| ------ | ----------------------- |
| +      | 加 addition             |
| -      | 减 subtraction          |
| *      | 乘 multiplication       |
| /      | 除 division             |
| //     | 取整除 integer division |
| %      | 余数 modulo             |
| **     | 指数 exponentiation     |

例子

```py
# 运算符
print("1 + 1 = ", 1 + 1)  # 2
print("2 - 1 = ", 2 - 1)  # 1
print("1 * 2 = ", 1 * 2)  # 2
print("4 / 3 = ", 4 / 3)  # 1.3333333
print("4 // 3 = ", 4 // 3)  # 1
print("5 % 3 = ", 5 % 3)  # 2
print("3 ** 3 = ", 3 ** 3)  # 27
```



### 1.8.2赋值运算符

在Python中使用赋值运算符为变量赋值。

a = 5是一个简单的赋值运算符，它将右边的值5分配给左边的变量a。

Python中有许多类似的复合运算符，a += 5它们会添加到变量中，然后再分配给它们。等同于a = a + 5。

| 操作符 | 示例     | 等同       |
| :----- | :------- | :--------- |
| =      | x = 5    | x = 5      |
| +=     | x + = 5  | x = x + 5  |
| -=     | x-= 5    | x = x-5    |
| *=     | x * = 5  | x = x * 5  |
| /=     | x / = 5  | x = x / 5  |
| %=     | x％= 5   | x = x％5   |
| //=    | x // = 5 | x = x // 5 |
| **=    | x ** = 5 | x = x ** 5 |
| &=     | x＆= 5   | x = x＆5   |
| \|=    | x \| = 5 | x = x \| 5 |
| ^=     | x ^ = 5  | x = x ^ 5  |
| >>=    | x >> = 5 | x = x >> 5 |
| <<=    | x << = 5 | x = x << 5 |



### 1.8.3比较运算符

比较运算符用于比较值。它返回True或False根据条件返回。

| 操作符 | 含义                                          | 例     |
| :----- | :-------------------------------------------- | :----- |
| >      | 大于-如果左操作数大于右操作数，则为True       | x> y   |
| <      | 小于-如果左操作数小于右操作数，则为True       | x <y   |
| ==     | 等于-如果两个操作数相等，则为True             | x == y |
| !=     | 不等于-如果操作数不相等则为True               | x！= y |
| >=     | 大于或等于-如果左操作数大于或等于右，则为True | x> = y |
| <=     | 小于或等于-如果左操作数小于或等于右，则为True | x <= y |

#### 示例2：Python中的比较运算符

```py
x = 10
y = 12

# 输出: x > y 是 False
print('x > y 是 ',x>y)

# 输出: x < y 是 True
print('x < y 是 ',x<y)

# 输出: x == y 是 False
print('x == y 是 ',x==y)

# 输出: x != y 是 True
print('x != y 是 ',x!=y)

# 输出: x >= y 是 False
print('x >= y 是 ',x>=y)

# 输出: x <= y 是 True
print('x <= y 是 ',x<=y)
```



### 1.8.4逻辑运算符

逻辑运算符是and，or，not运营商。

| 操作符 | 含义                                            | 例    |
| :----- | :---------------------------------------------- | :---- |
| and    | 如果两个操作数都为真，则为真                    | x和y  |
| or     | 如果任何一个操作数为真，则为真                  | x或y  |
| not    | 如果操作数为false，则为True（对操作数进行补充） | 不是x |

#### 示例3：Python中的逻辑运算符

示例

```
x = True
y = False

print('x and y 是 ',x and y)

print('x or y 是 ',x or y)

print('not x 是 ',not x)
```

**输出结果**

```
x and y 是 False
x or y 是 True
not x 是 False
```





### 1.8.5位运算符

按位运算符作用于操作数，就好像它们是二进制数字的字符串一样。它们一点一点地运行，因此得名。

例如，2是10二进制，7是111。

**在下表中：**令x= 10（0000 1010二进制）和y= 4（0000 0100二进制）

| 操作符 | 含义     | 例                       |
| :----- | :------- | :----------------------- |
| &      | 按位与   | x＆y = 0（0000 0000）    |
| \|     | 按位或   | x \| y = 14（0000 1110） |
| ~      | 按位非   | 〜x = -11（1111 0101）   |
| ^      | 按位异或 | x ^ y = 14（0000 1110）  |
| >>     | 按位右移 | x >> 2 = 2（0000 0010）  |
| <<     | 按位左移 | x << 2 = 40（0010 1000） |





### 1.8.6特殊运算符

Python语言提供了一些特殊类型的运算符，例如身份运算符或成员资格运算符。下面通过示例对其进行描述。

#### **1.8.6.1身份运算符**

is和is not是Python中的身份运算符。 它们用于检查两个值（或变量）是否位于内存的同一部分。 两个相等的变量并不意味着它们是相同的。

| 操作符 | 含义                                       | 例      |
| :----- | :----------------------------------------- | :------ |
| is     | 如果操作数相同，则为真（引用同一对象）     | x为真   |
| is not | 如果操作数不相同，则为真（不引用同一对象） | x不是真 |

##### 示例4：Python中的身份运算符

示例

```py
x1 = 5
y1 = 5
x2 = 'Hello'
y2 = 'Hello'
x3 = [1,2,3]
y3 = [1,2,3]

# 输出: False
print(x1 is not y1)

# 输出: True
print(x2 is y2)

# 输出: False
print(x3 is y3)
```

#### 1.8.6.2成员运算符

in和not in是Python中的成员操作符。它们用于测试在序列（[字符串](https://www.cainiaojc.com/python/python-string.html)，[列表](https://www.cainiaojc.com/python/python-list.html)，[元组](https://www.cainiaojc.com/python/python-tuple.html)，[集合](https://www.cainiaojc.com/python/python-set.html)和[字典](https://www.cainiaojc.com/python/python-dictionary.html)）中是否找到值或变量。

在字典中，我们只能测试键的存在，而不是值。

| 操作员 | 含义                              | 例         |
| :----- | :-------------------------------- | :--------- |
| in     | 如果在序列中找到值/变量，则为真   | 5 in x     |
| not in | 如果在序列中未找到值/变量，则为真 | 5 not in x |



##### 示例#5：Python中的成员资格运算符

示例

```
x = 'Hello world'
y = {1:'a',2:'b'}

# 输出: True
print('H' in x)

# 输出: True
print('hello' not in x)

# 输出: True
print(1 in y)

# 输出: False
print('a' in y)
```



## 1.8 行与缩进

python最具特色的就是使用缩进来表示代码块，不需要使用大括号 **{}** 。

缩进的空格数是可变的，但是同一个代码块的语句必须包含相同的缩进空格数。实例如下：

```py
if True:
    print ("True")
else:
    print ("False")
```

以下代码最后一行语句缩进数的空格数不一致，会导致运行错误：

### 实例

```py
**if** True:
  **print** ("Answer")
  **print** ("True")
**else**:
  **print** ("Answer")
 **print** ("False")   # 缩进不一致，会导致运行错误
    
    '''
     File "test.py", line 6
    print ("False")    # 缩进不一致，会导致运行错误
                                      ^
IndentationError: unindent does not match any outer indentation level
    '''
```

以上程序由于缩进不一致，执行后会出现类似以下错误：

#### Python Indentation

Indentation refers to the spaces at the beginning of a code line.

Where in other programming languages the indentation in code is for readability only, the indentation in Python is very important.

Python uses indentation to indicate a block of code.

## 多行语句

Python 通常是一行写完一条语句，但如果语句很长，我们可以使用反斜杠 **\** 来实现多行语句，例如：

```
total = item_one + \
        item_two + \
        item_three
```

在 [], {}, 或 () 中的多行语句，不需要使用反斜杠 **\**，例如：

```
total = ['item_one', 'item_two', 'item_three',
        'item_four', 'item_five']
```



## 2 课后题

Python是脚本语言



> 脚本语言(Scripting language)是电脑编程语言，因此也能让开发者藉以编写出让电脑听命行事的程序。以简单的方式快速完成某些复杂的事情通常是创造脚本语言的重要原则，基于这项原则，使得脚本语言通常比 C语言、C++语言 或 Java 之类的系统编程语言要简单容易。
>
> 也让脚本语言另有一些属于脚本语言的特性：
>
> - 语法和结构通常比较简单
> - 学习和使用通常比较简单
> - 通常以容易修改程序的“解释”作为运行方式，而不需要“编译”
> - 程序的开发产能优于运行性能
>
> 一个脚本可以使得本来要用键盘进行的相互式操作自动化。一个Shell脚本主要由原本需要在命令行输入的命令组成，或在一个文本编辑器中，用户可以使用脚本来把一些常用的操作组合成一组串行。主要用来书写这种脚本的语言叫做脚本语言。很多脚本语言实际上已经超过简单的用户命令串行的指令，还可以编写更复杂的程序。


**1. IDLE 是什么？**

IDLE是一个Python Shell，shell的意思就是“外壳”，基本上来说，就是一个通过键入文本与程序交互的途径！像我们Windows那个cmd窗口，像Linux那个黑乎乎的命令窗口，他们都是shell，利用他们，我们就可以给操作系统下达命令。同样的，我们可以利用IDLE这个shell与Python进行互动。


**2. print() 的作用是什么？**

print() 会在输出窗口中显示一些文本（在这一讲中，输出窗口就是IDLE shell窗口）。


**3. Python 中表示乘法的符号是什么？**

Python中的乘号是*（星号）。


**4. 为什么 >>>print('I love fishc.com ' \* 5) 可以正常执行，但 >>>print('I love fishc.com ' + 5) 却报错？**

在 Python 中不能把两个完全不同的东西加在一起，比如说数字和文本，正是这个原因，>>>print('I love fishc.com ' + 5) 才会报错。

**5. 如果我需要在一个字符串中嵌入一个双引号，正确的做法是？**

你有两个选择：可以利用反斜杠（\）对双引号转义：\"，或者用单引号引起这个字符串。例如：' I l"o"ve fishc.com '。



### pratice

```py
print(365 * 24 * 60 * 60)

print('----- HAHAHAHAHAHA -----')
temp = input("Lets guess a number ")
guess = int(temp)
if guess == 8:
    print("wow you are genius")
    print(" I will give you a price")
else:
    print("haha good try")
    print("game is over")

```

