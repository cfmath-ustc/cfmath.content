---
title: Radon测度
description: 
published: true
date: 2026-04-08T02:44:33.758Z
tags: 
editor: markdown
dateCreated: 2026-04-02T16:42:34.005Z
---

# Radon测度
**回顾构造 Borélienne 测度的一般方法**: 从一个单调递增且右连续的函数出发, 先在半开区间 $\{]a,b]:-\infty\leq a<b\leq+\infty\}$ 生成的代数 $\mathcal A$ 上定义 $\mathbb R$ 上的外测度, 再诱导出 $\mathbb R$ 上的测度. 
外测度定义: $\mu^*(A) := \inf\{\sum_1^\infty F(b_i)-F(a_i),A\subset\bigcup_1^\infty]a_i,b_i]\}$.

反之, 给定了一个 $\mathbb R$ 上的 Borélienne 测度 $\mu$, 若满足对任意有界 Borélien 集合 $A$, $\mu(A)<+\infty$, 则 $\mu$ 唯一确定了一个单调递增且右连续的函数 $F$ (在相差常数的意义下). 
由 $\mu$ 确定 $F$:
$$F(x):=\begin{cases}\mu(]0,x])&\text{si }x>0\\0&\text{si }x=0\\-\mu(]x,0])&\text{si }x<0\end{cases}$$