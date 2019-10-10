# 第三课：BMI计算器--复杂的条件组合
![BMI计算器](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/BMI.jpg)
## 课程概括： 
> 通过BMI计算器，了解条件运算符，学会用编程思维解决数学问题

## 本节课涉及到的知识点、使用到的模块：
> 运算：条件运算符：与，或，不成立，需要检测多个时使用，可以检测复杂的条件组合  
![条件运算符](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/BMI_term.jpg)
        1）条件运算符的优先级要高于+-*/运算   
        2）a与b的判断条件需要两者都满足才能成立，a或b的判断条件只需要二者满足其一    
        3）如：18.5 < BMI < 23.9 BMI既大于18.5又小于23.9 ，所以需要使用"与"的判断 18.5 < BMI 与 BMI < 23.9
              小鱼不管是碰到1号鲨鱼还是2号鲨鱼都需要隐藏起来，所以需要使用"或"的判断 "碰到shark1" 或 "碰到shark2"
![与&&或](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/BMI_andor.jpg)
> 侦测：询问**并等待，会将询问结果返回到"回答"中

##其他小知识
> 关于BMI中国指数：偏瘦<= 18.4; 18.5 <= 正常 <= 23.9; 24<=过重<=27.9 ; 肥胖 >= 28 
``
## 开始练习    
### BMI计算器，认识编程如何解决数学问题
> 说明：配合计算器使用，理解运算符在程序中的使用
> 知识点：深入理解条件，运算符，额外处理例外情况和临界值  
> 示例地址：[BMI计算器：https://scratch.mit.edu/projects/321460387/editor](https://scratch.mit.edu/projects/321460387/editor "BMI计算器")       
           [BMI计算器-上课演示：https://scratch.mit.edu/projects/324124989/editor](https://scratch.mit.edu/projects/324124989/editor "BMI计算器") 

> 核心算法：体质指数(BMI)=体重(kg)/身高 (m)^2

> 步骤：
>> step1. 添加人物角色、背景  
 
>> step2. 询问用户身高、体重 
            1）添加"身高"、"体重"的变量，并设置初始值为0    
            2）询问**并等待，将"回答"赋给身高、体重   
![询问，将回答赋给变量](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/BMI_ask.jpg)     
         
>> step3. 计算BMI值   
            1）添加 BMI 变量   
            2）计算BMI = 体重(kg)/身高 (m) * 身高 (m)  并赋值给BMI变量    
![计算BMI值](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/BMI_count.jpg)            
>> step4. 添加提示判断，使用如果。。。那么 做以下4个条件判断  
            1）BMI < 18.5   
            2）BMI > 18.5 与 BMI < 23.9   
            3）BMI > 24 与 BMI < 27.9   
            4）BMI > 28   
![条件判断](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/BMI_condition1.jpg)


## 此示例扩展 ：例外处理
>> step5. 例外处理
>>>> 1）临界值处理：上节课只做了大致范围<18.4,>18.5这样的条件判断，所以18.4就是临界值，需要额外处理临界值     
![临界值处理](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/BMI_condition2.jpg)     

>>>> 2）例外处理：BMI指数适用于18-65岁，所以如果用户小于18岁，或者大于65岁，需要给出提示，停止程序   
  
## 孩子们出现的问题： 
>>1. Q:条件判断与和或搞不清
     A: 两者都需要满足的为"与"，二者满足其一的为"或"，如：  
     18.5 < BMI < 23.9 BMI既大于18.5又要小于23.9 ---"与"   
     小鱼不管是碰到1号鲨鱼或是2号鲨鱼 game over---"或"   
     
## 课后练习
[本节课后练习，几个简单的数学问题，试试看](exercise3.md)


