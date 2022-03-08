---
title: tourist 和 newbie 竞争的 Day1
date: 2022-02-16 21:29:45
categories: 研究生入学考试
tags: 每日打卡
cover: /img/tourist.jpg
---

## 每日打卡

All of us , at certain moments of our lives , need to take advice and to receive help from other people .

> 翻译见文末

## 算法学习

<p align="center"  style="color: green ">最长上升子序列模型</p>

LIS: longest increasing sequence

 最长上升子序列模型属于线性DP

### 闫式DP分析法

$$
DP
\begin{cases} 
状态表示f[i]
	\begin{cases} 集合：所有以a[i]结尾的严格单调上升子序列
    \\ \\
    属性：Max/Min/数量
    \end{cases}
\\ \\
状态计算--集合的划分：依据最后一个不同的状态
\end{cases} 
$$



### [怪盗基德的滑翔翼](https://www.acwing.com/problem/content/1019/)

#### 题目分析

1. 只能选一个方向且中途不能改变方向
2. 正向 LIS 一遍，反向 LIS 一遍
3. 答案取最大值

> 时间复杂度：O ($n^2$)

#### 具体代码

```c++
#include <bits/stdc++.h>
using namespace std;
const int N = 110;
int T=1,n;
int a[N],f[N],g[N];

void solve()
{
    cin>>n;
    for(int i=1;i<=n;i++) cin>>a[i];
    
    // 正向 LIS
    for(int i=1;i<=n;i++)
    {
        f[i]=1; // 至少有一个，即当前位置的楼房
        for(int j=1;j<i;j++)
            if(a[j]<a[i])
                f[i]=max(f[i],f[j]+1);
    }
    
    // 反向 LIS
    for(int i=n;i;i--)
    {
        g[i]=1;
        for(int j=n;j>i;j--)
            if(a[j]<a[i])
                g[i]=max(g[i],g[j]+1);
    }
    
    int res=0;
    for(int i=1;i<=n;i++) res=max(res,max(f[i],g[i]));
    cout<<res<<"\n";
}
signed main()
{
    ios::sync_with_stdio(false);
    cin.tie(0);cout.tie(0);
    
    cin>>T;
    while(T--) solve();
}
```

### [登山](https://www.acwing.com/problem/content/1016/)

#### 题目分析

1. 按照编号递增顺序浏览景点
2. 一旦开始下山，就不再上山了
3. 浏览尽可能多的景点

引用一下[彩色铅笔](https://www.colopen-blog.com/)聚聚的图片：![登山](https://cdn.acwing.com/media/article/image/2021/05/30/55909_9c5a386ac1-IMG_67CBC7A02142-1.jpeg)

预处理出以每个点结尾的最长上升子序列和以每个点开始的最长下降子序列，结果取两者长度之和的最大值

#### 具体代码

```c++
#include <bits/stdc++.h>
using namespace std;
const int N = 1010;
int a[N],f[N],g[N],n;
signed main()
{
    ios::sync_with_stdio(false);
    cin.tie(0);cout.tie(0);
    
    cin>>n;
    for(int i=1;i<=n;i++) cin>>a[i];
    
    // 正向 LIS
    for(int i=1;i<=n;i++){
        f[i]=1;
        for(int j=1;j<i;j++)
            if(a[j]<a[i])
                f[i]=max(f[i],f[j]+1);
    }
    // 反向 LIS
    for(int i=n;i>=1;i--){
        g[i]=1;
        for(int j=n;j>i;j--)
            if(a[j]<a[i])
                g[i]=max(g[i],g[j]+1);
    }
    int res=0;
    for(int i=1;i<=n;i++) res=max(res,f[i]+g[i]-1);
    return cout<<res,0;
    
}
```

### [合唱队形](https://www.acwing.com/activity/content/problem/content/1261/)

与上一题  登山 几乎一模一样，这里不再赘述

### [友好城市](https://www.acwing.com/problem/content/1014/)

>  与《算法设计与分析》中的 “电路布线”一题 相同

#### 题目分析

1. 每个城市只有一个友好城市
2. 城市位置各不相同
3. 两条航线不相交

两岸的桥不相交，等价于将一端城市排序后，桥的另一端对应的城市也应该是有序的，否则就会有交叉

这样就转化为最长上升子序列问题了

#### 具体代码

```c++
#include <bits/stdc++.h>
using namespace std;
typedef pair<int, int> PII;
const int N = 5010;
PII a[N];
int f[N],n;
signed main()
{
    ios::sync_with_stdio(false);
    cin.tie(0);cout.tie(0);
    
    cin>>n;
    for(int i=1;i<=n;i++) cin>>a[i].first>>a[i].second;
    // 保证一端有序
    sort(a+1,a+n+1);
    // 正向 LIS
    for(int i=1;i<=n;i++){
        f[i]=1;
        for(int j=1;j<i;j++)
            if(a[j].second<a[i].second)
                f[i]=max(f[i],f[j]+1);
    }
    
    int res=0;
    for(int i=1;i<=n;i++) res=max(res,f[i]);
    return cout<<res,0;
    
}
```

> 参考文献：
>
> [xnuohz的动态规划总结](https://www.acwing.com/blog/content/2111/)
>
> [彩色铅笔的题解补全计划](https://www.acwing.com/blog/content/7459/)

---

在生命的某些时刻，我们每个人都需要听取他人的意见，接受他人的帮助。
