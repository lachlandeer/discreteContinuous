## The Stochastic Utility Model

We introduce stochastic shocks into the utility function of each household.
Following KAR, the shocks are multiplicative to conditional marginal utility.
We deviate from KAR by assuming the shocks are Gumbel Distributed.
Under our parameterization the individual's choice problem can be expressed as:

$$
    \max_{x_{i1t}, \ldots, x_{iJt}, z_{it}} u = \sum_{j=1}^J \psi_{ijt} e^{\varepsilon_{ijt}} (x_{ijt} + 1)^\alpha + e^{\varepsilon_{i0t}} (z_{it})^\alpha
$$

subject to

$$
\begin{aligned}
\sum_{j=1}^J p_{jt} x_{ijt} + z_{it} = y_{it} \\
x_{ijt} \geq 0, z_{it} > 0
\end{aligned}
$$

where we introduced the shock as an exponentiated draw from the Gumbel distribution  so that marginal utility is always positive.

We solve for the optimal demands by forming the Lagrangian and applying the Karush-Kuhn-Tucker (KKT) conditions.

### The Lagrangian Representation and the KKT conditions

The lagrangian associated with the stochastic utility maximization problem described above is:

$$
\mathcal{L} = \sum_{j=1}^J \psi_{ijt} e^{\varepsilon_{ijt}} (x_{ijt} + 1)^\alpha + e^{\varepsilon_{i0t}} (z_{it})^\alpha - \lambda \left[ \sum_{j=1}^J p_{jt} x_{ijt} + z_{it} - y_{it} \right]
$$

And the KKT conditions are then:

$$
\begin{aligned}
\frac{\partial \mathcal{L}}{\partial z_{it}} &= 0:
    \alpha e^{\varepsilon_{i0t}} (z_{it})^{\alpha -1} - \lambda = 0 \\
\frac{\partial \mathcal{L}}{\partial x_{ijt}} &= 0:
    \alpha \psi_{ijt} e^{\varepsilon_{ijt}} (x_{ijt} + 1)^{\alpha -1} - \lambda p_{jt} = 0 \text{ if } x_{ijt} >0, \text{ for }  j=1, \ldots, J\\
\frac{\partial \mathcal{L}}{\partial x_{ijt}} &< 0:
    \alpha \psi_{ijt} e^{\varepsilon_{ijt}} (x_{ijt} + 1)^{\alpha -1} - \lambda p_{jt} = 0 \text{ if } x_{ijt} =0, \text{ for }  j=1, \ldots, J\\
\end{aligned}
$$

together with the budget constraint, $\sum_{j=1}^J p_{jt} x_{ijt} + z_{it} = y_{it}$

From $\frac{\partial \mathcal{L}}{\partial z_{it}}$ we know that
$$
\lambda = \alpha e^{\varepsilon_{i0t}} (z_{it})^{\alpha -1}
$$

And using this in $\frac{\partial \mathcal{L}}{\partial x_{ijt}}$ implies:

$$
\begin{aligned}
\frac{ \psi_{ijt} e^{\varepsilon_{ijt}} (x_{ijt} + 1)^{\alpha -1}}{p_{jt}} = e^{\varepsilon_{i0t}} (z_{it})^{\alpha -1} \\
\end{aligned}
$$

Taking logs, this rewrites (for $x_{ijt} >0$):

$$
\begin{aligned}
\ln(\psi_{ijt}) + \varepsilon_{ijt} + (\alpha - 1) \ln(x_{ijt} + 1) - \ln(p_{jt}) =
    \varepsilon_{i0t} + (\alpha-1) \ln(z_{it})
\end{aligned}
$$
