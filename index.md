---
title: Radon测度
description: 
published: true
date: 2026-04-08T03:23:25.067Z
tags: 
editor: markdown
dateCreated: 2026-04-02T16:42:34.005Z
---

# Radon测度
**回顾构造 Borélienne 测度的一般方法**: 从一个单调递增且右连续的函数出发, 先在半开区间 $\{]a,b]:-\infty\leq a<b\leq+\infty\}$ 生成的代数 $\mathcal A$ 上定义 $\mathbb R$ 上的外测度, 再诱导出 $\mathcal B(\mathbb R)$ 上的测度. 
外测度定义: $\mu^*(A) := \inf\{\sum_1^\infty F(b_i)-F(a_i),A\subset\bigcup_1^\infty]a_i,b_i]\}$.

反之, 给定了一个 $\mathcal B(\mathbb R)$ 上的 Borélienne 测度 $\mu$, 若满足对任意有界 Borélien 集合 $A$, $\mu(A)<+\infty$, 则 $\mu$ 唯一确定了一个单调递增且右连续的函数 $F$ (在相差常数的意义下). 
由 $\mu$ 确定 $F$:
$$F(x):=\begin{cases}\mu(]0,x])&\text{si }x>0\\0&\text{si }x=0\\-\mu(]x,0])&\text{si }x<0\end{cases}$$

## $\mathbb R$ 上的 Radon 测度和 $C_c(\mathbb R)$ 上的线性型一一对应
一个 $\mathbb R$ 上局部有限的 Borélienne 测度称为 $\mathbb R$ 上的一个 Radon 测度.
给定一个 Radon 测度 $\mu$, 我们可以定义一个 $C_c(\mathbb R)$ 上的线性型: 
$$J_\mu:C_c(\mathbb R)\to \mathbb R,\quad f\mapsto\int f\,\mathrm{d}\mu.$$
为赋予 $C_c(\mathbb R)$ 一个拓扑使得 $J_\mu$ 连续, 我们定义 $C_c(R)$ 中的序列收敛: $C_c(R)$ 中的函数列 $(f_n)_{n\geq 1}$ 有一个公共的紧支撑集 $K$ (i.e. $\forall n,\text{supp}(f_n)\subset K$) 且 $f_n$ 一致收敛于 $f$. 此时有 $f\in C_c(\mathbb R)$ 且 $\text{supp}(f)\subset K$.
在此拓扑下, $J_\mu$ 是连续的, 因为: 若有 $f_n\to f$ 如上, $K$ 为公共的紧支撑集, 则
$$|J_\mu(f)-J_\mu(f_n)| \leq \int_K |f-f_n|\,\mathrm{d}\mu\leq\Vert f-f_n\Vert_\text{sup}\,\mu(K)\xrightarrow[n\to\infty]{}0.$$

**Thm** (Riez-Markov) 设 $J$ 是 $C_c(\mathbb R)$ 上的一个正线性型 (i.e. $\forall f\in C_c(\mathbb R),f\geq0\Rightarrow J(f)\geq 0$), 则存在唯一一个 $(\mathbb R,\mathcal B(\mathbb R))$ 上的 Radon 测度 $\mu$, 使得 $J=J_\mu$. 即
$$\forall f\in C_c(\mathbb R),\quad J(f)=\int f\mathrm{d}\mu.$$
