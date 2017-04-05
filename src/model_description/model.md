---
title: "A Simple Discrete Continuous Choice Model"
author: Lachlan Deer
date: April, 2017
---

## The Non-Stochastic Choice Problem

We consider a special case of the Kim, Allenby and Rossi (2002) model of discrete-continuous demand.
Households face the following problem:

$$
    \max_{x_{i1t}, \ldots, x_{iJt}, z_{it}} u = \sum_{j=1}^J \psi_{ijt}(x_{ijt} + 1)^\alpha + (z_{it})^\alpha
$$

subject to

$$
\begin{aligned}
\sum_{j=1}^J p_{jt} x_{ijt} + z_{it} = y_{it} \\
x_{ijt} \geq 0, z_{it} > 0
\end{aligned}
$$

where $i$ denotes households, $t$ denotes time, $j$ denotes brand, $x_{ijt}$'s are quantities purchased by household $i$ or brand $j$ at time $t$, $p_{jt}$ are prices, $y_{it}$ is trip expenditure, and $z_{it}$ denotes the numeraire good.

Preference parameters are constrained such that

$$
\psi_{ijt} > 0, \alpha \in (0,1)
$$

And are parameterized in terms of observed features (FEAT), HHsize, HHInc and Interpurchase time (IPT) as

$$
\begin{aligned}
\ln(\psi_{ijt}) &= \theta_j + \theta_5 FEAT + \theta_6 HHInc \\
\ln \left(\frac{\alpha}{1-\alpha}\right) &= \theta_7 IPT + \theta_8 HHsize
\end{aligned}
$$
