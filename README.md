# Python-26-
Python学习笔记(26)
# p83 字符串的比较操作
print('apple'>'app')  #True
print('apple'>'banana')  #False  97>98?
print(ord('a'),ord('b'))  #ord原始值

print(chr(97),chr(98))  #和ord是一对相等的操作

'==与is的区别'
'==比较的是value'
‘is比较的是id是否相等’
a=b='Python'
c='Python'
print(a==b)  #True
print(b==c)  #True

print(a is b)  #True
print(a is c)  #True
print(id(b))
print(id(c))
print(id(a))  #这三个字符串指向的是同一块内存空间



# p84 字符串的切片操作
#字符串是不可变类型，列表是可变类型
#共同特点是切片后会产生一个新的对象
s='hello,Python'
s1=s=[:5]
s2=s[6:]
s3='!'
newstr=s1+s3+s2   #切出来的字符串id都是新的

print(s[1:5:1])  #ello 从1开始截到5，不包括索引为5的元素
print(s[::2])  #hloPto  默认0开始，最后一个元素结束，步长为2
print(s[::-1])  #结果倒过来 从最后一个元素开始，到第一个元素结束
print(s[-6::1])  #输出Python，从索引为-6开始，到最后一个元素结束，步长为1



# p85 格式化字符串
#(1) % 占位符
name='张三'
age=20
print('我叫%s,今年%d岁' % (name,age))  #最后一个%是固定符号 (name,age)是一个元组

#(2) {} 占位符
print('我叫{0},今年{1}岁'.format(name,age))

#(3)f-string
print(f'我叫{name},今年{age}岁')

print('%10d' % 99)  #10指的是宽度，99前面会有一块空白
print('%.3f' % 3.1415926)  #.3表示的是精度输出3.142 这里保留了三位小数
print('hellohello')

#同时表示宽度和精度
print('%10.3f' % 3.1415926)  #输出为前面空一块总宽度为10，小数表留3位小数

print('{0:.3}'.format(3.1415926))  #这里的.3表示的是一共三位数 输出为3.14
print('{0:.3f}'.format(3.1415926))  #.3f表示的是3位小数
print('{0:10.3f}'.format(3.1415926))。#这里是宽度加精度  一共10位，3位是小数
