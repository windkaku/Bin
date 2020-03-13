# Python



## 1.基本语法

​	如无法正确打印汉字，在文件开头加入 **# -\*- coding: UTF-8 -\*-** 或者 **# coding=utf-8** 

​	Python 可以同一行显示多条语句，方法是用分号 **;** 分开

​	python用缩进来写模块。缩进的空白数量是可变的，但是所有代码块语句必须包含**相同的**缩进空白数量。

​	可以使用斜杠 **\\** 将一行的语句分为多行显示

​	**注释**：\# ，多行注释用'''   '''、""" """

​	**变量**：用来保存和表示数据的占位符号，变量采用标识符（名字）来表示。

​	**命名规则**：大小写字母、数字、下划线、汉字等字符及组合。注意：大小写敏感、首字符不能是数字、不与保留字相同。保留字有33个。

<p><img src="https://raw.githubusercontent.com/windkaku/Bin/master/%E4%BF%9D%E7%95%99%E5%AD%97%E8%A1%A8%E6%A0%BC.png" alt="保留字表格" width="300"/></p>
#### 		数据类型

​		**字符串类型**：‘ ‘ (单个)或者 “ ”(句子)

   > 字符串正向递增序号开头为0，反向递减序号结尾为-1

​		**索引[]**：返回字符串中单个字符  <字符串>[序号位置]

​		**切片[: ]**：返回字符串中一段字符子串  <字符串>[M:N]，意为取出字符串中第M-1到第N-1个字符，但不到第N个字符。<字符串>[M:]，输出从第M个字符开始的字符串。<字符串>[M:N:X]，输出从M-1到N-1并设置步长为X（间隔X-1个位置）。加号（+）是字符串连接运算符，星号（*）是重复操作。

​		**列表[ , , ]**

​		**元组 ( , , )**：类似于List（列表）。但是不能二次赋值，相当于只读列表。

​		**字典{ }**：字典由索引(key)和它对应的值value组成。

​		**数字语句**：整数int、浮点数float（带小数点）

​		**赋值语句**：=

​		**分支语句**：if: elif: else:

​		**输出语句print**：默认输出是换行的，如果要不换行在变量末尾加上 **,**

​		**删除语句del**：del vardel var_a, var_b



#### 		函数：<函数名>(<参数>)

   + 输入函数 **input()** ：从控制台获得用户输入的函数。使用格式：<变量>=input(<提示信息字符串>)

   + 输出函数 **print()** ：以字符形式向控制台输出结果的函数。

   + 评估函数 **eval()**：去掉参数最外侧引号并执行余下语句的函数。 

   **{ }** 表示槽，后续变量填充到槽中。

   > {:.2f}表示将变量C填充到这个位置时取小数点后2位。

​	Python数据类型转换：有时候，我们需要对数据内置的类型进行转换，数据类型的转换，你只需要将数据类型作为函数名即可

+ 随机数函数

| 函数                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [choice(seq)](https://www.runoob.com/python/func-number-choice.html) | 从序列的元素中随机挑选一个元素，比如random.choice(range(10))，从0到9中随机挑选一个整数。 |
| [randrange ([start,\] stop [,step])](https://www.runoob.com/python/func-number-randrange.html) | 从指定范围内，按指定基数递增的集合中获取一个随机数，基数默认值为 1 |
| [random()](https://www.runoob.com/python/func-number-random.html) | 随机生成下一个实数，它在[0,1)范围内。                        |
| [seed([x\])](https://www.runoob.com/python/func-number-seed.html) | 改变随机数生成器的种子seed。如果你不了解其原理，你不必特别去设定seed，Python会帮你选择seed。 |
| [shuffle(lst)](https://www.runoob.com/python/func-number-shuffle.html) | 将序列的所有元素随机排序                                     |
| [uniform(x, y)](https://www.runoob.com/python/func-number-uniform.html) | 随机生成下一个实数，它在[x,y]范围内。                        |



#### 运算符

​	**算术运算符**：加（+），减（-），乘（*），除（/），取余数（%），幂（**），取整数（//）。

​	**比较运算符**：等于（==），不等于（!=），大于（>），小于（<），大于等于（>=），小于等于（<=）

​	**赋值运算符**：=（c=a+b），+=（c=c+a），-=（c=c-a），\*=（c=c\*a），/=（c=c/a），%=（c=c%a），\*\*=（c=c\*\*a），//=（c=c//a）

​	**位运算符**：&，|，^，~，<<，>>，

​	**逻辑运算符**：and，or，not

​	**成员运算符**：in（在，返回true），not in（不在，返回true)

​	**身份运算符**：用于比较两个对象的存储单元。is，is not



#### 条件语句

 	**if 语句**用于控制程序的执行，基本形式为：
```
    if 判断条件:
        执行语句……
    elif 判断条件2:
         执行语句2……
    else:
        执行语句……
```



#### 循环语句

​	**while 循环**：在给定的判断条件为true时执行循环体，否则退出循环体。

```
while 判断条件(condition)：
      执行语句(statements)……
```



```flow
st=>start: 开始框
cond=>condition: 判断框(是或否?)
sub1=>subroutine: 子流程
e=>end: 结束框
st->cond
cond(no)->e
cond(yes)->sub1(left)->cond
```

​      while 语句时还有另外两个重要的命令 continue，break 来跳过循环，continue 用于跳过该次循环，break 则是用于退出循环.

​      while … else 在循环条件为 false 时执行 else 语句块。



​	**for 循环**：遍历任何序列的项目，如一个列表或者一个字符串

```
for iterating_var in sequence:
   statements(s)
```

​      另外一种执行循环的遍历方式是通过索引

```
fruits = ['banana', 'apple',  'mango']
for index in range(len(fruits)):
   print '当前水果 :', fruits[index]
```

`函数 len() 返回列表的长度，即元素的个数。 range返回一个序列的数。`



​	**嵌套循环**：在while循环体中嵌套for循环