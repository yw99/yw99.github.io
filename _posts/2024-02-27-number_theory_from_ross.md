---
layout: post
title: A lemma from Ross
date: 2024-02-27 11:12:00-0400
description: which is the best math summer camp in the world
tags: all-math
categories: number-theory
related_posts: false
---

Just for my own memory, here is a (very intuitive) lemma I struggled to prove in [Ross](https://rossprogram.org/) in Huangshan where I stayed up super late with Xqy (to whom I'm grateful) discussing and eventually proving it. 

**Statement** as follows:


$$
\forall g,k\in\mathbb{Z}\ with\ gcd(g,k)=1,\ it\ holds\ \forall t\in\mathbb{Z}\ \exists a\in\mathbb{Z}\ such\ that\ gcd(t,g+ak)=1.
$$


**Proof:**

Fix such $$g,k\in\mathbb{Z}$$ and arbitrary $$t\in\mathbb{Z}$$. Factorize $$t=\prod_{i=1}^np_i^{e_i}$$.

Consider $$p_i^{e_i}$$ for any $$1\leq i\leq n$$:

If $$p_i\mid k$$ and $$p_i\nmid g$$, then $$gcd(p_i^{e_i},g+ak)=1$$ for any $$a\in\mathbb{Z}$$.

If $$p_i\nmid k$$, then $$gcd(p_i^{e_i},k)=1$$. Proceed as follows:

Let set $$T=\{a\in\mathbb{N}\cup\{0\}: a<p_i^{e_i}\}$$ and $$S=\{g+ak:a\in T\}$$.

Let function $$f:S\rightarrow T$$ by $$g+ak\mapsto g+ak\mod{p_i^{e_i}}$$.

If $$g+a_1k \equiv g+a_2k\mod{p_i^{e_i}}$$ (and we know $$gcd(p_i^{e_i},k)=1$$), then $$p_i^{e_i}\mid (a_2-a_1)$$.

This then implies $$a_2=a_1$$ by definition of $$T$$, so $$f$$ is injective.

By injectivity, we have $$T = f(S)$$, which then implies $$\exists a_i\in T$$ such that $$g+a_ik\equiv 1\mod{p_i^{e_i}}$$ and so $$gcd(g+a_ik, p_i^{e_i})=1$$.

Finally, by Chinese Reminder Theorem (which I completely forget now), we get $$\exists a\in\mathbb{Z}$$ such that $$a\equiv a_i \mod{p_i^{e_i}}$$ for all $$i$$ where $$p_i\nmid k$$. And for this $$a$$, one can check $$gcd(g+ak,t)=1$$.