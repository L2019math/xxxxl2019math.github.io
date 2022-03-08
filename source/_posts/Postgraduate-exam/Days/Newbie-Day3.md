---
title: tourist 和 newbie 竞争的 Day3
date: 2022-02-18 17:05:40
categories: 研究生入学考试
tags: 每日打卡
cover: /img/tourist.jpg
---

## 每日打卡

If one does not know to which port one is sailing ,  no wind is favorite .

> 翻译见文末

## 算法学习

<p align="center"  style="color: green ">最长上升子序列模型</p>

LIS: longest increasing sequence

 最长上升子序列模型属于线性DP

> 接上文 [最长上升序列模型](https://www.selfknow.cn/Postgraduate-exam/Days/Newbie-Day1/)，继续熟练这个模型

### [最大上升子序列和](https://www.acwing.com/problem/content/1018/)

裸的最大上升子序列模型，且总和不会爆int

> 时间复杂度：O ($n^2$)

### [拦截导弹](https://www.acwing.com/problem/content/1012/)

第一问显然每套导弹拦截系统拦截导弹高度为不升子序列，求最长的就好了
第二问求导弹拦截系统的个数可以转化为求最长上升子序列长度
> 1、首先我们把这些导弹分为s组（s即为所求答案）
> 可以看出每一组都是一个不升子序列
> 2、划分完后我们在组一里找一个原序列里以组一的开头点连续的不升子串的最后一个元素，可以知道在组2中一定有一个大与它的点
> （如果组二中没有的话，那么组二中最高的导弹高度必然小于这个点，而其他的高度都小于这个高度而且是递减或相等的，那么没有必要再开一个组二了，矛盾，所以不存在找不到比他大的点的情况）
> 3、以此类推，对于每一个k组（1<=k<n）都可以找到这样的一些点
> 所以把这些点连起来，就是一条上升子序列。
> 4、设最长上升子序列长度为l
> 所求上升子序列为h
> 那么h<=l
> 因为最长上升子序列任意两个不在一组内
> (如果在同一个组内，则每个组的数不成为一个不生子序列，矛盾）
> 所以l==h
>
> 比较难理解
> 我们来看组数据
> 389 207 155 300 299 170 158 65
> 组一 389 207 155 65 组二 300 299 170 158
> 步骤一中我们一开始找到的点是1
> 因为如果找65不好解释，所以我们找原数列里连续的最后一个即155
> 组二里可以找到300比他大
> 所以最长上升子序列长度为2==答案
>
> 作者：空空如也
> 链接：https://www.acwing.com/solution/content/10173/
> 来源：AcWing
> 著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

题目的第二问，对于第i号导弹，要么选择末尾导弹高度最小的拦截系统，要么新创一个拦截系统，用一个数字即每套拦截系统此时所拦截的最后一个导弹高度，来表示该系统。
这样就得到了一个数组，数组最终长度就是所需最少拦截系统数目。

```c++
// 贪心代码

//数组g的每个元素代表一套导弹拦截系统的拦截序列
//g[i]表示此时第i套导弹拦截系统所拦截的最后一个导弹的高度
int p = lower_bound(g, g+cnt, a[i]) - g;
if(p == cnt) g[cnt ++] = a[i];  //a[i]开创一套新拦截系统    
else g[p] = a[i];               //a[i]成为第p套拦截系统最后一个导弹高度
```



### upper_bound与lower_bound

若数组升序排列
`lower_bound(begin, end, a)` 返回数组[begin, end)之间第一个大于或等于a的地址，找不到返回end ~~（可以等于所以low）~~
`upper_bound(begin, end, a) `返回数组[begin, end)之间第一个大于a的地址，找不到返回end ~~（一定大于所以up）~~

若数组降序排列，可写上比较函数`greater<type>()`
`lower_bound(begin, end, a, greater<int>()) `返回数组[begin, end)之间第一个小于或等于a的地址，找不到返回end
`upper_bound(begin, end, a, greater<int>()) `返回数组[begin, end)之间第一个小于a的地址，找不到返回end

---

如果你不知道要驶向那个港口，任何风向都毫无助益。
