# 第一课：初步认识scrach 

## 课程概括：
> scrach简介及社区初步认识    
> 认识(编辑)舞台角色，声音 / 认识指令和序列 / 认识变量

## 本节课使用到的模块：
> 控制
>> 循环：当有模块需要重复执行时，使用循环更简洁。循环就是一部分不断重复的代码。
        "重复执行"指令块创建了一个永远运行下去的循环，而其他类型的循环可以按照规定次数重复某个动作  
        举例：吃饭的时候，一直不停的吃就是一种循环
>> 条件： 如果。。。那么
        举例：如果饭熟了，那么回家吃饭 

> 事件：计算机检测到的按下键盘或者点击鼠标的行为叫"事件"   
>> 起始事件：绿旗   
>> 鼠标点击触发事件   
>> 键盘触发事件   

> 变量：变量是一个盒子，可以放任何东西，放进去的东西也可以随时变化

> 运动：移动/左右转/碰到边缘反弹

> 侦测：碰到"鼠标指针"（其他角色）

## 开始练习
### 例子1：小鱼水中游    
> 说明：大海里一条小鱼在游来游去，遇到边缘返回   
> 知识点：认识舞台，背景，角色，编辑角色，触发事件，forever循环 ，不同频率的重复的动作使用多个循环同步     
> 示例地址：[小鱼水中游](https://scratch.mit.edu/projects/321283450/editor "最简单的循环")
![小鱼水中游](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/fishSwim.jpg)
> 步骤：
>> step1. 加入场景（大海），角色（小鱼） 
![选择场景、角色](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/fishSwim_choose.jpg)     
>> step2. 给角色加上代码   
        1）加入小鱼的动作：让角色移动10步/碰到边缘反弹/将旋转方式设为左右翻转/下一个造型，加入到循环中，讲解循环              
        2）模拟小鱼的真实效果：   
            a）给游动加入时间间隔，模拟真实游动效果    
            b）起浮，加入右转代码，不同频率的动作需要加入另外的循环  
            c）声音，小鱼游动时吐泡泡的声音    
![小鱼的代码](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/fishSwim_code.jpg)        

 
> 此示例扩展1：大鱼吃小鱼   
> 说明：想让游戏有趣，一定要增加一个敌人。给游戏加入一条鲨鱼，当鲨鱼碰到小鱼的时候，小鱼发出"啊"的惨叫，被鲨鱼吃掉 
![大鱼吃小鱼](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/EatFish1.jpg)   
>> step3. 增加敌人：一条鲨鱼    
        1）加入一个新角色：鲨鱼    
        2）给鲨鱼加上游动的代码（可参考小鱼的，但频率要快一些）   
![鲨鱼的代码](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/EatFish1_shark.jpg) 
>> step4. 给小鱼添加碰撞侦测     
> 示例地址：[大鱼吃小鱼](https://scratch.mit.edu/projects/324020784/editor "加入敌人")    
![小鱼的代码](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/EatFish1_fish.jpg)

> 此示例扩展2（作业）：增加多个敌人   
> 说明：增加多个敌人  
> 示例地址：[大鱼吃小鱼2](https://scratch.mit.edu/projects/324022543/editor "加入多个敌人")  
![增加多个敌人](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/EatFish2.jpg)

>> step5. 增加敌人：另一条鲨鱼    
        1）直接在鲨鱼上点右键复制    
        2）给shark2修改游动频率和游动方向 
![复制一条鲨鱼](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/EatFish2_copy.jpg)
![修改第二条鲨鱼的游动频率和方向](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/EatFish2_shark2.jpg)

>> step6. 给小鱼的碰撞侦测上添加"或"条件    
![修改小鱼的碰撞侦测条件](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/EatFish2_fish.jpg)


## 孩子们出现的问题：  
>>1. 刚开始让小鱼移动的时候没有加上循环，到后面加入鲨鱼的时候就知道把代码放入循环了    
>>2. Q:刚加入碰撞检测时，大鱼小鱼即使相遇，小鱼也没有消失   
     A:碰撞检测是在绿旗启动后的条件代码块中， 只是在绿旗点击后执行了一次，而角色的其他代码是一直在运行的，所以当小鱼碰到大鱼时碰撞检测已经执行完成了，就不再触发了，所以要把碰撞检测也放到循环中，让代码一直执行起来      
>>3. Q:小鱼碰到大鱼后，需要隐藏起来，但当再次启动程序时，小鱼仍然是隐藏状态   
     A:所以要在小鱼的绿旗点击事件后加上初始化代码：显示     

        

## 课后练习
[本节课后练习，几个简单的小游戏，可以试着做一下](exercise1.md)


 


