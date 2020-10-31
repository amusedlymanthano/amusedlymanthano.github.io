---
title: STEP2SPN-Statistics：正态分布
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

因为交集运算是符合交换律的，我们有

$$ P(A \cap B) = P(B \vert A) P(A) $$

把这个式子代入贝叶斯定理的定义式，我们又有

$$ P(A \vert B) = \frac {P(B \vert A) P(A)} {P(B)} $$
