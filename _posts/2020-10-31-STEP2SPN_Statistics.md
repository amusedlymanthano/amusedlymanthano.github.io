---
title: STEP2SPN-Statistics：二项概率分布
layout: post
categories: [简单数学]
description: "test"
customexcerpt: "从STEP Support note里摘出的与MAT考试相关的部分"
---

MAT2018年新考纲中加入了binomial probabilities。迄今为止，还没有考到过这个知识点。在这里，我把STEP支持项目里的[STEP2统计学知识点笔记](https://maths.org/step/sites/maths.org.step/files/s2s3/Statistics_topic_notes_2019_1.pdf)中比较重要的部分摘出来。

&nbsp;  

__1.条件概率__

条件概率，写作 $P(A \vert B)$ ，是指**在认为B已经发生的时候，A发生的可能性**。贝叶斯定理（Bayes’ Theorem）的定义式如下：

$$ P(A \vert B) = \frac {P(A \cap B)} {P(B)} $$

我们可以对这个式子稍加变形，得到一个有关 $P(A \cap B)$ 的表达式：

$$ P(A \cap B) = P(A \vert B) P(B) $$

因为交集运算是符合交换律的，我们又有

$$ P(A \cap B) = P(B \vert A) P(A) $$

把这个式子代入贝叶斯定理的定义式，我们得到了一个联系 $P(A \vert B)$ 和 $P(B \vert A)$ 的式子：

$$ P(A \vert B) = \frac {P(B \vert A) P(A)} {P(B)} $$

&nbsp;  

__2.排列与组合__

排列（**P**ermutation），表示为 $ {}^nP_r $ ，意为从n个彼此不相同的元素中选出r个，把它们排成一列的方式——注意我们必须考虑**顺序**。排列的计算式为： 

$$ {}^nP_r = n \times (n-1) \times (n-2) \times ... \times (n-r+1) = \frac {n!} {(n-r)!} $$

组合（**C**ombination 或说 **C**hoosing），表示为 $ {}^nC_r $ 或 $\begin{pmatrix} n \\ r \end{pmatrix}$ ，意为从n个彼此不相同的元素中选出r个的方式——注意**顺序无关紧要**。组合的计算式为：

$$ {}^nC_r = \frac {n \times (n-1) \times (n-2) \times ... \times (n-r+1)} {r \times (r-1) \times (r-2) \times ... \times 1} = \frac {n!} {r!(n-r)!} $$

我们[先前谈到](https://amusedlymanthano.github.io/2020/10/30/STEPSPA6.html)，如果对n个元素进行排列，其中a个元素彼此相同，b个元素彼此相同但不同于那a个元素，c个元素彼此相同但不同于那a个元素及那b个元素……则可能的排序方式总个数为

$$ \frac {n!} {a! \times b! \times c! \times ...} $$

&nbsp;  

__3.离散概率分布__(Discrete Probability Distributions)

所谓“离散”，是指只能取到特定的值（比如掷骰子——我们不能掷出一个2和3之间的数）。能够取到的值可以不是整数，也可以有无限多个，重要的是我们**只能取到特定的值**。

离散概率分布的**期望值/平均值**（**E**xpectation 或说 mean value）用 $ E(X) $ 表示。$E(X)$ 的计算方式为

$$ E(X) =  \sum i  P(X=i) $$

即所有可以取到的值乘上它们各自的概率之和。

离散概率分布的**方差**（**Var**iance）用 $Var(X)$ 表示。 $Var (X) $ 的计算方式为

$$ Var (X) = E(X^2) - \left( E(X) \right)^2 $$

即**平方的期望值减去期望值的平方**。如果两个顺序记不清的话，记住方差**永远是正值**，临场试错就好了。

众数（**Mode** 或说 modal value）是 $P(X=x)$ 最大时x的值。

&nbsp;  

__4.二项分布__ (binomial distribution)

二项分布表示为 $X ~ B(n,p)$ 。对于这样的一个二项分布， $P(X=x)$ 的含义如下：假设一次试验有一种输出为“成功”，其概率为p，其他输出都为“失败”。现在，假设该实验重复发生n次，次次之间相对独立，那么 $P(X=x)$ 就是n次中有x次成功的概率。

对于二项分布 $X ~ B(n,p)$ 而言，

 $$ P(X=x) = \begin{pmatrix}n\\x\end{pmatrix} p^x (1-p)^{n-x} $$ 
 
 $$ E(X) = np $$
 
 $$ Var(X) = np(1-p) $$

 
