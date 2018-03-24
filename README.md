# InterviewSummary

Fighting for  a good result         
## 逻辑推理
有20个自然数1-20.每次取两个数字,取出不放回，其中一个数字是另一个数字2倍多。则最多取出来（）个数字。
答案有18,16,14,12，应该选18          
解析举例：
考虑最大,则考虑极限
9 -- 20
8 -- 19
7 -- 18
6 -- 17
5 -- 16
4 -- 15
3 -- 14
2 -- 13
1 -- 12
或者         
 1  10
 2  11
 3  12
 4  13
 5  14
 6  15
 7  16
 8   17
 9   19
共18个

## 组合
### 插板法：
有 10 粒糖，如果每天至少吃一粒（多不限），吃完为止，求有多少种不同吃法？（ ）
答案是C
         根据题意可知，此题满足插板法的应用条件：所有元素无差别，每份至少包含一个元素（每天至少吃一粒），因此考虑采用插板法求解。将10粒糖并列一排放置，中间形成9个空位，在这9个空位中任意插入0，-，9个隔板，（即表示10粒糖在1到10天吃完），故共有，即C为512种吃法。因此，选C
         
C(0,9)+C(1,9)+C(2,9)+...+C(9,9) = 512

### 三集合容斥原理 
AUBUC=A+B+C-A交B-B交C-A交C+A交B交C
例题
参加支付宝夜谈分享的同学共有50人，现设有甲、乙、丙三个夜谈主题。有40人选择参加甲夜谈主题，36人选选择参加乙夜谈主题，30人选择参加丙夜谈主题，兼选甲乙夜谈主题的有28人，兼选甲丙夜谈主题的有26人，兼选乙丙两门夜谈主题的有24人，甲乙丙三个夜谈主题均选的有20人，问三个夜谈主题未选的有多少人？( 2)


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
