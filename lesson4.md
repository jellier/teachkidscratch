# 第四课：青蛙捉虫子游戏：使用克隆增加游戏对象，重力在游戏中的使用，开发游戏思维

## 课程概括：   
> 通过青蛙捉虫子的游戏，了解克隆在游戏中的作用
>> 今天的概念有点难，讲了克隆，克隆体和原型的区别和关系，坐标轴。开始新的小游戏—青蛙吃虫子，游戏实现起来不难，但概念理解起来难，这也是图形化编程的优势所在，用直观的方式来理解抽象的概念

> 在青蛙捉虫子中加入重力，模拟真实世界中物体运动的轨迹

> 完善大鱼吃小鱼的克隆部分    
  
> 如何创作属于自己的游戏   

## 本节课涉及到的知识点、使用到的模块：
> 控制
>> 克隆：当需要很多角色的复制品时，克隆功能就非常有用。如生成很多小鱼。很多编程语言都允许你生成复制品，但他们都叫"对象"，如java,c++   
    "当做为克隆体启动时": 当一个克隆体诞生以后，会执行这个指令开始的一段脚本。克隆体不会执行这个角色原来的脚本，而是执行"当作为克隆体启动"下面的脚本  
    "克隆自己"：这个角色生成一个角色的克隆体，和原来的那个完全一样，它们出现在同样的位置，面向同样的方向，所以如果你不移动它，是看不到它的   
    "删除此克隆体" ：这个指令块会删除克隆体。当作品停止运行的时候，所有的克隆体都会消失，只有最初的那个角色留在舞台上

> 事件
>> 当按下"**"键，本节课示例是使用上下左右箭头来启动脚本   

> 运算：
>> 在*和*之间取随机数

## 其他小知识  
> 重力：真实世界中的重力：在真实世界中，当你试图沿直线抛出一个物体时，它总是会在重力的作用下画出一道落向地面的弧线。  
        斜抛运动的轨迹是抛物线。斜抛运动的加速度是重力加速度，所以斜抛运动是匀变速运动。-- 这种解释对于孩子太难理解了。    
        所以孩子们只要知道重力会影响物体的运动轨迹，运动轨迹取决于物体本身的重量和发射速度。      
        在本节课的示例中，物体重量是一定的，所以可以通过发射速度来控制运动轨迹（如何吃到虫子）  

> 随机数：[什么是随机数](https://www.6zou.net/docs/what_is_random.html "什么是随机数") 

> 坐标轴/直角坐标系
[直角坐标系](https://baike.baidu.com/item/%E7%9B%B4%E8%A7%92%E5%9D%90%E6%A0%87%E7%B3%BB/1835293)  
注意：坐标轴是是指一条带方向有刻度的直线.而坐标系则是指若干条坐标轴组成的若干维的空间.


## 开始练习    
### 弹射控制类游戏：青蛙捉虫子      
> 说明： 使用键盘上下箭头控制青蛙弹跳的方向，空格键控制发射，用尽量少的跳跃次数捕获更多的虫子   
> 知识点：键盘控制，复习广播，了解重力的概念        
        
> 示例地址：[青蛙捉虫子-上：https://scratch.mit.edu/projects/324177292/editor](https://scratch.mit.edu/projects/324177292/editor)    
> 示例地址：[青蛙捉虫子-中：https://scratch.mit.edu/projects/324174825/editor](https://scratch.mit.edu/projects/324174825/editor)  

> 步骤：
>> step1. 增加螳螂（初始化，克隆体初始化)    
![青蛙捉虫子-第一步-添加螳螂及克隆体](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/Frog1.jpg)
![螳螂的代码](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/Frog1_hopper.jpg)

>> step2. 添加青蛙（初始化，发射控制）和发射器（初始化，上下左右箭头控制）
![青蛙捉虫子-第二步-添加青蛙和发射控制](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/Frog2.jpg)   
![青蛙的代码](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/Frog2_frog.jpg)  

>> step3. 在螳螂的克隆体上增加触碰判断
![螳螂的代码](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/Frog2_hopper.jpg)

>> step4. 添加箭头角色作为发射器，上下左右箭头控制
![发射器的代码](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/Frog2_arrow.jpg)

>> step5. 添加game over的角色，发射次数变量（初始化，空格事件计数，接收广播显示）
![添加game over角色](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/Frog2_addgameover.jpg)
![game over的代码](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/Frog2_gameover.jpg)

>> step6. 收尾：game over时其他角色的处理：gameover显示，其他隐藏
 
## 此示例扩展 1： 增加障碍物   
> 示例地址：[青蛙捉虫子-下：https://scratch.mit.edu/projects/323834199/editor](https://scratch.mit.edu/projects/323834199/editor)   
> 说明：增加一颗小灌木，确保角色轻微偏离舞台中心，稍靠左侧，否则虫子可能会粘在树后，游戏永远也结束不了   
> 只需要在青蛙的代码中加入"或'碰到树'"的判断即可   
![青蛙捉虫子-添加障碍物-树](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/Frog3.jpg)   
![树的代码](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/Frog3_tree.jpg)
  
## 此示例扩展 2: 增加重力加速度（重力的理解较难）    
> 说明：增加了障碍物之后，青蛙撞到树后会停止飞行，这使得它无法抓到页面右侧的虫子，所以需要重力来帮忙   
> 步骤： 增加两个变量"重力"和 "下落速度"， 用于模拟重力加速度   
        在青蛙的初始化中增加变量"重力"的初始值（-0.2）-->   
        在青蛙的发射控制中（空格键触发）将"下落速度"设为0，表示在刚开始发射的时候青蛙还没有开始下落 -->    
        在发射控制的循环中将青蛙的y坐标增加"下落速度"，让青蛙（在循环中）不断下落，   
        同时将"下落速度"增加"重力"，让青蛙在每次循环之后加快下落速度    
![青蛙加了重力的代码](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/Frog3_frog.jpg)
  
> 备注：真实世界中的重力：在真实世界中，当你试图沿直线抛出一个物体时，它总是会在重力的作用下画出一道落向地面的弧线
        为了让游戏以同样的方式运行，我们让青蛙先沿着直线运动，但同时在它每次谓一致后添加一次向下的运动，这样就能模拟出持续不断的重力下拉效果。这样会让运动看起来更自然逼真。    
        


## 孩子们出现的问题：  
>>1. Q:坐标取值问题    
     A:坐标系理解起来有点难，所以当要求把虫子显示在页面右方时，还不能明白如何设定 X / Y 的取值范围，还需要加强坐标轴的练习。另外可以选择scratch自带的坐标系背景作为辅助，定位好角色后再把辅助背景删除
![添加坐标系背景作为辅助背景](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/Frog_xy.jpg) 
 ![可以在背景选项卡下看到添加的背景](https://raw.githubusercontent.com/jellier/teachkidscratch/master/thumb/Frog_addbg.jpg) 
 
>>2. Q: 搞不清楚代码该加到原型上还是克隆体上
     A: 需要理解克隆体和原型的关系，克隆体复制之前的代码加到原型上（如初始化，复制克隆体），对克隆出来的对象的操作放到""当作为克隆体启动时"下面。另外在克隆出新对象后可以把原型隐藏，统一处理克隆体比较简便

>>3. Q: 在前一天的作业中，让孩子们根据已经掌握的知识去把青蛙捉虫子的部分实现，今天完成度都很高，他们反馈的问题是：把控制发射方向的代码加在了箭头上，但应该发射的物体是青蛙，不知道如何让青蛙按照箭头的方向发射    
     A: 这一点之前确实没有讲过，我忽略了。应该用运动模块下的"面向***的方向"，把***设定为arrow的方向即可
   
>>4. Q: 通过青蛙捉虫子的学习已经掌握了克隆在游戏中的操作，所以要求他们把小鱼游戏改编成克隆版本，克隆出多条小鱼，每条小鱼碰到大鱼后都要被吃掉（隐藏或删除）      
     A:  在第一天的游戏中，几乎每个孩子都把对小鱼和大鱼的碰撞检测都直接放到了"当绿旗被点击"下， 而小鱼游动是一个持续的过程（循环），所以检测只在绿旗被点击后发生了一次，而小鱼一直在游动，导致游戏运行起来后大鱼碰撞到小鱼并不会消失 。今天把碰撞检测从绿旗点击挪到了克隆体启动时下面，又发生了同样的错误。因为大鱼小鱼持续在动，所以检测也需要时时监听。   

  
## 如何创作属于自己的游戏
> 通过学过的这几个游戏，给孩子们介绍了一下写游戏的方法（套路）： 
> 创作步骤：  
>> step1. 添加主要的角色（对象），对角色进行控制（键盘？鼠标？）   
>> step2. 添加目标（或敌人）：    
    1) 明确目的：chase? catch? reach?    
    2) 记分或计时...    
    3) 对敌人或目标控制：移动，隐藏，碰撞      
>> step3. 增加阻碍（也可以是更多的敌人）以增加难度：如墙壁，障碍物，或者不同方向/类型的敌人   
>> step4. 加速器/能量石：如主要角色碰到加速器可以让敌人统统消失或者能量翻倍，得分翻倍诸如此类      
>> step5. 游戏结束标志：game over提示     
>> step6. 思考还可以做什么：如片头说明提示，或者多个关卡，进入下一关    

> 希望孩子们可以创造出属于自己的游戏   
> 如果没有思路可以多逛逛社区： [scratch中文社区](https://scratch.mit.edu/discuss/17/)   
> 在社区里也可以看到别人的作品，充实思路的同时也在别人发生的错误上积累经验。社区是程序员成长的最好地方  


## 课后练习
> 到目前为止，你应该能独立设计、实现并优化一个游戏，以下示例可作为参考：  

>> [重力模拟](review1.md)

>> [星球大战游戏(一个完整的追逐躲避游戏)](exercise4.md)  

>> [控制指定克隆体](review2.md)

>> [打地鼠游戏(练习克隆)](lesson6.md)
