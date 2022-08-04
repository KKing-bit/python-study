# 环境搭建

1、安装python： https://www.python.org/downloads/windows/ <br>
2、安装PyCharm Community（社区版，免费）；https://www.jetbrains.com/pycharm/download/<br>
3、安装python解释器：//www.python.org/  - Downloads - 选择python版本号<br>
4、安装VScode，官网地址：https://code.visualstudio.com/ <br>

# 语法  
## 行和缩进：同一个代码语句缩进需要相同  
```python
if True:  
    print("answer")  
    print("Ture")  
else:  
    print("answer")  
    print("False")  
 ```

## 多行语句:\实现多行语句,在 [], {}, 或 () 中的多行语句，不需要使用 \  
```python
total = ['item_one', 'item_two', 'item_three',  
        'item_four', 'item_five']  
```
## 数字类型  
```python
str='123456789'  

print(str)# 输出字符串  
print(str[0:-1])  
print(str[0])  
print(str[2:5])  
print(str[2:])  
print(str[1:5:2])  
print(str*2)  
print(str+'你好')  
print('--------------------------------')  
print('hello\nrunboot')  
print(r'hello\nrunboot')  
print('\n') # \n代表转义  
print(r'\n') # r代表 raw string，自动反转义  
```

## 空行  
```python 
print("hello") 
# 空行不影响执行，主要为了维护  
```

## 同一行显示多条语句  
```python 
import sys; X='runoob'; sys.stdout.write(X + '\n')  
```

## print输出  

```python 
# 换行输出
x="a"  
y="b"  
print( x )  
print( y )  
print('-------')  

#不换行输出加上, end=''即可
print( x, end='')  
print( y, end='')  
print()  
```


# 基础数据类型
## 变量赋值
```python 
counter = 100 # 变量必须要被赋值
miles   =1000.0
name    ='runoob'
print(counter)
print(miles)
print(name)
# 多个变量赋值
a=b=c=1
a ,b ,c ,=1,2,'runoob'
print(a)
print(b)
print(c)
```


## Number(数字)
```python 
## 数据类型包含:不可变：number（数字）string（字符串）tuple（元组）；可变：list（列表）dictionary（字典）、set（集合）；
# 数值运算
```
## String（字符串）
```python 
str = 'runoob'

print(str)
print(str[0:-1])
print(str[0])
print(str[2:5])
print(str * 2)
print(str + 'TEST')
```
## list（列表）
```python 
# ()[]{}的区别，()是tuple元组数据，不可变序列；[]是list数据类型，可变序列；{}dict字典类型，字典的值存在于key下

list=['abcd',786,2.23,'runoob',70.2 ]
tinylist = [123,'runoob']
print(list)
print(list[0])
print(list[1:3])
print(list[2:])
print(tinylist * 2)
print(list + tinylist) #与字符串不一样，列表元素可变
```
```python 
def reverseWords(input):
    inputWords = input.split(" ")
    inputWords = inputWords[-1::-1]
    output = ' '.join(inputWords)
    return output
if __name__ == "__main__":
    input = 'I like runoob'
    rw = reverseWords(input)
    print(rw)
```
## tuple（元组）
```python 
tuple = ('abcd',786,2.23,'runoob',70.2 )
tinytuple = (123,'runoob')

print(tuple)
print(tuple[0])
print(tuple[1:3])
print(tuple[2:])
print(tinytuple * 2)
print(tuple + tinytuple)
```

```python 
#字符串也是一种特殊的元组
tup =(1,2,3,4,5,6)
print(tup[0])
print(tup[1:5])
```
## SET（集合）
```python 
sites = {'google','taobao','runoob','facebook','zhihu','baidu'}
print(sites)
#成员测试
if 'runoob'in sites :
    print('runoob在集合中')
else:
    print('runoob不在集合中')

#site可以进行集合运算
a = set('abracadabra')
b = set('alacazam')

print(a)
print(a-b)
print(a | b)
print(a & b)
print(a ^ b)
```
## dictionary（字典）
```python 
dict = { }
dict['one'] = '1-菜鸟教程'
dict[2] = '2-菜鸟教程'
tinydict={'name':'runoob','code':1,'site':'www.runoob.com'}

print(dict['one'])
print(dict[2])
print(tinydict)
print(tinydict.keys())
print(tinydict.values())
```
# 数据类型转换
## 隐式类型互换
```python 
num_int = 123
num_flo = 1.23

num_new = num_int + num_flo

print('datatype of num_int:',type(num_int))#num_int 的数据类型是整型（int）
print('datatype of num_flo:',type(num_flo))#num_flo 的数据类型是浮点型(flo)

print('value of num_new:',num_new)
print('datatype of num_new:',type(num_new))

print('---------')

num_int = 123
num_str = '456'
print('datatype of num_int:',type(num_int))
print('datatype of num_str:',type(num_str))
```
## 显式转换
```python 
x = int(1),float(1),
y = int(2.8),float(2.8),
z = int('3'),float('3'),
print(x)
print(y)
print(z)

#整型和字符串的计算可以用强制转类型完成
num_int = 123
num_str = '456'
num_str = int(num_str)
print(num_int + num_str)
```
#python 推导式
## 列表式推导
```python 
for变量 in列表 if条件
# 过滤掉长度小于或等于3的字符串列表，并将剩下的转换成大写字母：

names = ['bob','tom','alice','jerry','wendy','smith']
new_names = [name.upper() for name in names if len(name)>3]
print(new_names)

```
```python 
#计算 30 以内可以被 3 整除的整数：

multiples = [i for i in range (30) if i % 3 == 0]
print(multiples)
```

## 字典推导
```python 
#使用字符串及其长度创建字典

listdemo = ['google','runoob','taobao']
newdict = {key:len(key) for key in listdemo}
print(newdict)

# 有三个数字，以三个数字的平方为值创建字典

dic = {x :x **2 for x in (2,4,6)}
print(dic)
```

## 集合推导式
```python 
#计算1，2，3的平方

setnew = {i**2 for i in (1,2,3)}
print(setnew)

#判断不是abc的字母并且输出

a = {x for x in "abracadabra" if x not in 'abc'}
print(a)

```

## 元组推导式
```python 
# 生成包含1~9的元组,元组是用的（）,使用tuple（）可以将生成器换成元组

a = (x for x in range(1,10))
print(a)

#疑点：怎么用tuple() 函数，将生成器对象转换成元组
```





