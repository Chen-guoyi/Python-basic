# Task2 


## 1. 列表
### 1)标志
- 列表用方括号"[]"表示
- 列表是可变序列对象
- 列表可以包含任何种类的对象：数字、字符串、元组、其他列表
- 列表支持索引、合并和迭代等操作

### 2)基本操作(创建，append(),pop(),del(),拷贝)
假设变量：L
#### 创建列表：
- L = [1, 2, 3]
- L = list(1, 2, 3)
#### append()  列表增长：在列表末端增加单一对象
- L.append(4) 结果是 L = (1, 2, 3, 4)
#### pop() 删除一个元素，并返回该元素值
- L.pop(), 删除最末端一个元素，并返回该元素
- L.pop(i)， 删除给定偏移（索引值）的元素，并返回该元素
#### del() 删除某项或某片段（给定索引包含的所有元素）
- del L[0], 删除元素"1"
- del L[1:], 删除元素"2", "3"
### 3)列表相关方法 
假设变量：L
- L.sort() 排序 假设L = [3, 2, 0, 5], L.sort()，L 返回[0, 2, 3, 5]
- L.extend() 列表末端插入多个元素 L.extend([4, 5, 6])
- L.insert(i, x) 在位置 i 之前插入元素 x
- L.remove(k) 移除列表 L 元素 k, 若k不在列表内，则返回 ValueError
- L.clear() 移除列表 L 的所有项
## 2.元组
### 1)标志
- 元组以小括号"()"表示
- 元组是不可变序列
- 元组可以包含其他的复合对象，如：列表、字典和其他元组等
- 元组支持索引、分片

### 2)基本操作(创建及不可变性)
#### 创建
假设变量：L
- L = (1, 2, 3)
- L = (1,)
- L = 1, 2, 3
- L = tuple()
#### 不可变性
- 元组中的元素值是不允许修改的
- 元组之间可以使用 + 号和 * 号进行运算，运算后会生成一个新的元组
## 3.string字符串
### 1)定义及基本操作(+，*，读取方式)
#### 定义：一个有序的字符的集合，用来存储和表现基于文本的信息
#### 基本操作（+，*，读取方式）
- '+' 合并字符串
- '*' 重复字符串自身
- 元组可以用下标索引来访问元组中的值
### 2)字符串相关方法
- replace() 字符串替换，给定被替换字符串、替换字符串
- find() 返回子字符串出现处的偏移量（默认从前向后开始搜索）
- split() 将一个字符串分割为一个子字符串的列表，以分隔符字符串为标准。分隔符如：空格、逗号,、甚至字符串
- rstrip() 清除每行末尾的空白
## 4.字符串格式化问题
1. f-Strings：一种改进Python格式字符串的新方法
2. str.format()
3. %-formatting
