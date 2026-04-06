---
title: My_first_md
description: markdown test of Descartes 
published: true
date: 2026-04-06T07:34:55.922Z
tags: 
editor: markdown
dateCreated: 2026-04-02T15:49:03.913Z
---

# 控制收敛定理在含参积分中的应用
**Théorème de convergence dominée** 设 $(f_n)$ 是 $\mathcal L^1(E,\mathcal A,\mu)$ 中的一个函数列, 满足: 
1. 存在可测函数 $f$ 使得 $f_n(x)\xrightarrow[n\to\infty]{}f\quad\mu-p.p.$ (简单收敛)
2. 存在函数 $g\in\mathcal L_+^1(E,\mathcal A,\mu)$ 使得 $\forall n\geq 1, |f_n(x)|\leq g(x)\quad\mu-p.p.$ (控制条件)

则 $f\in\mathcal L^1(E,\mathcal A,\mu)$ 且 $\int |f-f_n|\xrightarrow[n\to\infty]{}0$ ($f_n$ 在 $L^1$ 意义下收敛于 $f$)

