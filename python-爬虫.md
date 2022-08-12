# 环境搭建

1、安装python： https://www.python.org/downloads/windows/ <br>
2、安装PyCharm Community（社区版，免费）；https://www.jetbrains.com/pycharm/download/<br>
3、安装python解释器：//www.python.org/  - Downloads - 选择python版本号<br>
4、安装VScode，官网地址：https://code.visualstudio.com/ <br>

# 一、语法  
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
# 二、数据类型转换
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
# 三、推导式
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

# 四、运算符
## 算数运算符
```python
a = 21
b = 10
c = 0
c = a + b
print('1-c的值为：',c)
c = a - b
print('2-c的值为：',c)
c = a * b
print('3-c的值为：',c)
c = a / b
print('4-c的值为：',c)
c = a % b
print('5-c的值为:',c)
c = a ** b
print('6-c的值为：',c)
c = a // b
print('6-c的值为：',c )
```

## 比较运算符
```python
a = 21
b = 10
c = 0
if(a == b ):
    print('1-a等于b')
else:
    print('1-a不等于b')

if a!=b:
    print('2-a不等于b')
else:
    print('2-a等于b')

if a<b:
    print('3-a小于b')
else:
    print('3-a大于b')

if a>b:
    print('4-a大于b')
else:
    print('4-a小于b')

if a <= b :
    print( '5-a 小于等于b')
else:
    print('5-a大于b')

if b >= a :
    print('6-b大于等于a')
else:
    print('6-b小于a')
```

## python的赋值运算
```python
# 假设变量a为10，变量b为20
a = 21
b = 10
c = 0

c = a + b
print('1-c:',c)

c += a
print('2-c:',c )

c *=a
print('3-c:',c)

c /=a
print('4-c:',c)

c = 2
c %=a
print('5-c:',c)

c **=a
print('6-c:',c)

c //=a
print('7-c:',c)
```

## python位运算符
```python
# 二进制的计算 &，|，^，~，<<，>>
a=60
b=13
c=0
c=a&b  #如果两个相应位都为1,则该位的结果为1,否则为0
print('1-c:',c)

c=a | b  #只要对应的二个二进位有一个为1时，结果位就为1。
print('2-c:',c)

c=a ^ b #当两对应的二进位相异时，结果为1
print('3-c:',c)

c= ~ a #对数据的每个二进制位取反,即把1变为0,把0变为1。~x 类似于 -x-1
print('4-c:',c)

c =a << 2 #运算数的各二进位全部左移若干位，二进制左移几位就是后面加几个0，前面去掉几位
print('5-c:',c)

c=a >> 2 #运算数的各二进位全部右移若干位，二进制右移几位就是后面去几位，前面加几位（正数加0，负数加1）
print('6-c:',c)
```

## 逻辑运算符
```python
# not and or,not:真变假假变真、and：两个为真才为真、or：两个为假才为假
print( 2 >0 )
print(not 2>0 and 3>0 or 4>0 )
```

## 成员运算符
```python
a = 10
b = 20
list = [1,2,3,4,5,6]
print( a in list )
```

## 身份运算符
```python
#is,is not;  is和==的区别，is判断是不是同一个，==判断值是否相等
a = 20
b = 20
print(a is b)
print( id(a) == id(b) )
```

# 数字（NUMBER)
```python
#// 得到的并不一定是整数类型的数，它与分母分子的数据类型有关系。
print(7.0//2)
print(7//2)
```
```python
#**进行幂运算
print( 2**7 )
```

# 字符串
```python
#字符串格式化
print('我叫%s，今年%d岁！'  %('小明' , 10 ))
print(f"我叫%s，今年%d岁！" %('小明' , 10 ))
```
```python
#字符串三引号
parade='''这是一个字符串的实例
多行字符串可以通过制表符
TAB(\t)。
也可以用换行符[ \n ]。
'''
print( parade )
```
```python
#f-string,f用大括号 {} 包起来，它会将变量或表达式计算后的值替换进去,不用再去判断使用 %s，还是 %d
x=1
print(f'{x+1}')

print(f'{x+1=}')
```

# 五、编程第一步
```python
#斐波纳契数列:第三项开始，每一项都是前两项之和
a , b =0 , 1
while b<10:
    print(b)
    a,b = b,b+a
```
```python
#数列输出到一行，用end
a , b=0 , 1
while b <1000:
    print(b, end=',')
    a,b=b,b+a
```

# 六、条件控制
```python
#if语句关键词，if elif else,条件后面要加：，表示满足条件后执行
#算算狗的年龄脚本
age = int(input('请输入你家狗的年龄:'))
print('')
if age <= 0:
    print('你在逗我吧')
elif age == 1:
    print('相当于14岁的人')
elif age == 2:
    print('相当于22岁的人')
elif age > 2:
    human =22+(age - 2)*5
    print('相当于人类年龄：', human )
```
```python
#数字猜谜游戏脚本
number = 7
guess = -1
print('数字猜谜游戏！')
while guess != number:
    guess = int(input('请输入你猜的数字： '))

    if guess == number :
        print('恭喜你猜对了！')
    elif guess < number:
        print('猜的数字太小了!!')
    elif guess > number:
        print('猜的数字太大了！！')
```
```python
#if嵌套语句
num=int(input('请输入一个数字：'))
if num%2 == 0:
    if num%3 == 0:
        print('你输入的数字可以整除2 和 3 ')
    else:
        print('你输入的数字可以整除2 但不能整除3')
else:
    if num%3 == 0:
        print('你输入的数字可以整除3，但不能整除2')
    else:
        print('你输入的数字不能整除2和3 ')
```

# 七、循环语句
## while 循环
```python
# 计算1~100的和
n = 100
sum = 0
counter = 1
while counter <= n:
    sum = sum + counter
    counter += 1
print('1到 %d 的和为： %d'  %(n,sum))
```
```python
# 无限循环
var = 1
while var == 1:
    num = int(input('请输入一个数字 ： '))
    print('你输入的数字是：', num )
print('good bye!')
```
```python
#while循环使用else
count = 0
while count < 5:
    print(count, '小于5')
    count = count + 1
else:
    print(count, '大于或等于5')
```
```python
#简单语句组
#如果只打印一个语句，那可以与while写成一行，无限循环，用control c打断
flag = 1
while(flag):print("欢迎光临")
print('good bye!')
```

## for循环
```python
languages = ['c','c++','per1','python']
for x in languages:
    print(x)
```
```python
#for循环的break语句
sites = ['baidu' ,'google' ,'runoob','taobao']
for site in sites:
    if site == 'runoob':
        print('菜鸟教程')
        break
    print('循环数据' + site)
else:
    print('没有循环语句')
print('完成循环')
```

## range()函数
```python
for i in range(5):
    print(i)
#指定范围
for i in range(5,9):
    print(i)
#指定步长
for i in range(0,10,4):
    print(i)
#序列索引
a = ['google','baidu','runoob','taobao','qq']
for i in range(len(a)):
    print(i,a[i])

#创建列表
print(list(range(5)))
```

## break 和 continue 语句及循环中的 else 子句
```python
#break是打断循环，结束；continue跳过当前语句，继续循环
n = 5
while n > 0:
    n -= 1
    if n == 2:
        break
    print(n)
print('循环结束。')
```
```python
#continue 案例
n = 5
while n > 0:
    n -= 1
    if n == 2:
        continue
    print(n)
print('循环结束。')
```
```python
#for in案例
for letter in 'runoob':
    if letter == 'b':
        break
    print('当前字母为：',letter)
```
```python
#while案例
var = 10
while var > 0:
    print('当前变量为：', var)
    var = var - 1
    if var == 5:
        break
print('good bye!')

```

## else子句
```python
for n in range(2,10):
    for x in range(2,n):
        if n%x == 0:
            print(n,'等于',x,'*',n//x)
    else:
        print(n,'是质数')
```
## 循环中的else
```python
#for else 、 while else
#下载一个视频，从0~100%，下载完成后，显示下载完成，否则不显示:用while else

i = 0
while i <= 100:
    if i == 60:
        print('下载非法文件，终止下载')
        i += 1
    print(f'下载进度：{i}%')
    i += 1
else:
    print('下载完成')
```
```python
#下载一个视频，从0~100%，下载完成后，显示下载完成，否则不显示：用for else

for i in range(0,101):
    if i == 60:
        print('下载非法文件，终止下载')
        continue
    print(f'下载进度：{i}%')
else:
    print('下载完成')
    
```

# 面向对象
```python
类(Class): 相同属性对象的集合，它定义了该集合中每个对象共有的属性和方法
方法：类中定义的函数
类变量、数据成员、方法重写、局部变量、实例变量、继承、实例化、对象

class myclass:
    i = 12345
    def f(self):
       return 'hello world'
x = myclass()
print('myclass的属性为：', x.i)
print('myclass的属性为：', x.f())
```

## init的用法
```python
class complex:
    def __init__(self,realpart,imagpart):
        self.r = realpart
        self.i = imagpart
x = complex(3.0, 4.5)
print(x.r,x.i)
#类的内部，def来定义一个构造方法，方法里面又必须包含self
class people:
    name=''
    age =0
    _weight = 0
    def __init__(self,n,a,w):
        self.name = n
        self. age = a
        self._weight = w
    def speak(self):
        print('%s说：我今年%d岁。' %(self.name , self.age) )
p = people('runoob',19,170)
p.speak()
#单继承
class people:
    name=''
    age = 0
    _weight = 0
    def __init__(self,n,a,w):
        self.name = n
        self. age = a
        self._weight = w

class student(people):
    grade = ''
    def __init__(self,n,a,w,g):
        people.__init__(self, n, a, w)
        self.grade= g
    def speak(self):
        print('%s说：我今年%d岁，我在读%g年级。' %(self.name , self.age,self.grade) )
s = student('Joe',30,170,4)
s.speak()

# 多继承
#父1
class people:
    name=''
    age =0
    _weight = 0
    def __init__(self,n,a,w):
        self.name = n
        self. age = a
        self._weight = w
#子1
class student(people):
    grade = ''
    def __init__(self,n,a,w,g):
        people.__init__(self, n, a, w)
        self.grade= g
#父2
class speaker():
    topic =''
    name =''
    def __init__(self,n,t):
        self.name = n
        self.topic = t
    def speak(self):
        print('我叫%s，我是一个演说家，我今天演讲的题目是%s。' %(self.name , self.topic) )
#多重混合
class sample(speaker,student):
    a=''
    def __init__(self,n,a,w,g,t):
        student.__init__(self, n, a, w, g)
        speaker.__init__(self,n,t)
test = sample('Joe',30,170,4,'python')
test.speak()

```
## 方法重写
```python
class parent:
    def mymethod(self):
        print('调用父类方法')
class child(parent):
    def mymethod(self):
        print('调用子分类方法')
c = child()
c.mymethod()
super(child,c).mymethod()
```
## 类属性和方法
```python
class justcounte:
    __secretcount = 0
    publiccount =0
    def count(self):
        self.__secretcount +=1
        self.publiccount +=1
        print(self.__secretcount)
counter = justcounte()
counter.count()
counter.count()
print(counter.publiccount)
print(counter.__secretcouont)
```

## 类的私有方法
```python
class site:
    def __init__(self,name,url):
        self.name = name
        self.__url=url
    def who(self):
        print('name；',self.name)
        print('url:',self.__url)
    def __foo(self):
        print('这是私有方法')
    def foo(self):
        print('这是共有方法')
        self.__foo()
x = site('菜鸟教程', 'www.runoob.com')
x.who()
x.foo()
x.__foo()
```

## 运算载重符
```python
class vector:
    def __init__(self,a,b):
        self.a=a
        self.b=b
    def __str__(self):
        return 'vector %d%d'%(self.a,self.b)
    def __add__(self, other):
        return vector(self.a + other.a,self.b + other.b)
v1 = vector(2,10)
v2 = vector(5,-2)
print(v1 + v2)
```

# 迭代器和生成器
```python
list= [1,2,3,4]
it = iter(list)
print(next(it))
```

## 迭代器用于for语句
```python
list = [1,2,3,4]
it = iter(list)
for x in it:
    print(x,end='')
```

## sys模块：从程序外部获取参数
```python
import sys
a = sys.argv[0]
print(a)
#sys.stdout与print
import sys
aa = sys.stdin.readline()
bb= input('请输入:')

sys.stdout.write(str(len(aa)) + '\n')

print(len(bb))
```

## next 函数
```python
import sys
list = [1,2,3,4]
it = iter(list)
while True:
    try:
        print(next(it))
    except StopIteration:
        sys.exit()
```

## 创建迭代器
```python
class mynumbers:
    def __iter__(self):
        self.a = 1
        return self
    def __next__(self):
        x = self.a
        self.a += 1
        return x
myclass = mynumbers()
myiter = iter(myclass)

print(next(myiter))
print(next(myiter))
print(next(myiter))
print(next(myiter))
print(next(myiter))
```
## StopIteration 结束迭代
```python
class mynumbers:
    def __iter__(self):
        self.a = 1
        return self
    def __next__(self):
        if self.a <= 20:
            x = self.a
            self.a += 1
            return x
        else:
            raise StopIteration
myclass = mynumbers()
myiter = iter(myclass)

for x in myiter:
    print(x)
```
## 生成器
```python
import sys
def fibonacci(n):
    a,b,counter = 0,1,0
    while True:
        if (counter > n):
            return
        yield  a
        a,b = b ,a+b
        counter +=1
f = fibonacci(10)
while True:
    try:
        print(next(f),end='')
    except StopIteration:
        sys.exit()
```

