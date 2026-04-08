---
title: Lecon11
description: 
published: true
date: 2026-04-08T12:18:49.616Z
tags: 
editor: markdown
dateCreated: 2026-04-08T12:18:49.616Z
---

# Leçon 11
## § 6.4 $A[X_1,\dots,X_n]$, $A$ factoriel, alors $A[X]$?
**Lem 1** (de Gauss) $A$ factoriel, $P$ et $Q$ polynomes primitifs de $A[X]$, alors $PQ$ est primitif.

**Lem 2** $A$ factoriel, $K_A$ le corps des fraction de $A$. Si $P\in A[X]$ primitif, $k\in K_A$, $kP\in A[X]$, alors $k\in A$. 

**Rappel** : $A$ factoriel ($\Rightarrow$ pgcd $\Rightarrow$ ppcm), $K_A[X]$ factoriel. $\Rightarrow$ base de décompositon en irréductible $\mathcal P:=\{\pi\}_{\pi\in\text{Irr}(K_A[X])}$.  
$\pi\in\text{Irr}(K_A[X])\rightarrow\tilde{\pi}\in A[x]$ primitive, $\tilde{\pi}\sim\pi$.

**Prop** $A$ factoriel. $\mathcal P_{K_A[X]}$ une base de $K_A[X]$ dont les éléments sont des polynomes irréductibles primitif de $A[X]$, $\mathcal P_A$ base de $A$. 
$A[X]$ est un anneau factoriel pour la base $\mathcal P:=\mathcal P_{K_A[X]}\sqcup\mathcal P_A$.
**Dem** $P\in A[X]\subset K_A[X]$ factoriel : 
$$P = u\prod_{\pi\in\mathcal P_{K_A[X]}}\pi^{v_\pi},\quad u\in(K_A[X])^*=K_A\setminus\{0\},(v_\pi)\in\mathbb N^{(\mathcal P)}.$$
$\pi\in A[X]$ primitif, $\prod\limits_{\pi\in\mathcal P}\pi^{v_\pi}$ est primitif (**Lem 1**)
$$\underbrace{P}_{\in A[X]} = \underbrace{u}_{\in K_A}\cdot\underbrace{\prod\limits_{\pi\in\mathcal P_{K_A[X]}}\pi^{v_\pi}}_{\text{primitif}}\,\overset{\tiny \text{Lem 2}}{\Rightarrow}\,u\in A.$$  
On décompose $u$ sur $\mathcal P_A$ : 
$$u=\underbrace{U}_{\in A^*}\prod_{p\in\mathcal P_A}p^{\sigma_p}.$$
$$P = U\prod_{p\in\mathcal P_A}p^{\sigma_p}\prod_{\pi\in\mathcal P_{K_A[X]}}\pi^{v_\pi}.$$
_Unicité_ : 



