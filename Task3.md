
# Task3（2day）

## 1. Dict 字典

### 1） 定义

字典(dict, dictionary的简写)是Python中另一个非常重要的内置数据类型，是Python中映射类型(Mapping Type)，它把“键”(key)映射到“值”(value)，通过key可以快速找到value，它是一种“键值对”(key-value)数据结构。

- “键”，可以是任意不可变的类型对象，如字符串，数字或元组，同一个字典中键是唯一的。
- “值”，可以取任何数据类型。

### 2）创建


```python
# 花括号创建字典，花括号内可以创建多个键值对，键值对用冒号":"隔开
d1 = {} 
d2 = {'a': 1, 'b': 2, 'c': 4} 

# 通过 dict()创建字典
d3 = dict()
d4 = dict(a = 1, b = 2)

# 字典推导式创建字典，通过一个for循环表达式来创建一个字典
dict1 = {x: x*x for x in range(10)}
```

- 不允许同一个键出现两次。创建时如果同一个键被赋值两次，后一个值会被记住


```python
dict = {'Name': '陈国艺', 'City': "广州", 'Name': '广州'}
 
print ("dict['Name']: ", dict['Name'])
```

    dict['Name']:  广州
    

- 键必须不可变，所以可以用数字，字符串或元组充当，而用列表就不行


```python
dict = {['Name']: '陈国艺', 'Age': 28}
 
print ("dict['Name']: ", dict['Name'])
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-11-5d0da9a5f94c> in <module>
    ----> 1 dict = {['Name']: '陈国艺', 'Age': 28}
          2 
          3 print ("dict['Name']: ", dict['Name'])
    

    TypeError: unhashable type: 'list'


### 3）字典的方法

- dictname.clear() 删除字典内所有元素


```python
dict = {'Name': '陈国艺', 'City': "广州"}
dict.clear()
dict
```




    {}



- dictname.copy() 返回一个字典的浅复制


```python
dict = {'Name': '陈国艺', 'City': "广州"}
d = dict.copy()
print(d)
id(d) == id(dict) # 浅拷贝只是拷贝“值”，内存地址 id 没有拷贝
```

    {'Name': '陈国艺', 'City': '广州'}
    




    False



- dictname.items() 以列表返回可遍历的（键，值）元组


```python
dict = {'Name': '陈国艺', 'City': "广州"}
d = dict.items()
print(d)
```

    dict_items([('Name', '陈国艺'), ('City', '广州')])
    

- key in dictname 如果键在字典 dictname 里返回 True，否则返回 False


```python
dict = {'Name': '陈国艺', 'City': "广州"}
'Name' in dict
```




    True



- dictname.values() 返回一个迭代器，可以使用 list() 来转换为列表


```python
dict = {'Name': '陈国艺', 'City': "广州"}
d = dict.values()
print(d)
print(list(d))
```

    dict_values(['陈国艺', '广州'])
    ['陈国艺', '广州']
    

- dictname.pop(key, [default]) 删除字典给定键 key 所对应的值，返回值为被删除的值。key值必须给出，否则，返回默认值（[default] 自主设定该默认值）。


```python
dict = {'Name': '陈国艺', 'City': "广州"}
print(dict.pop('Name', 'N'))
print(dict.pop('', None))
print(dict.pop('','g'))
```

    陈国艺
    None
    g
    

- dictname.popitem() 随机返回并删除字典中的一对键和值(一般删除末尾对)。


```python
dict = {'Name': '陈国艺', 'City': "广州"}
dict.popitem()
```




    ('City', '广州')



- dictname.update(dictname1) 把字典 dictname1 的键值对更新到 dictname 里


```python
dict = {'Name': '陈国艺', 'City': "广州"}
dict1 = {'Age': 26, 'Weight': 130}
dict.update(dict1)
dict
```




    {'Name': '陈国艺', 'City': '广州', 'Age': 26, 'Weight': 130}



- dictname.get(key[,default]) 返回指定键的值，如果值不在字典中返回默认值（[default] 可选参数，不指定参数会返回None，可自主设定参数）


```python
dict = {'Name': '陈国艺', 'City': "广州"}
print(dict.get('Age'))
print(dict.get('Weight', 'hahah'))
```

    None
    hahah
    

- dictname.setdefault(key, default=?) 和get()类似, 但如果键不存在于字典中，将会添加键并将值设为default


```python
dict = {'Name': '陈国艺', 'City': "广州"}
dict.setdefault('Age', 27)
dict
```




    {'Name': '陈国艺', 'City': '广州', 'Age': 27}



- dictname.fromkeys(seq[, value]) 创建一个新字典，以序列seq中元素做字典的键，value 为字典所有键对应的初始值（value 为可选参数）


```python
seq = ('Google', 'Baidu', 'Yahoo')
print(dict.fromkeys(seq))
dict = dict.fromkeys(seq)
print("搜索引擎为 ： {0}".format(str(dict)))

print(dict.fromkeys(seq, 20))
dict = dict.fromkeys(seq, 20)
print("常用的引擎 ： {0}".format(str(dict)))
```

    {'Google': None, 'Baidu': None, 'Yahoo': None}
    搜索引擎为 ： {'Google': None, 'Baidu': None, 'Yahoo': None}
    {'Google': 20, 'Baidu': 20, 'Yahoo': 20}
    常用的引擎 ： {'Google': 20, 'Baidu': 20, 'Yahoo': 20}
    

- dictname.keys()返回一个迭代器，可以用list()来转换为列表


```python
dict = {'Name': '陈国艺', 'City': "广州"}
dict.keys()
list(dict.keys())
```




    ['Name', 'City']



## 2. 集合

### 1） 特性 

- 集合（set）是一个无序的不重复元素序列。

### 2） 创建 

- 使用大括号 { } 创建


```python
set1 = {1, 2, 3, 4, 4}
set1
```




    {1, 2, 3, 4}



- 使用set() 函数创建集合


```python
set2 = set()
print(set2)
```

    set()
    


```python
set3 = set('123456')
print(set3)
set4 = set('abscdsd')
print(set4)
```

    {'5', '2', '3', '6', '4', '1'}
    {'a', 'd', 'b', 'c', 's'}
    

*注意：创建一个空集合必须用 set() 函数而不是大括号 { }，因为 { } 是用来创建一个空字典

- 通过集合推导式创建集合，for...in...循环表达式来创建一个集合


```python
set1 = {x for x in 'abdcgteshdh'}
set1
```




    {'a', 'b', 'c', 'd', 'e', 'g', 'h', 's', 't'}



### 3） 方法

- set.add() 为集合添加元素


```python
set1 = set('abcdefg')
print(set1)
set1.add('k')
set1
```

    {'a', 'e', 'f', 'd', 'b', 'c', 'g'}
    




    {'a', 'b', 'c', 'd', 'e', 'f', 'g', 'k'}



- set.clear() 移除集合中的所有元素


```python
set1 = set('abcdefg')
set1.clear()
set1
```




    set()



- set.difference() 返回多个集合的差值


```python
set1 = set('abcdefg')
set2 = set('fghd')
print(set2.difference(set1))
print(set1.difference(set2))
```

    {'h'}
    {'c', 'a', 'e', 'b'}
    

- set.intersection() 返回集合的交集


```python
set1 = set('abcdefg')
set2 = set('fghd')
set1.intersection(set2)
```




    {'d', 'f', 'g'}



- set.isdisjoint() 判断两个集合是否包含相同的元素，如果没有返回 True，否则返回 False。


```python
set1 = set('abcdefg')
set2 = set('fghd')
print(set1.isdisjoint(set2))
set3 = set('jkl')
print(set3.isdisjoint(set1))
```

    False
    True
    

- set.issubset() 判断指定集合是否为该方法参数集合的子集。如果不是，返回False，否则返回True


```python
set1 = set('abcdefg')
set2 = set('fghd')
set2.issubset(set1)
```




    False



- set.issuperset() 判断该方法的参数集合是否为指定集合的子集。如果不是，返回False，否则返回True


```python
set1 = set('abcdefg')
set2 = set('fg')
set1.issuperset(set2)
```




    True



- set.union() 返回两个集合的并集


```python
set1 = set('abcdefg')
set2 = set('fghd')
set1.union(set2)
```




    {'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h'}



## 3. 判断语句（要求掌握多条件判断）

### if 语句一般形式： elif 、else为可选部分

if <test1>:
    <statements1>
elif <test2>:
        <statements2>
else:
    <statements3>


```python
# 玩猜字游戏
y = 27
x = eval(input("它是一个数字： "))
if x == y:
    print("WOW, you are awesome")
elif x > y:
    print("No, it is too big")
elif 0 < x < y:
    print("No, it is an int. We forget to tell you. Come on, boy, try again")
elif x == 0:
    print("I can't believe you gave me an egg last test")
else:
    print("End")
```

    它是一个数字： -20
    End
    

## 4. 三目表达式

###  Y if X else Z

*只有当 X 为真，Python 才会执行表达式 Y，而只有当 X 为假，才会执行表达式 Z


```python
"广州" if "hotest" else "武汉"
```




    '广州'




```python
"广州" if "" else "武汉"
```




    '武汉'




```python
"一颗不二家棒棒糖" if False else "糖吃多了，会蛀牙"
```




    '糖吃多了，会蛀牙'




```python
"一颗不二家棒棒糖" if True else "糖吃多了，会蛀牙"
```




    '一颗不二家棒棒糖'



## 5. 循环语句

 Python中的循环语句有 while 和 for

### while 循环语句

#### 1. 一般格式

while <test>:
    <statements1>
else:                 # else 为可选部分
    <statements2>


```python
x = 'fantastic'
while x:
    print(x, end=', ')
    x = x[1:]
else:
    print("END")
```

    fantastic, antastic, ntastic, tastic, astic, stic, tic, ic, c, END
    

#### 2. break\ continue\ pass 和循环 else

- break ：跳出最近所在的循环（跳过整个循环语句）
----
- continue ：跳到最近所在循环的开头处（来到循环的首行）
----
- 循环 else 块 ：只有当循环正常离开时才会执行（也就是没有碰到 break 语句）
----
- pass :pass语句是无运算的占位语句

while <test1>:
    <statements1>
    if <test2>: break
    if <test3>: continue
else:
    <statements2>


```python
x = 10
while x:
    x -= 1
    if x % 2 != 0: continue
    print(x, end=' ')
```

    8 6 4 2 0 


```python
x = 10
while x:
    x -= 1
    if x % 2 == 0:   # 无continue，判断语句条件等式发生改变
        print(x, end=' ')
```

    8 6 4 2 0 


```python
while True:
    name = input('Enter your name: ')
    if name == 'stop': break
    age = eval(input('Enter your age: '))
    print('Hello', name, '=>', age**2)
print('End')
```

    Enter your name: guoyi
    Enter your age: 20
    Hello guoyi => 400
    Enter your name: stop
    End
    


```python
y = eval(input('Enter a number: '))
x = y // 2
while x > 1:
    if y % x == 0:
        print(y, 'has factor', x)
        break
    x -= 1
else:
    print(y, 'is prime')
```

    Enter a number: 18
    18 has factor 9
    

### for 循环语句

for 循环是一个通用的序列迭代器：可以遍历任何有序的序列对象内的元素，包括字符串、列表、元组、其它内置可迭代对象等

- 一般格式

for <target> in <object>:
    <statements>
else:    # 可选部分
<statements>

- 添加 break/continue 语句

for <target> in <object>:
    <statements>
    if <test>: break
    if <test>: continue
else:
    <statements>


```python
# for 循环可用于列表数据
for x in ["spam", "eggs", "ham"]:
    print(x, end=' ')
    
```

    spam eggs ham 


```python
# for 循环可用于列表数据
sum = 0
for x in [1, 2, 3, 4]:
    sum += x
sum
```




    10




```python
# for 循环可用于字符串
S = "CHENGUOYI"
for x in S:
    print(x, end=' ')
    
```

    C H E N G U O Y I 


```python
# for 循环可用于元组
T = ("and", "I'm", "okay")
for x in T:
    print(x, end=' ')
    
```

    and I'm okay 


```python
# 嵌套 if 判断语句，break 语句
items = ["aaa", 111, (4, 5), 2.01]
tests = [(4, 5), 3.14]
for key in tests:
    for item in items:
        if item == key:
            print(key, "was found")
            break
    else:
        print(key, "not found")
```

    (4, 5) was found
    3.14 not found
    


```python

```
