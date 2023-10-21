Candidate Periods definition
----------------------------
 
| The choice of representative periods is preceded by the choice of candidate periods to become representative.
We can note :math:`d\subset[0,T]` these periods and group them into a set :math:`\mathcal{D}`.

.. math::
    \mathcal{D} = \text{ Set of candidate periods}

| To each period :math:`d` we can associate the load function normalized in absolute power:

.. math::
    \hat{f}_{|d}= \left\{\begin{array}{ccc}
        d & \longrightarrow &  [0,1]  \\ 
        t & \mapsto & \frac{f(t)-f_{min}}{f_{max}-f_{min}}  
        \end{array}\right. \text{ où } \left.\begin{array}{l}
            f_{min} = \underset{t\in[0,T]}{\text{min }} f(t)  \\ 
            f_{max} = \underset{t\in[0,T]}{\text{max }} f(t)
            \end{array}\right.

.. note::
    Potentially : :math:`\forall t \in d , \hat{f}_{|d}(t)>0 \text{ or } \forall t \in d , \hat{f}_{|d}(t)<1`

| We associatethe duration function:
.. math::
    \tilde{C}(\hat{f}_{|d}) = \left\{\begin{array}{ccc}
        \mathbb{R}_+ & \longrightarrow & [0,1]    \\ 
        x & \mapsto & \frac{\lambda(\{t\in d|f(t)\geq x\})}{\lambda(d)}
        \end{array}\right.

.. warning::
    Currently in ``periods``, the set of candidate periods corresponds to a uniform split of the global period :math:`[0,T]`.
    It means that ``RP_length`` must divide ``TemporalData`` length. A periods of 336 hours would have 7 candidate periods of 48 hours partitioning the 336 hours.

    It could be possible to have overlapping candidate periods in future version.