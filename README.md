# InterviewSummary

Fighting for  a good result         
# 智力题
## 逻辑推理
有20个自然数1-20.每次取两个数字,取出不放回，其中一个数字是另一个数字2倍多。则最多取出来（）个数字。                
答案有18,16,14,12，应该选18                                      
解析举例：                    
考虑最大,则考虑极限</br>
9 -- 20</br>
8 -- 19</br>
7 -- 18</br>
6 -- 17</br>
5 -- 16</br>
4 -- 15</br>
3 -- 14</br>
2 -- 13</br>
1 -- 12</br>                       
或者</br>                                    
1  10</br>
 2  11</br>
 3  12</br>
 4  13</br>
 5  14</br>
 6  15</br>
 7  16</br>
 8   17</br>
 9   19</br>
共18个</br>

## 组合
### 插板法：
有 10 粒糖，如果每天至少吃一粒（多不限），吃完为止，求有多少种不同吃法？（ ）</br>
解析：根据题意可知，此题满足插板法的应用条件：所有元素无差别，每份至少包含一个元素（每天至少吃一粒），因此考虑采用插板法求解。将10粒糖并列一排放置，中间形成9个空位，在这9个空位中任意插入0，-，9个隔板，（即表示10粒糖在1到10天吃完），故共有，即C为512种吃法。因此，选C</br>
         
C(0,9)+C(1,9)+C(2,9)+...+C(9,9) = 512</br>

# 概率论 （《概率论与数理统计》 主编 金大勇 徐永）
## 1.2.3 概率的性质         
加法定理  A,B是任意两个事件，则P（AUB）=P（A）+P（B）-P（AB） </br>
         A,B是任意两个事件，则P（A-B）=P（A非B）=P（A）-P（AB） </br>    
## 1.3 古典概型（抽球！）


## 1.4 条件概率

定义1.4 A，B是两个事件，且P（A）>0，称P(AB)/P(A)为在事件A发生的条件下事件B发生的*条件概率*，记为P(B|A),即有 P(B|A)=P(AB)/P(A)</br>
条件概率也满足 </br>
- P（（~B）|A）=1-P（B|A）</br>
- P((B1UB2)|A)=P(B1|A)+P(B2|A)-P[(B1B2)|A]
- 当B属于C时，P[(C-B)|A] =P(C|A)-P(B|A)

典型考题：考察一个有两个小孩的家庭，假如已看见该家庭中的一个小孩是男孩，问另一个小孩也是男孩的概率是多大（假设另一个小孩是男孩还是女孩是等可能的）   
设A：已看见一个是男孩 A={(男，女),(女，男),(男，男)} B=另一个小孩是男孩 AB={(男，男)}            
P(A)=3/4 P(AB)=1/4
P(B|A)=P(AB)/P(A)=(1/4) /  (3/4) =1/3


## 几何概型（画图求阴影面积！）
在区间[-2, 2]里任取两个实数，它们的和>1的概率是(9/32)</br>
解析：
画直角坐标系，x和y的取值范围都在[-2,2]，所以是一个面积为4 * 4=16的正方形</br>
画x+y=1,即y=-x+1的直线，与正方形相交于(-1,3)和(2,-1)，所以线与正方形围城一个面积为3 * 3 * 0.5=4.5的三角形</br>
所以概率为4.5/16=9/32</br>



## 期望 和 方差 
例题1：若ξ，η相互独立且同服从分布N(0，1) ，Z=ξ+2η，则（ ）</br>
<font face="黑体">由题意知 E（ξ+2η）=E（ξ）+2E（η）=0+2*0=0</br>
        D(ξ+2η)=D（ξ）+2的平方 * D（η）1+4 * 1=5</br>
所以：E(z)=0,D（z）=5,Z~N(0,5)
注明： N（0,1）的N 表示正态分布，0是均值，1是方差
例题2：
若ξ~N(0，1),η=2ξ+1，则η~（  1,4  ）</br>
由题意知： E(η)=2E(ξ)+1=2 * 0+1=1              
          D(η)=2的平方D(ξ)=4 * 1=4</font >


## 三集合容斥原理 
AUBUC=A+B+C-A交B-B交C-A交C+A交B交C </br>  
例题：参加支付宝夜谈分享的同学共有50人，现设有甲、乙、丙三个夜谈主题。有40人选择参加甲夜谈主题，36人选选择参加乙夜谈主题，30人选择参加丙夜谈主题，兼选甲乙夜谈主题的有28人，兼选甲丙夜谈主题的有26人，兼选乙丙两门夜谈主题的有24人，甲乙丙三个夜谈主题均选的有20人，问三个夜谈主题未选的有多少人？( 2)</br>




例题：假设一段公路上，1小时内有汽车经过的概率为96%，那么，30分钟内有汽车经过的概率为?</br> 
解析：一小时有车的概率 = 1 - 一小时没车的概率 = 1 - 两个半小时都没车的概率 = 1 - （1 - 半小时有车的概率）^2 </br> 
1-(1-x)^2=0.96</br> 
x = 0.8</br> 


## 编译原理
编译原理流程：
源程序->词法分析->语法分析->语义分析->中间代码生成->代码优化->目标代码生成->目标代码
参见： http://www.docin.com/p-752401947.html
      https://baike.baidu.com/item/%E7%BC%96%E8%AF%91

（单选）以下说法错误的是        
A.在数中出现非数字字符属于词法分析 （对的）            
B.数组下标越界属于语义分析 （数组下标越界属于运行时或语义分析）                
C.目标语言书写的程序称为目标程序 （没有目标语言）                   
D.一颗分析树可对应多个记号串（一个串的分析树，对应着多个串的推导；推导不能唯一地表示串结构，而分析树可以）

个人感觉A和B肯定对，C和D不确定，C更不对             
解析C：                    
目标代码                  
目标代码生成是编译的最后一个阶段。目标代码生成器把语法分析后或优化后的中间代码变换成目标代码。目标代码有三种形式：
① 可以立即执行的机器语言代码，所有地址都重定位；
② 待装配的机器语言模块，当需要执行时，由连接装入程序把它们和某些运行程序连接起来，转换成能执行的机器语言代码；
③ 汇编语言代码，须经过汇编程序汇编后，成为可执行的机器语言代码。
目标代码生成阶段应考虑直接影响到目标代码速度的三个问题：一是如何生成较短的目标代码；二是如何充分利用计算机中的寄存器，减少目标代码访问存储单元的次数；三是如何充分利用计算机指令系统的特点，以提高目标代码的质量。
解析D：
https://wenku.baidu.com/view/e4e074bec77da26925c5b02d.html


# 软件结构
## 软件结构图的宽度
    考点：理解成树的宽度，按最宽的一行的宽度就是软件结构图的宽度
    
    
# 数据结构
## （多选）有关哈夫曼树的叙述中正确的是（）                
A.哈夫曼树中没有度数为1的分支结点（对）            
B.在哈夫曼树中，权值越大的叶结点离根越近（对）             
C.哈夫曼树可以用于通信编码（对）                 
D.在哈夫曼树中，权值越大的叶结点离根越远（错）  

哈夫曼树：
<li>哈夫曼树是一种带权路径长度最短的二叉树，也称为最优二叉树。
<li>编码时左零右一
<li>记住，设计电文总长最短的二进制前缀编码，就是以n个字符出现的频率作为权构造一棵哈夫曼树，由哈夫曼树求得的编码就是哈夫曼编码。
参考：https://blog.csdn.net/wo16fafafa/article/details/52420007
解析：A.证明：由赫夫曼树的构造过程可知，赫夫曼树的每一分支结点都是由两棵子树合并产生的新结点，其度必为2，所以赫夫曼树中不存在度为1的结点。

# 计算机网络 
## TCP 的 三次握手和 四次挥手 
详见 https://github.com/CyC2018/Interview-Notebook/blob/master/notes/%E8%AE%A1%E7%AE%97%E6%9C%BA%E7%BD%91%E7%BB%9C.md
# 机器学习

## 数据归一化
### Decimal scaling小数定标标准化
这种方法通过移动数据的小数点位置来进行标准化。小数点移动多少位取决于属性A的取值中的最大绝对值。将属性A的原始值x使用decimal scaling标准化到x'的计算方法是：
                                   x'=x/(10*j)
    其中，j是满足条件的最小整数。

例1： 假定A的值由-986到917，A的最大绝对值为986，为使用小数定标标准化，我们用1000（即，j=3）除以每个值，这样，-986被规范化为-0.986。
     注意，标准化会对原始数据做出改变，因此需要保存所使用的标准化方法的参数，以便对后续的数据进行统一的标准化。
     
例2： 属性值A取值在-86到917之间，使用小数定标标准化。A值35变化为 _0.035____
      最大值917，使用1000即j=3去标准化，所以小数点左移3位
## 神经网络
### 权值共享 
（单选）以下哪些神经网络结构中采用了 B
A.全连接神经网络      
B.卷积神经网络（就是CNN）         
C.CNN和RNN               
D.递归神经网络（就是RNN）

解析：
所谓的权值共享就是说，给一张输入图片，用一个filter去扫描这张图片，filter里面的数就叫权重，这张图每个位置是被同样的filter扫的，所以权重是一样的，即权值共享。         
详见https://www.zhihu.com/question/47158818?from=profile_question_card

（单选）在CNN中使用1*1的卷积核，以下表述正确的是：
A.用于特征池化
B.都对
C.有利于降维
D.过拟合几率更低
### 表示学习
（单选）以下哪一个是“表示学习”的算法？       
A.K近邻
<font color=red size=5>B.神经网络</font>
C.都不是
D.随机森林

解读：
https://zhuanlan.zhihu.com/p/27345918
表示（表达）学习（Representation Learning）是什么？为什么表示的概念有助于深度学习框架的设计？
表示学习，又称学习表示。在深度学习领域内，表示是指通过模型的参数，采用何种形式、何种方式来表示模型的输入观测样本X。表示学习指学习对观测样本X有效的表示。            
表示学习有很多种形式，比如CNN参数的有监督训练是一种有监督的表示学习形式，对自动编码器和限制玻尔兹曼机参数的无监督预训练是一种无监督的表示学习形式，对DBN参数-先进性无监督预训练，再进行有监督fine-tuning-是一种半监督的共享表示学习形式。              
表示学习中最关键的问题是：如何评价一个表示比另一个表示更好？表示的选择通常通常取决于随后的学习任务，即一个好的表示应该使随后的任务的学习变得更容易。以基于CNN的图像分类任务为例。模型可以分为基于CNN的特征抽取和基于softmax回归的线性分类两个部分。通过模型参数有监督的训练，通过CNN，从线性不可分的图片里抽取出线性可分表示（特征），softmax线性分类器可以基于抽取的线性可分的表示进行分类。

总之，表示学习就和神经网络连接起来!
