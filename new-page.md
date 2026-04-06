---
title: My_first_md
description: markdown test of Descartes 
published: true
date: 2026-04-06T08:28:10.397Z
tags: 
editor: markdown
dateCreated: 2026-04-02T15:49:03.913Z
---

# 控制收敛定理在含参积分中的应用
**Théorème de convergence dominée** 
设 $(f_n)$ 是 $\mathcal L^1(E,\mathcal A,\mu)$ 中的一个函数列, 满足: 
1. 存在可测函数 $f$ 使得 $f_n(x)\xrightarrow[n\to\infty]{}f\quad\mu-p.p.$ (简单收敛)
2. 存在函数 $g\in\mathcal L_+^1(E,\mathcal A,\mu)$ 使得 $\forall n\geq 1, |f_n(x)|\leq g(x)\quad\mu-p.p.$ (控制条件)

则 $f\in\mathcal L^1(E,\mathcal A,\mu)$ 且 $\int |f-f_n|\xrightarrow[n\to\infty]{}0$ ($f_n$ 在 $L^1$ 意义下收敛于 $f$)

## 含参积分
设有函数 $f(u,x)$, 其中 $x\in(E,\mathcal A,\mu)$ 为测度空间, $u\in U$ 为度量空间. 我们定义 $F(u) = \int f(u,x) \,\rm{d}\mu(x)$
问: $F(u)$ 是否关于参数 $u$ 连续? 是否关于参数 $u$ 可微?

**Thm** (Continuité d'une intégrale à paramètre) 
设 $(E,\mathcal A,\mu)$ 是一个测度空间, $U$ 是一个度量空间. 设 $f:U\times E\to\mathbb R$. 取定一点 $u_0\in U$. 若 $f$ 满足如下条件: 
1. $\forall u\in U$, 函数 $x\mapsto f(u,x)$ 是可测的. 
2. 对 $\mu-p.p.$ 的 $x\in E$, 函数 $u\mapsto f(u,x)$ 在 $u_0$ 点连续. 
3. 存在函数 $g\in\mathcal L_+^1(E,\mathcal A,\mu)$ 使得 
$$\forall u\in U,\quad|f(u,x)|\leq g(x)\quad \mu-p.p.$$

则函数 $F(u) = \int f(u,x) \,\rm{d}\mu(x)$ 是良定义的, 且在 $u_0$ 点连续.

**证明思路** 1.+3. $\Rightarrow F$ 是良定义的. 连续性可转**序列刻画**, 再使用 TCD. 

**Thm** (Dérivabilité d'une intégrale à paramètre)
设 $(E,\mathcal A,\mu)$ 是一个测度空间, $U=I$ 为 $\mathbb R$ 中的一个区间. $f:I\times E\to\mathbb R$. 我们固定一点 $u_0\in I$. 若 $f$ 满足如下条件: 
1. $\forall u\in I$, 函数 $x\mapsto f(u,x)\in \mathcal L^1(E,\mathcal A,\mu)$.
2. 对 $\mu-p.p.$ 的 $x\in E$, 函数 $u\mapsto f(u,x)$ 在 $u_0$ 点 (关于 $u$) 可导, 导数为 $\frac{\partial f}{\partial u}(u_0,x)$.
3. 存在函数 $g\in\mathcal L_+^1(E,\mathcal A,\mu)$ 使得
$$\forall u\in I,\quad|f(u,x)-f(u_0,x)|\leq g(x)|u-u_0|\quad\mu-p.p.$$
则函数 $F(u) = \int f(u,x) \,\rm{d}\mu(x)$ 在 $u_0$ 点连续且可导, 导数为
$$F'(u_0) = \int \frac{\partial f}{\partial u}(u,x) \,\rm{d}\mu(x).$$

**证明思路** 任取一列 $I$ 中收敛到 $u_0$ 的点列 $(u_n)$ avec $u_n\neq u_0$, 定义差分函数 $\varphi_n(x)=\frac{f(u_n,x)-f(u_0,x)}{u_n-u_0}$, 它是可积函数的线性组合, 从而也可积. 由条件 3. 可知 $|\varphi_n(x)|\leq g(x)\quad\mu-p.p.$ 令 $\varphi_\infty(x):=\limsup_{n\to\infty}\varphi_n(x)$.
由条件 2. 可知, 对 $\mu-p.p.$ 的 $x\in E$,
$$\varphi_n(x)\xrightarrow[n\to\infty]{}\frac{\partial f}{\partial u}(u_0,x) = \varphi_\infty(x).$$
于是函数列 $(\varphi_n)$ 和 $\varphi_\infty$ 满足 TCD 的条件, 故 $\varphi_\infty\in\mathcal L^1(E,\mathcal A,\mu)$ 且
$$\int \varphi_\infty(x)\,\rm{d}\mu(x) = \lim_{n\to\infty}\int \varphi_n(x)\,\rm{d}\mu(x) = \lim_{n\to\infty}\frac{F}{}$$


我们可以扩充 $\frac{\partial f}{\partial u}(u_0,x)$ 的定义域至整个 $E$ 且有
$$\int\frac{\partial f}{\partial u}(u_0,x)\,\rm{d}\mu(x) = \int \varphi_{\infty}(x) \,\rm{d}\mu(x).$$
