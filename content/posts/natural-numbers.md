---
date: '2025-07-24T18:33:43+05:30'
title: 'Natural Numbers, Induction and Well Ordering'
summary: 'What actually the hack?'
---

My goal in this post and future posts is axiomatic development of Natural Numbers, Integers, Rational Numbers, and Real Numbers. Maybe I will also develop Complex Numbers and try to show the difference between \(\mathbb{C}\) and \(\mathbb{R}^2\). I will try to do it in as modern a terminology as possible. So let's start with Natural numbers.

### Natural Numbers
Natural numbers consist of a set \(\mathbb{N}\), a distinguished element \(0\in\mathbb{N}\) and a function ,called **successor function**, \(\nu\colon\mathbb{N}\to\mathbb{N}^{\times}\colon= \mathbb{N}\backslash\{0\}\) with the following properties:  

\((N_{0})\) \colon \(\nu\) is injective.  
\((N_{1})\): If \(N\subseteq\mathbb{N}\:\wedge (0\in\mathbb{N})\:\wedge (\forall n\in N : \nu(n) \in N)\) then \(N=\mathbb{N}\)

For our first theorem let's prove that \(\nu\) is surjective or in other words every Natural number except \(0\) every natural number is a successor of some other natural.

**Theorem** : \(\nu\) is surjective.  
**Proof** : Suppose \[N=\text{im}(\nu)\cup\{0\}=\{n\in\mathbb{N}^{\times}: \exists n'\in\mathbb{N}\colon\nu(n')=n\}\cup\{0\}\]
Trivially, \(0\in N\). Suppose \(n\in N\) then \(\nu(n)\in\mathbb{N}\) because for \(\nu(n)\) we have \(n'=n\).  
Therefore, by \((N_1)\) we have \(N=\mathbb{N}\).
