[TOC]

# 章节一  就这么愉快的开始吧

## 课时1	我和python的第一次亲密接触

下一条语句： control+n

上一条语句： control+p

新建文件：    command+n

保存文件：    command+s

打开文件：    command+o

运行：	   command+f5

<!--以上快捷键适用于运行在mac os上的idle环境-->

## 课时2	用Python设计第一个游戏

```python
print('-------------我爱鱼C工作室-----------------')
temp = input("不妨猜一下小甲鱼现在心里想的是哪个数字 : ")
guess = int(temp)
if guess == 8:
        print("卧槽 ，你是小甲鱼心里的蛔虫吗？！")
        print("哼 ，猜中了也没有奖励 ！ ")
else:
    print("猜错了 ，小甲鱼现在心里想的是8 ！")
print("游戏结束，不玩啦^_^")
```

# 章节二  成为高手前必须知道的一些基础

## 课时3	小插曲之变量和字符串

### 变量

在使用变量之前，需要对其先赋值

变量名可以包含字母，数字，下划线，但变量名不能以数字开头

字母可以是大写或小写，但大小写是不同的。

等号（=）是赋值的意思，左边是名字，右边是值，不能写反

变量的命名可以取任何合法的名字，但尽量给变量取一个专业的名字

如果在正确的位置输入冒号“:”，IDLE 会自动将下一行缩进！

### 字符串

在一些编程语言，我们可以将两个字符串“相加”在一起，如：'I' + 'Love' +
'FishC' 会得到 'ILoveFishC'，在 Python 里，这种做法叫做拼接字符串

```python
name = input("请输入您的姓名： ")

print("你好， " + name + "!")
```

```python
temp = input('请输入1到100之间的数字: ')
num = int(temp)
if 1 <= num <= 100:
    print('你妹好漂亮')
else:
    print('你大爷好丑')
```

### 原始字符串

- 好像反斜杠是一个好东西，但不妨试试打印：>>>str ='C:\now'
- 我们可以用反斜杠对自身进行转移：>>>str = 'C:\\now'
- 但如果对于一个字符串中有很多个反斜杠：>>>str = 'C:\Program Files\Intel\WiFi\Helpo'
- 原始字符串的使用非常简单，只需要在字符串前边加一个英文字母r即可: >>>str = r'C:\now'

如果字符串中需要出现单引号或双引号怎么办？使用转移符号（\）对字符串中的引号进行转义：

```python
>>> 'let\'s go!'
```

如果非要在原始字符串结尾输入反斜杠，可以如何灵活处理？

```python
>>>str = r'C:\Program Files\FishC\Good''\\'
```

### 长字符串

如果希望得到一个跨越多行的字符串，我们就需要用到三重引号字符串 """ """

## 课时4	改进我们的小游戏

### 条件分支

Python的比较操作符

| >    | 左边大于右边     |
| ---- | ---------------- |
| >=   | 左边大于等于右边 |
| <    | 左边小于右边     |
| <=   | 左边小于等于右边 |
| ==   | 左边等于右边     |
| !=   | 左边不等于右边   |

Python的条件分支语法：

if 条件 ：

​	条件为真(Yrue)执行的操作

else:

条件为假（Flase）执行的操作

```python
print("---------我爱鱼c工作室------")
temp = input("不妨猜一下小甲鱼现在心里想的是哪个数字：")
guess = int(temp)
if guess == 8:
  print("挖槽，你是小甲鱼心里的蛔虫吗？")
  print("哼，猜中了也没有奖励")
else:
  if guess > 8:
    print("哥，大了大了～～")
  else:
    print("嘿，小了小了！")
print("游戏结束，不玩了～～")
```

### while循环

Python的While循环语法：

while 条件 ：

条件为真(True)执行的操作

```python
print("---------我爱鱼c工作室------")
temp = input("不妨猜一下小甲鱼现在心里想的是哪个数字：")
guess = int(temp)
while guess != 8:
		temp = input("哎呀，输错了，重新输入吧：")
		guess = int(temp)
		if guess == 8:
		  print("挖槽，你是小甲鱼心里的蛔虫吗？")
  		print("哼，猜中了也没有奖励")
		else:
  		if guess > 8:
    		print("哥，大了大了～～")
  		else:
   			print("嘿，小了小了！")
print("游戏结束，不玩了～～")
```

and逻辑操作符——Python的and逻辑操作符可以将任意表达式连接在一起，并得到一个布尔类型的值。

| 运算符 | 描述                                                         | 实例                      |
| ------ | ------------------------------------------------------------ | ------------------------- |
| and    | 布尔"与" - 如果x为False，x and y返回False，否则它返回y的计算值。 | (a and b) 返回 true       |
| or     | 布尔"或" - 如果x是True，它返回True，否则它返回y的计算值。    | (a or b) 返回 true。      |
| not    | 布尔"非" - 如果x为True，返回False。如果x为False，它返回True。 | not(a and b) 返回 false。 |

random模块——这个random模块里边有一个函数叫做randint(), 它会返回一个随机的整数。

```python
import random
secret = random.randint(1,10)
print("---------我爱鱼c工作室------")
temp = input("不妨猜一下小甲鱼现在心里想的是哪个数字：")
guess = int(temp)
while guess != secret:
		temp = input("哎呀，输错了，重新输入吧：")
		guess = int(temp)
		if guess == secret:
		  print("挖槽，你是小甲鱼心里的蛔虫吗？")
  		print("哼，猜中了也没有奖励")
		else:
  		if guess > secret:
    		print("哥，大了大了～～")
  		else:
   			print("嘿，小了小了！")
print("游戏结束，不玩了～～")
```

## 课时5	闲聊之Python的数据类型

### 数值类型

整型——整数，如 1，2，

浮点型——如3.1415926

布尔型——True表示1，False表示1

e记法——如1.5e10表示1.5的十次方

### 类型转换

转整数：int()

转字符串：str()

转浮点数：float()

### 获得关于类型的信息

```python
>>> a = '520'
>>> type(a)
<class 'str'>
```

```python
>>> a = '小甲鱼'
>>> isinstance(a, str)
True
>>> isinstance(a, int)
False
>>> isinstance(320, int)
True
>>> isinstance(320.25, bool)
False
```

## 课时6	Python之常用操作符

### 算术操作符

+,-,*,/

% 取余数

** 幂运算

// 取整数

#### 优先级

先乘除后加减，遇到括号先算括号里面的

### 比较操作符

### 逻辑操作符

and,or,not	True / false

#### 优先级

幂运算		 **

正负号		 +x 	+x

算数操作符	* 	/	 //	 +	 -

比较操作符	< 	<=	 >	 >= 	==	 !=

逻辑运算符	not 	and 	or

# 章节三  了不起的分支和循环

## 课时7	了不起的分支和循环1

```python
打飞机框架.py

加载背景音乐
播放背景音乐（设置单曲循环）
我放飞机诞生
interval = 0

while True:
 		if 用户是否点击了关闭按钮：
  			退出程序
    interval += 1
    if interval  == 50:
      	interval = 0
     		小飞机诞生
    小飞机移动一个位置
    屏幕刷新
    
    if 用户鼠标产生移动：
    		我方飞机中心位置 = 用户鼠标位置
      	屏幕刷新
      
    if 我方飞机与小飞机发生肢体冲突：
    		我方挂，播放撞机音乐
    		修改我方飞机图案
        打印"Game over"
        停止背景音乐，最好淡出
```

## 课时8	了不起的分支和循环2

### assert 的作用

assert这个关键字我们称之为“断言”，当这个关键字后边的条件为假的时候，程序自动崩溃并抛出AssertionError的异常。
什么情况下我们会需要这样的代码呢？当我们在测试程序的时候就很好用，因为与其让错误的条件导致程序今后莫名其妙地崩溃，不如在错误条件出现的那一瞬间我们实现“自爆”。
一般来说我们可以用Ta再程序中置入检查点，当需要确保程序中的某个条件一定为真才能让程序正常工作的话，assert关键字就非常有用了。

### 如何快速将三个变量的值互相交换？

假设有 x = 1，y = 2，z = 3，

x, y, z = z, y, x

### 成员资格运算符：in

用于检查一个值是否在序列中，如果在序列中返回 True，否则返回 False。

```python
>>>name = '小甲鱼'
>>>'鱼' in name
True
>>>'肥鱼' in name
False
```



## 课时9	了不起的分支和循环3

### while循环

while	条件：

​		循环体

### for循环

#### 语法：

for	目标	in	表达式：

​		循环体

```python
> > > favourite = 'FishC'

> > > for i in favourite:
  				print(i,end="")
FishC
```

```python
>>>member = ['小甲鱼'，'小布丁'，'黑夜']
>>>for each in member:
		print(each,len(each))
小甲鱼 3
小布丁 3
黑夜 2
```

### range()

#### 语法：

range([strat,] stop[, step=1])

——这个BIF有三个参数，其中用中括号括起来的两个表达这两个参数是可选的。

——step=1表示第三个参数的值默认值是1。

——range这个BIF的作用是生成一个从start参数的值开始到stop参数的值结束的数字序列。

```python
>>>range(5)
range(0,5)
>>>list(range(5))
[0,1,2,3,4]
for i in range(5):
  	print(i)
    
0
1
2
3
4
>>>for i in range(2,9):
  			print(i)
    
2
3
4
5
6
7
8
>>>for i in range(1,10,2):
  			print(i)
    
1
3
5
7
9

```

### 两个关键语句break和continue

break语句的作用是终止当前循环，跳出循环体。

continue语句的作用是终止本轮循环并开始下一轮循环（这里要注意的是：在开始下一轮循环之前，会先测试循环条件）

# 章节四  列表，元组和字符串

## 课时10 列表：一个打了激素的数组1

```python
打飞机框架.py
		加载背景音乐
		播放背景音乐（设置单曲循环）
    我方飞机诞生
while True:
  	if 用户是否点击了关闭按钮：
    		退出程序
    小飞机诞生
    小飞机移动一个位置
    屏幕刷新
    if	用户鼠标产生移动：
    		我方飞机中心位置 = 用户鼠标位置
      	屏幕刷新
    if  我方飞机与小飞机发生肢体冲突：
    		我方挂，播放撞击音乐
      	修改我方飞机图案
      	打印"Game over"
        停止背景音乐，最好淡出
```

