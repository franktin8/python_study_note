# 1 基础知识

## 1.1 起步

## 1.2 变量和简单数据类型

### 入门

解释器、语法突出

### 变量

变量

值

变量的命名与使用

### 字符串

函数**title()**：以首字母大写的方式显示每个单词

函数**upper()**：全部大写

函数**lower()**：全部小写

**+**：拼接字符串

**\t**：制表符

**\n**：换行符

函数**strip()**：剔除字符串两端的空白

函数**lstrip()**：剔除字符串开头的空白

函数**rstrip()**：剔除字符串末尾的空白

### 数字

运算（加+ 减- 乘* 除/ 乘方**）

浮点数（带小数点的数字）

函数**str()**：以避免**类型错误**

### 注释

**#**：单行注释

**'''**/**"""**：多行注释

## 1.3 列表简介

### 列表是什么

**列表**：用[ ]表示，用,分隔其中的元素 fruits = ['apple' , 'banana' , 'pear']

**访问列表元素**：print(fruits[0]) 返回结果apple  print(fruits[-1]) 返回结果pear

### 修改、添加和删除元素

**修改列表元素**：fruits[1] = watermelon

方法**append()**：在列表末尾添加元素 fruits.append('pineapple')

方法**insert()**：在列表任意位置添加元素 fruits.insert(0, 'pineapple')

语句**del**：删除指定位置的元素 del fruits[0]

方法**pop()**：弹出列表指定位置的元素 last_ate = fruits.pop(2) 未给定位置的情况下默认弹出末尾元素

方法**remove()**：删除指定值的元素 fruits.remove('apple')

### 组织列表

方法**sort()**：永久性排序 参数reverse=True

方法**sorted()**：临时排序

方法**reverse()**：反转

函数**len()**：获取列表长度

### 使用列表时避免索引错误

## 1.4 操作列表

### 遍历整个列表

```python
for magician in magicians:
```

### 避免缩进错误

### 创建数值列表

函数**range()**：

```python
value in range(1,5)

numbers = list(range(1,6))

# 1～10之间的偶数，从2开始数，然后不断增加2，直到达到终值11
even_numbers = list(range(2,11,2))  
```

函数**min()**：min(numbers)

函数**max()**：max(numbers)

函数**sum()**：sum(numbers)

列表解析：squares = [value**2 for value in range(1,11)]

### 使用列表的一部分

切片：players[0,3]

遍历切片：

复制列表：创建一个包含整个列表的切片 nums_a = nums[:]

### 元组

sum = (1 , 2)

## 1.5 if语句

### 一个简单示例

```python
cars = ['audi', 'bmw', 'subaru', 'toyota']
for car in cars:
		if car == 'bmw':
				print(car.upper())
		else:
      	print(car.title())
```

### 条件测试

检查是否相等：==

检查是否相等时**区分大小写**

检查是否**不**相等：!=

比较数字：小于 <  小于等于 <=  大于 >  大于等于 >=

检查多个条件：and or

检查特定值是否包含在列表中：in

检查特定值是否**不**包含在列表中：not in

布尔表达式：True False

## 1.6 字典

### 一个简单的字典

```python
alien_0 = {'color': 'green', 'points': 5}
print(alien_0['color'])
print(alien_0['points'])
```

### 使用字典

```python
# 创建一个空字典
alien_0 = {}

# 创建一个字典
alien_0 = {'color': 'green'}

# 添加键-值对
alien_0['x_position'] = 0

# 访问字典中的值
print(alien_0['color'])

# 修改字典中的值
alien_0['color'] = 'yellow'

# 删除键-值对
del alien_0['points']
```

### 遍历字典

```python
# 由类似对象组成的字典
favorite_languages = {
    'jen': 'python',
    'sarah': 'c',
    'edward': 'ruby',
    'phil': 'python',
    }

# 遍历所有的键-值对 方法items() 
for name, language in favorite_languages.items():
    print(name.title() + "'s favorite language is " +
        language.title() + ".")

# 遍历字典中的所有键 方法keys()
for name in favorite_languages.keys():
    print(name.title())

# 遍历字典时，会默认遍历所有的键 即，下面的代码跟上面一段得到的输出一致
for name in favorite_languages:
    print(name.title())

# 在遍历前对列表进行排序 函数sorted()
for name in sorted(favorite_languages.keys()):
    print(name.title()+", thank you for taking the poll.")

# 遍历字典中的所有值 方法values()
print("The following languages have been mentioned:")
for language in favorite_languages.values():
  	print(language.title())

# 遍历并剔除重复项 set()
print("The following languages have been mentioned:")
for language in set(favorite_languages.values()):
  	print(language.title())
```

### 嵌套

```python
# Make an empty list for storing aliens.
aliens = []

# Make 30 green aliens.
# range()的唯一用途是控制循环次数
for alien_number in range(30):
    new_alien = {'color': 'green', 'points': 5, 'speed': 'slow'}
    aliens.append(new_alien)

for alien in aliens[:3]:
    if alien['color'] == 'green':
        alien['color'] = 'yellow'
        alien['speed'] = 'medium'
        alien['points'] = 10
    
# Show the first 5 aliens.
for alien in aliens[:5]:
    print(alien)
print("...")
```

## 1.7 用户输入和while循环

### 函数input()的工作原理

编写清晰的程序

使用int()来获取数值输入：age = int(age)

求模运算符%：将两个数相除并返回余数，可用于判断奇偶

### while循环简介

使用while循环

```python
current_number = 0
while current_number < 10:
    current_number += 1
    if current_number % 2 == 0:
        continue
    print(current_number)
```
