---
title: tourist 和 newbie 竞争的 Day2
date: 2022-02-17 17:26:40
categories: 研究生入学考试
tags: 每日打卡
cover: /img/tourist.jpg
---

## 每日打卡

Plans to protect air and water , wilderness and wildlife are in fact plans to protect man .

> 翻译见文末

## 数学学习

<p align="center"  style="color: green ">迷糊概念扯清</p>

在数学中有许多微小的概念看似不起眼，却在理解上发挥重大作用。

### 导数定义

两种形式：
$$
\begin{aligned}
f'(x_0) =& \lim_{\Delta x \to 0} \frac {f(x_0+\Delta x)-f(x)} {\Delta x} 
\\ \\
f'(x_0) =&  \lim_{\Delta x_0 \to 0} \frac {f(x)-f(x_0)} {x-x_0}
\end{aligned}
$$

> 在导数在导数的分式极限定义中，分母的极限 → $0_+$或→ $0_-$,如果只是单边行为 ( 即仅$0_+$或仅
> →$0_-$ ),则该极限只能是函数在该点处的左导数或右导数,而不是在该点的导数.

### dy和 $\Delta y$ 的区别

dy 表示微分，$dy=f'(x)dx$

$\Delta y$ 表示函数的增量，$Δy=f(x+Δx)-f(x)$



1. 二者一般不相等，但有时可由公式相互转化。
2. 一般的， dy ≠ Δy。dy相当于当Δx趋近于无穷小时的Δy。
3. 可微时，Δy=dy+o(Δx) 。而o(Δx)是比Δx高阶的无穷小。

### 四者关系

极限存在、连续、有界、可积、可导/可微

1. 可导（可微）一定连续，连续不一定可导。

2. 连续则极限存在，极限存在不一定连续。

3. 连续一定可积，可积不一定连续。

   1. 定理1 设f(x)在区间[a,b]上连续，则f(x)在[a,b]上可积。（这是定理所以连续一定可积）

   2. 定理2 设f(x)在区间[a,b]上有界，且只有有限个间断点，则f(x)在[a,b]上可积。 （有间断点函数就不连续了 但仍可积）根据定理连续函数一定可积而可积不一定连续。

4. 连续一定有界（闭区间），可积一定有界，可导可微等价。


### 碎碎念

1. 分段点的导数值，一般是考察导数的定义
2. 由极限确定的函数，先把具体函数计算出来，一般是分段函数
3. 莱布尼兹公式

## 外文赏析

### Text

<center><b>Why jK8v!ge4D Isn't a Good Password</b></center>

<p align="right"  style="color: green "># 科普</p>

Take a look at these two passwords: jK8v!ge4D, greenelephantswithtophats

> 开篇引出两个密码，说明与密码相关

Which password do you think takes the longest for a computer to **crack**? And which password do you think is the easiest to remember?

The answer to both of these questions is password number 2 . Yet people are encouraged to create passwords that look like number 1 . People have been taught to write passwords that are difficult for humans to remember ,  **for no real reason.**

> 人们被教导 创建一个不好记的密码，然而这毫无道理。
>
> 表明文章观点，以下开始阐述。

There are many **bizarre** things in internet standards. Validation is one of them. As a front-end developer, I am expected to validate the input that users enter into so-called input fields. These are the fields that you use when you enter your username, your email, your home address, your postal number, and so on.

It is the duty of a front-end developer to ensure that the user doesn't enter anything **malicious** or anything improperly formatted into these fields.

Phone numbers can often include numbers, a plus sign and a dash, maybe some parenthesis too if we're feeling liberal. E-mail addresses are difficult to validate, however a common practice is that they must include an at-sign (@) followed by a period, even though a perfectly valid e-mail address could actually have none of those attributes.

Some websites try to validate names by forcing people to keep their names within a certain length or by forcing people to only use certain characters, though such validations never really work as people's names can be just about anything.

**Validation is implemented for several reasons .** One is security concerns. Validation prevents users from entering scary code into the fields that could alter the database or perform other malicious actions. Another is to force a certain data type.

> 验证是为了几个原因。

If a field is only supposed to consist of numbers, the database engineer might have set up a database column that only allows for numbers, which means that a symbol that isn't a number would cause an error to occur.

But the primary reason is to help the user avoid making mistakes .

Forcing your passwords

For some reason, front-end developers are expected to babysit users into entering what is traditionally conceived to be a good password. It should be at least eight characters long, including uppercase and lowercase characters, a number, and if we're feeling really obnoxious, it should even include a special character, like an exclamation mark.

Here is an example of what is generally considered to be a solid password: jK8v|ge4D. Considering the fact that you are often asked to enter a password like this, it'd be fair of you to assume that we'd consider this a good password .

But it's a bad password . 

First of all, how is anyone supposed to remember that? What ends up happening is that users can't remember it so they write the passwords down somewhere. Like on a post-it note. And then they end up getting "hacked".

Secondly, users end up using the same password for different services, because it's **obnoxious** to keep track of a whole bunch of these complex passwords. When you create an account for a decent website, some magical code behind-the-scenes transforms your password into a hash . 

Your password ends up looking something like this in the database:
k5ka2p8bFuSmoVTItzOyyuaREkkKBcCNqoDKzYiJL9RaE8yMnPgh2XzzFONDrUhgrcLwg78xs1w5pJiypEdFX

Even if the database is hacked, the hacker cannot really do anything with this information. It is possible to figure out the original password if the password is common enough and the algorithm is simple enough, though with a somewhat decent password that's been properly hashed, it's generally quite safe . 

The issue is that not all services hash their users' passwords. If you use the same password for many services, you might end up using a poorly programmed service that actually does save your password in plain text in their database.

If they end up getting compromised, the hacker suddenly has your password to all of your accounts where you use the same password. This is scary, and it happens a lot more often than one might think.

This is why you MUST use different passwords for different websites. However today's users have accounts on tons and tons of websites. How are they supposed to remember all of their passwords? Power users may use a password tool, but you can't expect the average user to do that.

> Conclusion:
>
> 这一篇对 计算机er 非常友好哇hh，简洁易懂。
>
> 但是我经常用 钥匙串 记住密码 qwq

### Analysis

1. xxx is implemented for ....  xxx 是为了...
2. bizarre 奇怪的，奇特的
3.   malicious 恶毒的，怀有恶意的

---

那些保护空气、水和野生动物的计划，实际上是为了保护人类自己。
