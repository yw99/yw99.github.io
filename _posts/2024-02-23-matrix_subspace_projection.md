---
layout: post
title: Inequality for norms of matrix producted with projection
date: 2024-02-22 11:12:00-0400
description: compare norms with projections between nested subspaces
tags: all-math
categories: game-theory-perspective
related_posts: false
---

Suppose we have an arbitrary $$m$$-by-$$n$$ matrix $$M$$ and any subspaces $$A\subseteq B$$ in $$n$$-dim. Let $$P_{A,B}$$ denote the projection matrix to $$A,B$$ respectively. We want to compare the norms of $$MP_A$$ and $$MP_B$$ that are related to the singular values.



First and most obvious, the **operator norm** (induced by some arbitrary vector norm):


$$
\begin{align*}
\|MP_A\|_{op} \equiv \sup_{x\in A,\|x\|=1}\|Mx\| \leq \|MP_B\|_{op}.
\end{align*}
$$


Second, the **Frobenius norm**, observe $MP_A=MP_BP_A​$:


$$
\begin{align*}
\|MP_A\|_F^2 &= \|(MP_BP_A)^T\|_F^2\\
&= \|P_A^TP_B^TM^T\|_F^2\\
&\leq \|P_A^T\|_{op}\|P_B^TM^T\|_F^2\\
&=\|MP_B\|_F^2\quad\quad\quad\text{when $\|P_A^T\|_{op}=\|P_A\|_{op}=1$, i.e. $A$ is not null space}
\end{align*}
$$


Third, the **nuclear norm** follows immediately from the above observation:


$$
\begin{align*}
\|MP_BP_A\|_* \leq \|MP_B\|_*
\end{align*}
$$


since $$\|QV\|_*=\sum_i\sigma_i(QV)\leq \sum_i\sigma_i(Q)\|V\|_{op} = \|Q\|_*\|P\|_{op}$$ where operator norm gives the largest singular value.

