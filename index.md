---
layout: default
title: Spline Functions and Approximation Theory
---

# 2024-Fall-Spline-Functions-and-Approximation-Theory

## 绪论
多项式插值：Lagrange、Newton、Hermite
P_m:最高不超过m次的多项式
Runge现象：f(x)=\frac{1}{1+x^2},x\in[-5,5]，用一个多项式插值不能很好的拟合这个函数
1. 分段插值→样条：分段光滑多项式
2. 插值方法不行，不做插值，改做逼近

给定区间[a,b]，假设a=x_0 < x_1< \cdots < x_k < x_{k+1}=b，
\begin{cases}
I_i=[x_i,x_{i+1}),i=0,\cdots,k
\end{cases}
每一段上都可以约定多项式的次数，叫做multi-degree spline，就是每段上最高次数不一样。我们这门课，每一段上多项式次数，给一个统一的最高值。

$$
S_m(\Delta):=\left\{s(x)\mid s(x)\mid_{I_i}\in \mathbb{P}_m, s(x)\in C^{m-1}[a,b]\right\}
$$

以后每个结点可以指定不同的光滑次数

S_m(\Delta)\subset C^{m-1}[a,b]
线性空间（关心基函数）+对偶基

从计算的角度来说，具有紧支集的基函数

学过有限元的话，具有紧支集的函数\int_\Rf(x)g(x)\d x就很好算

B样条基函数(B-spline) B是Basic

## 回顾
问题：给定区间 $ [a,b] $ 上的函数 $ f(x) $, 给定插值节点组 $ \left\{ x_i \right\}_{i=0}^m $ 使得

$$
a\leqslant x_0 < x_1 < \cdots < x_m \leqslant b
$$

找 $ p_m(x)\in \mathbb{P}_m $ 满足插值条件 $ p_m(x_i)=f(x_i),i=0,\cdots,m $.

> **Theorem**: 插值问题的解存在且唯一.

> **Proof**: 设 $ p_m(x)=a_0+a_1x+\cdots+a_mx^m $, 则插值条件等价于
> 
> $$
 \begin{cases}
a_0+a_1x_0+\cdots+a_mx_0^m=f(x_0)\\
\cdots\ \cdots\ \cdots\ \cdots\ \cdots\ \cdots\ \cdots\ \cdots\\
a_0+a_1x_m+\cdots+a_mx_m^m=f(x_m)\\
\end{cases}
> $$
> 
> d
> 3
>
> 
前m个没有变，加一个额外节点，要全部重新算一遍，所以引入Newton插值


