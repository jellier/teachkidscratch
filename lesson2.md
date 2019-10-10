# 第二课：小鱼水中游 使用变量、广播

## 课程概括：
> 通过对上一节课小鱼游戏的扩展了解广播的机制，学会添加文字角色

 
## 本节课涉及到的知识点、使用到的模块：
> 控制
>> 停止全部脚本：在广播game over后 需要让页面上所有的脚本停止下来，使用此命令  

> 事件
>> 广播：1）广播是一对多使用的，一个发送端，多个接收端；发送端和接收端的消息要一样，才能执行程序   
        2）举例理解"广播"：在学校中我们经常听到喇叭里的广播，跟着广播我们每天做“广播体操”，在做“广播体操”时，喇叭中发出的广播就像是指令一样，所有人需要按照这些指令来完成动作。    
        3）scratch中的广播功能，可以在“事件”分类中找到它们：     
        其中一共有3个模块：当接收到广播、广播一个消息、广播一个消息并等待    


## 小鱼水中游的扩展        
### 此示例扩展2：增加多个敌人   
> 说明：增加游戏的趣味性，可添加多个敌人  
> 示例地址：[大鱼吃小鱼2：https://scratch.mit.edu/projects/324022543/editor](https://scratch.mit.edu/projects/324022543/editor "加入多个敌人")  
![增加多个敌人](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/EatFish2.jpg)

>> step5. 增加敌人：另一条鲨鱼    
        1）直接在鲨鱼上点右键复制    
        2）给shark2修改游动频率和游动方向 
![复制一条鲨鱼](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/EatFish2_copy.jpg)
![修改第二条鲨鱼的游动频率和方向](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/EatFish2_shark2.jpg)

>> step6. 给小鱼的碰撞侦测上添加"或"条件    
![修改小鱼的碰撞侦测条件](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/EatFish2_fish.jpg)


   
### 此示例扩展3：增加game over提示   
> 说明：当小鱼被大鱼吃掉，广播"game over"，鲨鱼接收到game over 广播后隐藏，文字game over接收到广播后显示   
> 知识点：广播 添加文字角色    
> 示例地址：[大鱼吃小鱼3：https://scratch.mit.edu/projects/324056921/editor](https://scratch.mit.edu/projects/324056921/editor "加入广播")  
![增加game over](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/EatFish3.jpg)

>> step7. 添加文字角色game over
         1）在"选择一个角色"的按钮上点"绘制"   
         2）选择文字工具，输入game over,调整大小   
         3）给game over加上代码："当绿旗被点击" 隐藏，"当接收到game over" 显示  
![选择"绘制"](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/EatFish3_text.jpg)
![选择文字工具输入"game over"](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/EatFish3_text2.jpg)
![调整文字大小](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/EatFish3_text3.jpg)

![给"game over"添加代码](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/EatFish3_gameover.jpg)
 
>> step8. 在小鱼的脚本上，被大鱼吃掉隐藏后面加上广播game over,并且停止全部脚本  
![给小鱼加上广播](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/EatFish3_fish.jpg)

>> step9. 在两只鲨鱼的脚本上添加"当接收到game over" 隐藏，并且在绿旗点击时显示   
![给鲨鱼加上接收广播](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/EatFish3_shark.jpg)


## 孩子们出现的问题：  
>>1. Q:小鱼游戏里广播不知道该加在哪个角色上，
     A:如果游戏里有一对多的角色，那就添加到唯一的那个角色上,因为广播的机制就是一对多，发送广播的只能是一个对象，但接收方可以很多
>>2. Q:多条鲨鱼或者多条小鱼时，会给每条小鱼/鲨鱼加上同样的代码，一旦添加新代码或者修改原有代码，总会有漏掉的
     A:判断条件里加上"与""或"，减少重复代码
     
## 课后练习
[本节课后练习，几个简单的小游戏，可以试着做一下](exercise1.md)