# 第五课：打印乘法口诀表
![打印乘法口诀表](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/MultiTable.jpg)   

## 课程概括：   
> 认识列表（数组），使用嵌套循环实现乘法口诀的打印，打印过程中学习连接字符串

## 知识点：数组，字符串的使用，嵌套循环
#### 数组
> 数组也是变量的一种，但是是一组变量，相当于一个队列，用来存放同一类的变量
> 举个例子吧，比如今天天气如何？晴天？阴天？多云？雷阵雨？等等，这些就可以看成一组变量，因为都是描述天气的。再比如今天是星期几？周一到周日，7个变量，也可以看成有关周几的一组变量。
> 在乘法口诀表这个示例中，我们要用到这种极为有用的数据结构

> 在Scratch中数组叫"列表"
> 建立一个列表（数组）

点击"变量"--"建立一个列表"：
![建立一个列表](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/MultiTable_addnew.jpg)    

在弹出框中输入列表的名称：
![建立一个列表](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/MultiTable_new.jpg)      

确定后，变量功能中会出现以下功能：
![建立一个列表](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/MultiTable_listmethod.jpg)  
    
舞台上显示刚刚创建的列表，点击右下角的加号，可以添加列表项
![建立一个列表](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/MultiTable_additem.jpg)

#### 字符串：
> 字符串是由数字、字母、下划线组成的一串字符，它是编程语言中表示文本的数据类型。
> 通常以串的整体作为操作对象，如：连接两个或多个字符串、在串中查找某个字符、求取字符串长度等。  
> 在Scratch中对字符串操作的功能在"运算"模块中
![字符串的操作](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/MultiTable_string.jpg)


## 开始练习：
### 数组的使用：打印乘法口诀表    
> 说明：点击绿旗，开始逐行打印乘法口诀    
> 知识点：数组，字符串的使用，嵌套循环     
> 示例地址：[打印乘法口诀表：https://scratch.mit.edu/projects/321784470/editor](https://scratch.mit.edu/projects/321784470/editor)   

> 步骤：
>> step1. 添加人物角色，在人物上添加代码，当绿旗被点击，说"现在开始背乘法口诀"
>> step2. 添加一个列表"乘法口诀表"， 让列表显示在舞台上；添加三个变量"乘数"、"被乘数"、"当前口诀"，不要勾选变量前的方框，这几个变量不需要显示在舞台上。变量初始化：
![变量初始化](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/MultiTable_init.jpg)

>> step3. 因为乘数是从1--9，每一行的乘数相同，所以外循环需要循环9次，每次乘数加1，每次更新第"乘数"项（行）的口诀；
          在每一次内循环中更新第"乘数"项（行）的口诀，被乘数都是从1开始，每次被乘数加1，直到被乘数>乘数；
          注意字符串的显示处理（见下图）
![循环](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/MultiTable_loop.jpg)



## 遇到的问题：  
>>1. Q: 如何在Scratch中显示比较复杂的字符串         
     A: Scratch中处理字符的功能比较简单，所以使用起来就比较麻烦。没有如python中的print或者js中的alert功能，比如想输出一个6 * 3 =18，需要将 "6"，"3"，"*","=","18" 作为5个字符拼接起来，而在其他编程语言中，可以直接print(6*3)
 
 ![当前口诀](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/MultiTable_now.jpg)

    
     

