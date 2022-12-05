# What is Python?

Python is a popular programming language. It was created by Guido van Rossum, and released in 1991.

- web development (server-side),
- software development,
- mathematics,
- system scripting.

### What can Python do?

- Python can be used on a server to create web applications.
- Python can be used alongside software to create workflows.
- Python can connect to database systems. It can also read and modify files.
- Python can be used to handle big data and perform complex mathematics.
- Python can be used for rapid prototyping, or for production-ready software developm

### Why Python?

- Python works on different platforms (Windows, Mac, Linux, Raspberry Pi, etc).
- Python has a simple syntax similar to the English language.
- Python has syntax that allows developers to write programs with fewer lines than some other programming languages.
- Python runs on an interpreter system, meaning that code can be executed as soon as it is written. This means that prototyping can be very quick.
- Python can be treated in a procedural way, an object-oriented way or a functional way.

- 实用性广
    - 
- 优雅
    - 简单
    - 易学
    - 开发效率高

### Good to know

- The most recent major version of Python is Python 3, which we shall be using in this tutorial. However, Python 2, although not being updated with anything other than security updates, is still quite popular.
- In this tutorial Python will be written in a text editor. It is possible to write Python in an Integrated Development Environment, such as Thonny, Pycharm, Netbeans or Eclipse which are particularly useful when managing larger collections of Python files.

### Python Syntax compared to other programming languages

- Python was designed for readability, and has some similarities to the English language with influence from mathematics.
- Python uses new lines to complete a command, as opposed to other programming languages which often use semicolons or parentheses.
- Python relies on indentation, using whitespace, to define scope; such as the scope of loops, functions and classes. Other programming languages often use curly-brackets for this purpose.

# First program

```py
print("hello world")
```



# Python 解释器

Python解释器由编译器和虚拟机构成，编译器将源代码转换成字节码，然后再通过Python虚拟机来逐行执行这些字节码。

**python程序执行过程：**

1、执行 .py 文件，就会启动python解释器

2、编译器将源文件解释成字节码
3、虚拟机将字节码转化成机器语言，与操作系统交互

4、程序运行结束后，将字节码存到pyc文件，便于后续直接执行