# 1. 环境搭建

## 1.1 Anaconda 环境配置

第一步，Anaconda 官网下载最新版本

[链接到 Anaconda](https://www.anaconda.com/)

第二步，找到适合电脑操作系统版本的 Anaconda

[对应操作系统的 Anaconda版本选择](https://www.anaconda.com/distribution/#download-section)

第三步，下载安装，选择默认选项即可

第四步，配置环境变量方法

[环境变量配置](https://blog.csdn.net/baidu_32542573/article/details/79361456)



## 1.2 解释器



# 2. Python 初体验

## 1)  print and input

print()是函数，表示将小括号内的数据打印（显示）到屏幕，可以输出 string, number, variable 等值
例：
print("Hello world!")
print(123)

a = 100
print(a)

input() 是输入函数，接受用户的输入，用户可以输入 string, number
例：
a = input('请输入你的名字：')

# 3. python 基础讲解

## 1) python 变量特征 + 命名规则

### python 变量特征

变量可以指定不同的数据类型，可以存储 number，string, python 数据容器（列表、元组、集合、字典）
a = 120
b = "this is an example."
c = [1, 2, 3]
d = (1, 2, 3)
e = {12, 23, 34}
f = {'name':'陈国艺', 'city':'广州'}

### python 变量命名规则
python 使用标识符给变量命名
规则：
a. 第一个字符必须是字母表中字母或下划线 _ 
b. 标识符的其他的部分由字母、数字和下划线组成
c. 标识符对大小写敏感，严格区分大小写。ab 与 Ab 是不一样的

在 Python 3 中，允许非 ASCII 标识符命名变量，如中文、日文字符

## 2) 注释方法

三种注释方法：

①  # 这是一条单行注释，程序执行过程中会被忽视

② '''这是多行注释，

程序执行过程中

会被忽视'''

③ """这是多行注释，

程序执行过程中

会被忽视"""

## 3) python中“：”的作用

① 出现在函数定义、类定义、if/for/while等语句末尾，表示下面的代码应当缩进，作为语句块，从属以上语句

② 出现在字典中，分开键值对

③ 定义分片、步长

## 4)学会使用 dir() 及 help()

dir() 函数不带参数时，返回当前范围内的变量、方法和定义的类型列表；带参数时，返回参数的属性、方法列表
help() 函数用于查看函数或模块用途的详细说明，返回对象帮助信息

## 5)import使用

导入模块、第三方库

例：

import os
import numpy as np

## 6)pep8 介绍

规范 python 代码风格
建议：
① 所有行的字符数量不超过79个

② 使用 spaces 代替 tab 缩进代码行

③ 



# 4. Pyhon 数值基本知识

## 1) python 中数值类型，int float bool e记法等
int 表示整数，如：1， 2， 3, 4，...整数类型可以转换为浮点数类型，float()
float 表示浮点数，如：3.14, 2.35。浮点类型可以转换为整数类型，int()
Bool 布尔类型，有两个值 True 和 False
e记法 表示过小数或过大数的一种方法



## 2) 算数运算符

假设两变量：a = 5, b = 2：

| 运算符 | 描述                                             | 实例                 |
| :----- | ------------------------------------------------ | :------------------- |
| +      | 两个对象相加                                     | a + b 输出结果为 7   |
| -      | 两个数相减，或表示负数                           | a - b 输出结果为 3   |
| *      | 两个数相乘                                       | a * b 输出结果为 10  |
| /      | 两数相除                                         | a / b 输出结果为 2.5 |
| %      | 取模，返回除法的余数                             | a % b 输出结果为 1   |
| **     | 幂，返回 a 的 b 次幂                             | a ** b 输出结果为 25 |
| //     | 取整除，返回商的整数部分（向下取整，非四舍五入） | a // b 输出结果为 2  |

l   运算符  l        描述        l        实例        l

l :----------- l :----------------- l :---------------- l

l + l 两个对象相加 l a + b 输出结果为 7 l

l - l 两个数相减，或表示负数 l a - b 输出结果为 3 l

l * l 两个数相乘 l a * b 输出结果为 10 l

l / l 两数相除 l a / b 输出结果为 2.5 l

l % l 取模，返回除法的余数 l a % b 输出结果为 1 l

l ** l 幂，返回 a 的 b 次幂 l a ** b 输出结果为 25 l

l // l 取整除，返回商的整数部分（向下取整，非四舍五入） l a // b 输出结果为 2 l

 ## 3)逻辑运算符



 ## 4)成员运算符

 ## 5)身份运算符

## 6)运算符优先级
