---
title: MAT最难的三份试卷分析
layout: post
categories: [简单数学]
description: "test"
customexcerpt: "MAT 2013、2015和2012年的试卷分析"
---

[牛津官网](https://www.maths.ox.ac.uk/study-here/undergraduate-study/maths-admissions-test)给出了每年考试的分档平均分。如果我们以**当年被牛津数学系录取的学生的平均分**为难度判断标准，可以发现卷子最难的三年分别为

$$ {\text{2013年, }} \mu = 60.6 $$

$$ {\text{2015年, }} \mu = 62.7 $$

$$ {\text{2012年, }} \mu = 68.2 $$

所以我在这里理出这三份卷子的难点。

__1. 函数图像的转换__

(2013, 1B)

这个知识点并不难，只是我本人非常生疏（。 所以把它理在这里。MAT的函数transformation在选择题中主要涉及到沿x轴方向平移、沿y轴方向平移、关于一条平行于x轴的直线对称、关于一条平行于y轴的直线对称、关于原点或函数上任意一点的对称。

先来考虑沿x轴方向平移，也即左右平移。这里最为重要的口诀是**左加右减**，即 $y=f(x)$ 向左平移t个单位得到 $y=f(x+t)$ ，向右平移t个单位得到 $y=f(x-t)$ 。沿y轴方向平移则要稍微简单一些。 $y=f(x)$ 向上平移t个单位得到 $y=f(x)+t$ ，向下平移t个单位得到 $y=f(x)-t$。

再来考虑对称。先考虑关于x轴和y轴对称。当函数 $y=f(x)$ 图像关于x轴进行对称变换的时候，得到 $-y=f(x)$ （对于同一个x值，对应的y值正负号掉换）；当其关于y轴进行对称变换的时候，得到 $y=f(-x)$ （为了得到同一个y值，x值需正负号掉换）。

再来考虑关于直线 $y=t$ （平行于x轴）对称。我们可以考虑 $y=f(x)$ 上的任意一点 $({x_0}, {y_0})$ 。若它关于 $y=t$ 对称，它的x坐标不会发生改变。设它的新的y坐标为 %y_t% ，我们有

$$ \frac {y_t + y_0} {2} = t $$

也即

$$ y_t = 2t - y_0 $$

所以 $({x_0}, {y_0})$ 关于 $y=t$ 的对称点为 $({x_0}, {2t-y_0})$ 。

所以， $y=f(x)$ 关于直线 $y=t$ 对称的曲线是 $2t - y=f(x)$ 。

再来考虑关于直线 $x=t$ （平行于y轴）对称。我们仍然来考虑 $y=f(x)$ 上的任意一点 $({x_0}, {y_0})$ 。若它关于 $x=t$ 对称，它的y坐标不会发生改变。设它的新的x坐标为 %x_t% ，我们有

$$ \frac {x_t + x_0} {2} = t $$

也即

$$ x_t = 2t - x_0 $$

所以$({x_0}, {y_0})$ 关于 $x=t$ 的对称点为 $({2t-x_0}, {y_0})$ 。

所以， $y=f(x)$ 关于直线 $x=t$ 对称的曲线是 $y=f(2t-x)$ 。

既然都讲到这儿了，我们顺便来看一看函数的**自对称**。如果函数 $y=f(x)$ 满足 $f(x)=f(2t-x)$ ，就说这个函数关于直线 $x=t$ 对称。我们可以把x换成(t+x)，得到这个式子的另一个表达： $f(t+x)=f(t-x)$ 。

对应的题目不难，我就不写了。

------

__2. 微分__

（2013, 1E）

*The expression*

$$ \frac{\mathrm{d^2} }{\mathrm{d} x^2} \left(2x-1\right)^4 \left(1-x\right)^5 +  \frac{\mathrm{d} }{\mathrm{d} x} \left(2x+1\right)^4 \left(3x^2-2\right)^2 $$

*is a polynomial of degree*

*(a) 9; (b) 8; (c) 7; (d) less than 7.*

这类题（……表达式是几次的多项式）已经考过好几次了，唯一的重点就是**要看整理之后最高项会不会相互抵消**。如果不会相互抵消，则次数即为最高次项的次数；如果相互抵消了，则次数低于最高次项的次数。

我们可以发现 $\left(2x-1\right)^4 \left(1-x\right)^5$ 的最高次部分是 $\left(2x\right)^4 \left(-x\right)^5 = 16x^4 \times \left(-x^5\right) = - 16 x^9 $ ，而 $\left(2x+1\right)^4 \left(3x^2-2\right)^2 = \left(2x\right)^4 \left(3x^2\right)^2 = 16x^4 \times 9 x^4 = 144 x^8 $ 。

我们有

$$ \frac{\mathrm{d^2} }{\mathrm{d} x^2}  \left(- 16 x^9 \right) =  \frac{\mathrm{d} }{\mathrm{d} x} \left(- 144 x^8 \right) = \left(- 144 \times 8 x^7 \right) $$

$$ \frac{\mathrm{d} }{\mathrm{d} x} 144 x^8 = 144 \times 8 x^7 $$

所以两边最高项相加相消，最高次项小于7，这道题选择(d).

------

__3.对数__

（2013, 1F）

*Three **positive** numbers a, b, c satisfy* $ \log_b {a} = 2, \log_b {(c − 3)} = 3, \log_a {(c + 5)} = 2 $. *This information*

*(a) specifies a uniquely.*

*(b) is satisfied by two values of a.*

*(c) is satisfied by infinitely many values of a.*

*(d) is contradictory.*

这个结构的题也考过至少两次了。我们把三个对数式重写成幂：

$$b^2=a{\text{,  }} (I)$$ 

$$b^3=c-3{\text{,  }} (II)$$ 

$$a^2=c+5{\text{,  }} (III)$$

$(I)^2$ 代入 $(III)$ 可得

$$ b^4 = c+5 {\text{,  }} (IV)$$

$ (IV) - (II) $ 可得

$$ b^4-b^3-8=0 $$

很容易看出一个可能的正数解是 $b=2$ 。这种情况下，$a=b^2=4$ ， $c=4^2-5=11$ ，确定了**一个**a的值。 

接下来，考虑

$$ f(x) = b^3 \left( b-1 \right) = 8 $

我们容易看出 $f(x)$ 在 $(-\infty, 0), (0,1)$ 和 $(1, \infty)$ 上单调。所以， $b=2$ 是 $(1, \infty)$ 上的唯一的解。因为题干要求只考虑正数，我们只需要再考虑区间 $(0,1)$ 。不难看出， $f(x)$ 在这个区间上是负的，所以 $f(x)=8$ 在这个区间上没有解。我们得出结论： $a=4$ , $b=2$ , $c=11$ 是这个方程组唯一的正数解。答案选(a).

**注意在数学的语境里，*unique*相当于*only one*.**

&nbsp;  

(2013, 1J)

*For a real number x we denote by* $[x]$ *the largest integer less than or equal to x.*

*Let n be a natural number. The integral*

$$ \intop\nolimits_{0}^{n} \left[ 2^x \right] \operatorname{d} {x} $$

*equals*

*(a)* $\log_2 {\left( \left( 2^n − 1 \right) ! \right)}$ *, (b)* $ n 2^n − \log_2 \left( \left(2^n \right)! \right) $ *, (c)* $n 2^n$ *, (d)* $\log_2 \left( \left(2^n \right)! \right)$ *

*where* $k! = 1 \times 2 \times 3 \times... \times k$ *for a positive integer k.*

这题其实相当好玩，画个图可能会更好理解一点。这题很重要的一个思路是，**从y轴倒着想回x轴来**。这是这道题的Geogebra的链接：[prqt9awz](https://geogebra.org/classic/prqt9awz)。根据这样的思路，把不同颜色的矩形加起来（注意这些矩形的纵宽都为1），我们有

$$ \intop\nolimits_{0}^{n} \left[ 2^x \right] \operatorname{d} {x} $$

$$  = (n-\log_2(1)) + (n-\log_2(2)) + (n-\log_2(3))+ (n-\log_2(4)) + ... + (n-\log_2(2^{n}-1)) $$

$$ = n(2^{n}-1)-\log_2{(2^{n}-1)!} $$

$$ = n 2^{n} - (n + \log_2{(2^{n}-1)!} $$

$$ = n 2^{n} - \left( \log_2{2^n} + \log_2{(2^{n}-1)!} \right) $$

$$ = n 2^n − \log_2 \left( \left(2^n \right)! \right) $$

所以选(b).

------


**11.4，考前最后三个小时，我试图把这三份卷子里真正难的内容理进来，结果写的所有东西全部因为文件名冲突消失不见，在赛博碎纸机里化为齑粉……哈哈！life is full of surprise! 至少我搞懂了（惨淡的微笑**
