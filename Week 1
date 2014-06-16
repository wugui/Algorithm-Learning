Week 1
=============

本课程会提供设计好的Java库和代码。

概论
-------------
·几个概念，几位先驱
·运行时间：这一概念的理解要追溯到查尔斯·巴贝奇，计算机之父。
·离散傅立叶变换：数学王子高斯。
·N体问题模拟：Andrew Appel。
·另外，增长级是最基础的概念。

几个问题
3-SUM问题：给定一个数组，有多少种三个数相加为零的情况？
以最笨拙的三层循环穷举法为例进行算法分析
观察算法运行时间可以采取对数函数图（去除指数的陡峭性）
二分查找
比较典型的用递归公式分析，可引出分治算法运行时间的基本定理

基本的数据类型大小
bit为0或1；byte为8bits；32bits、64bits以bit来衡量；MB、GB以byte来衡量；
（Java中的）boolean为1byte；byte为1byte；char为2bytes；int为4bytes；float为4bytes；long为8bytes；double为8bytes；数组另外加24bytes；二维数组近似为数组大小相关；
Java中的内存术语（例子：一个类的大小）：
Object overhead：16bytes
Reference：8bytes
Padding：补足整个数据结构的大小到8bytes的倍数

Dynamic Connectivity
第一周举的具体例子主要是针对图论的Dynamic Connectivity（动态连接？）
要做到能够动态地连接两个点
能够动态地检测两个点是否连通
API：int union(int p, int q); boolean connected(int p, int q)

Quick-Find
对于图中的边，把起点及其子节点的根节点设为终点的根节点；要看两个点是否连通，只需比较二者根节点是否相同即可
这样可想而知，union时每一步要设置的节点数可能会很多；但find很快
各项操作耗时：initialize:N；union:N；find:1

Quick-Union
相比于上一个方法，要把起点的根节点的父节点置为终点的根节点；这时判断两点是否连通，要层层向上取父节点，直到根节点，比较
不做改进的话有可能树的高度会很高；这也是下一个方法的由来
各项操作耗时：initialize:N;union:N;find:N（union的耗时应当还是比Quick-Find少）

Weighted Quick-Union
对Quick-Union做改进在union之前，先比较起点所在树和终点所在树的高度，然后较矮树的根节点加到较高树的根节点，这样能降低最后生成树的高度
各项操作耗时：initialize:N;union:log N;find:log N

Quick-Union和Weighted Quich-Union两种方法构造的树高度比较：
