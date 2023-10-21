Representative Periods duration function
----------------------------------------

| Let :math:`f = \left\{\begin{array}{ccc} [0,T]  & \longrightarrow &  \mathbb{R}_+  \\ t & \mapsto & f(t) \end{array}\right.`

| Let :math:`RP = \{(d_i,\omega_i), i \in \{1,\cdots , n\}\}` a set of representative periods where :math:`d_i` are a part of :math:`[0,T]` and :math:`\omega_i` are weights (:math:`\sum \omega_i = 1`).

The duration function of :math:`RP` is defined as :

.. math::
    C(f) : = \left\{\begin{array}{ccc}
            \mathbb{R}_+  & \longrightarrow &  [0,T]  \\ 
            x & \mapsto & \sum_{i=1}^n \omega_i \cdot C(f_{|d_i})(x)
            \end{array}\right.