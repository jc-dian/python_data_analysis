# SVM

<img src="SVM.assets/image-20210203210139902.png" alt="image-20210203210139902" style="zoom:50%;" />

## 6.1 间隔与支持向量

<img src="SVM.assets/image-20210203204247065.png" alt="image-20210203204247065" style="zoom:67%;" />

在样本空间中，划分超平面可通过如下线性方程来描述：

<img src="SVM.assets/image-20210203210352505.png" alt="image-20210203210352505" style="zoom:80%;" />

​        其中 **w** = （w1；w2,；...wd)为法向量，决定了超平面的方向；b为位移项，决定了超平面与原点之间的距离。显然，划分超平面可被法向量w和位移b确定，下面我们将其记为（w，b）。样本空间中任意点x到超平面（w，b）的距离可写为

<img src="SVM.assets/image-20210203210950011.png" alt="image-20210203210950011" style="zoom:80%;" />

<!--通过上面ppt图可以看出怎么推出来的-->

<img src="SVM.assets/image-20210203212154875.png" alt="image-20210203212154875" style="zoom:80%;" />

如图6.2所示，距离超平面最近的这几个训练样本点（6.3）的等号成立，它们被称为“支持向量”（support vecotr），两个**异类**（一正一负）支持向量到超平面的距离之和为

<img src="SVM.assets/image-20210203212335818.png" alt="image-20210203212335818" style="zoom: 80%;" />

它被称为“间隔”（margin）

欲找到具有“最大间隔”（maximum agrgin）的划分超平面，也就是要找到能满足式（6.3）中约束的参数w和b，使得y最大，即

<img src="SVM.assets/image-20210203213437317.png" alt="image-20210203213437317" style="zoom:80%;" />

<img src="SVM.assets/image-20210203213454481.png" alt="image-20210203213454481" style="zoom:80%;" />

这就是支持向量机（Support Vector Machine，简称SVM）的基础型。

## 6.2 对偶问题

<img src="SVM.assets/image-20210203214058780.png" alt="image-20210203214058780" style="zoom:80%;" />

<!--详细公式参考《西瓜书》pdf第123页-->

<img src="SVM.assets/image-20210203214239015.png" alt="image-20210203214239015" style="zoom:80%;" />

## 6.3 核函数

<img src="SVM.assets/image-20210203215049493.png" alt="image-20210203215049493" style="zoom:80%;" />

![image-20210203215437454](SVM.assets/image-20210203215437454.png)

<img src="SVM.assets/image-20210203215342215.png" alt="image-20210203215342215" style="zoom:80%;" />

### 几种常用核函数

![image-20210203215537764](SVM.assets/image-20210203215537764.png)

## 6.4 软间隔与正则化

![image-20210203215729272](SVM.assets/image-20210203215729272.png)

缓解该问题(线性不可分)的一个方法是**允许支持向量机在一些样本上出错**，为此，要引入“软间隔”（soft margin）的概念，如图6.4所示。

![image-20210203220140493](SVM.assets/image-20210203220140493.png)

这就是常用的“软间隔支持向量机”

## 6.5 支持向量回归

![image-20210203220604960](SVM.assets/image-20210203220604960.png)

## 6.6 核方法

![image-20210203220710050](SVM.assets/image-20210203220710050.png)

参考林轩田《机器学习技法》，SVM这部分的推导讲得很清楚；或者参考https://blog.csdn.net/abcjennifer/article/details/7849812/）

《机器学习技法》第1课笔记 线性SVMhttps://blog.csdn.net/u013382288/article/details/80978410

《深度之眼》