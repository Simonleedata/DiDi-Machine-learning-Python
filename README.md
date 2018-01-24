# DiDi-Machine-learning-Python
DiDi  ML  Learning groups Codes

# coding: utf-8

# <font size = 5>     汇报人：李琛（数据科学部-统计科学组-数据分析实习生） </font>

# <font size = 5> 2018.01.24 第一周 python 基本语法</font> 

# 
# 1. 基本语法</font>
#     -  基础对象
#     -  基本运算
#     -  控制流
#          - if判断语句
#          - while循环
#          - for循环
#     - 自定义函数
# 2. 数据结构
#     -  列表
#     -  字典
# 

# ## 基本语法

# ### 基础对象
int:   整数，如1, 2, 3
float: 浮点数，如2.3, 3.6
bool:  布尔值，包括True, False
str:   字符串，如'12.3', 'abcd' 特点：用单引号''或者""引起来的内容
python 中是大小写敏感的
单引号和双引号的作用是一样的，没有区别，但是不能够混合使用 如：('")
# In[1]:

1 + 2      #按shift + enter 键输出结果


# In[2]:

type(1)    #type()函数用于打印变量的类型


# In[3]:

type(2.1)


# In[4]:

print(type(2))
print(type(2.2))
print(type(True))
print(type("abcd"))     #print函数用于输出内容


# In[5]:

print("hello python")


# ### 基本运算

# In[6]:

10/3


# In[7]:

10 // 3 #求商的整数部分


# In[8]:

10 % 3 #求余运算


# In[9]:

5 ** 3 #幂运算


# In[10]:

get_ipython().magic(u'pinfo pow')


# In[11]:

pow(5,3)  #幂运算的另外一种写法


# In[12]:

25 ** 0.5   #可以利用幂运算开方


# In[13]:

pow(25,0.5)  #功能和上一条相同


# In[14]:

#比较大小的运算符，注意两个等号代表数学意义上的等号
print(1 > 1)
print(1 >= 1)
print(1 < 2)
print(1 <= 1)
print(1 == 1)
print(1 != 1)


# In[15]:

#逻辑运算符
print(True and False)    #逻辑与，只有当每个子表达式都为真时，整个表达式才为真
print(True or False)    #逻辑或  当子表达式中有一个为真时，整个表达式为真
print(not False)        #逻辑非 与子表达式相反


# In[16]:

x = 2
print(x >= 2 and x < 1)
print(x == 2 or x < 2)
print( not x == 1)


# ### 控制流

# #### if判断语句                       
python中用4个空格的缩进来表示代码的层级结构
if <condition>:
    do()
elif <condition>:
    do_other()
else:
    do_another() 
# In[17]:

a  = 0

if a > 0 :
    print("a大于0")
else :
    print("小于等于0")


# In[18]:

a  = 0.5

if a > 2 :
    print("大于2")
elif a > 1 :
    print("小于等于2，大于1")
elif a > 0 :
    print("a是正数， <=1")
else:
    print("小于等于0")


# #### while循环
while 循环


while <condition>:
    do()
    update_condition()


# In[19]:

#1 +2 +3 + 4 + 5 + ...+ 100

sum = 0
i = 1
while i <= 100:
    sum = sum + i
    i = i + 1#i+=1
print(sum)


# In[20]:

#计算100以内所有偶数的和

n = 2
sum = 0 

while n <= 100 :
    sum = sum + n 
    n = n + 2
print(sum)


# #### for 循环
-for 循环


for x in <iterator>:
    do()

# In[21]:

range(10)


# In[22]:

list(range(0,10))#range函数包含左边的数，不包含右边的数


# In[23]:

list(range(2,5))


# In[24]:

list(range(2,16,2))#表示等差数列，差为2，默认差为1


# In[25]:

# 1 + 2 + 3 + 4 + 5 + 。。。+100

sum = 0
for i in range(1,101):
    sum = sum + i
    
print(sum)


# In[26]:

for x in range(11):
    if (x % 2 == 0) and (x % 3 != 0):
        print(x)


# ### 自定义函数

# In[27]:

def pingfang(x) :
    pf = x * x
    return pf

print(pingfang(2))


# In[28]:

def area(r) : 
    area = 3.14 * r * r 
    return area

print(area(1))


# ## 数据结构
list(列表): 支持插入，索引，切片等
dict(字典): 无序的key－val健值对
# ### 列表

# #### 列表操作

# In[29]:

a = [1,2,4,6,2.1] #用中括号括起来代表列表
a


# In[30]:

b = ["a","g","c","r"]
b


# In[31]:

c = [1,"r",True] #list内元素支持不同类型的数据；
c


# In[32]:

d = [1,5,["f","h"]]
d


# In[33]:

print([a,b,c,d])#列表支持嵌套


# In[34]:

a.insert(3,"n")
a


# In[35]:

a.pop()
a


# In[36]:

a.append(9)
a


# In[37]:

#列表的索引和切片
lst = [1,5,7,9,["g","t","y"]]
lst[1]            #元素的序号从0开始！


# In[38]:

lst[4][1] #双重索引


# In[39]:

lst[1:4]#取出列表中位置1到位置4的元素，不包括位置4的元素


# In[40]:

lst[1:]#取出列表中位置1及其之后所有的元素


# In[41]:

lst[:4]#取出列表中位置4之前所有的元素（不包括位置4上的元素）


# #### 列表推导式

# In[42]:

#基于已有列表，创建新的列表
fb = [4,5,9,7,12,56]
[i + 1 for i in fb]


# In[43]:

new_lst = []
for i in fb :
    i = i + 1
    new_lst.append(i)
new_lst


# In[44]:

[i + 1 for i in fb if i % 3 ==0]#添加if判断语句，如果i能够被3整除，将i加1


# In[45]:

#与上一条语句功能相同
res = []
for i in fb : 
    if i % 3 ==0 :
        res.append(i + 1)
        
print(res)


# ### 字典

# In[46]:

dict = {} # 建立一个空的字典


# In[47]:

dict["地址"] = "研究生教学楼"


# In[48]:

dict #可以看出字典用花括号表示，属性—值的组合（key-values）


# In[49]:

someone = {'gender': 'male', 'height': 6.1, 'age': 30}#属性和值之间用冒号，键值对之间用逗号
print(someone)


# In[50]:

print(someone["gender"])#取出字典中的某个属性对应的值


# In[51]:

print(someone.keys())#打印列表中的属性（key）
print(someone.values())#打印列表中的值（values）

