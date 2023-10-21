Duration load definition
------------------------

| Let :math:`f = \left\{\begin{array}{ccc} [0,T]  & \longrightarrow &  \mathbb{R}_+  \\ t & \mapsto & f(t) \end{array}\right.` , a function representing a load or a production as a function of time.
| We define the charge monotone of the function :math:`f` as follows:

.. math::
    C(f) : = \left\{\begin{array}{ccc}
            \mathbb{R}_+  & \longrightarrow &  [0,T]  \\ 
            x & \mapsto & \lambda(\{t|f(t)\geq x\})  
            \end{array}\right.

:math:`\lambda(\{t|f(t)\geq x\}) = \int_{\{t|f(t)\geq x\}}dt` represents time during which the load exceeded the value :math:`x`.

| We define the charge monotone of the function :math:`f` as follows:

.. math::
    C(f) : = \left\{\begin{array}{ccc}
            \mathbb{R}_+  & \longrightarrow &  [0,T]  \\ 
            x & \mapsto & \lambda(\{t|f(t)\geq x\})  
            \end{array}\right.
            
:math:`\lambda(\{t|f(t)\geq x\}) = \int_{\{t|f(t)\geq x\}}dt` represents the time the charge exceeded the value :math:`x`.

.. centered:: Normalization

| Normalized variants are possible. 
| We can do a “power normalization” by setting:  
.. math::
    \tilde{f} = \left\{\begin{array}{ccc}
        [0,T]  & \longrightarrow &  [0,1]  \\ 
        t & \mapsto & \frac{f(t)-f_{min}}{f_{max}-f_{min}}  
        \end{array}\right. \text{ where } \left.\begin{array}{l}
            f_{min} = \underset{t\in[0,T]}{\text{min }} f(t)  \\ 
            f_{max} = \underset{t\in[0,T]}{\text{max }} f(t)
            \end{array}\right.
| We can do a time normalization” by setting: 
.. math::
    \tilde{C}(f) = \left\{\begin{array}{ccc}
        \mathbb{R}_+ & \longrightarrow & [0,1]    \\ 
        x & \mapsto & \frac{C(f)(x)-C(f)_{min}}{C(f)_{max}-C(f)_{min}} =  \frac{\lambda(\{t|f(t)\geq x\})}{T}
        \end{array}\right. \text{ where } \left.\begin{array}{l}
            C(f)_{min} = \underset{x\in\mathbb{R}_+}{\text{min }} C(f)(x)  \\ 
            C(f)_{max} = \underset{x\in\mathbb{R}_+}{\text{max }} C(f)(x)
            \end{array}\right.
| Time and power normalisation corresponds to :math:`\tilde{C}(\tilde{f})` function.
.. note::
    In (`Poncelet et al., 2017`), :math:`L_{c,b} = \tilde{C}(\tilde{f_{c}})(b)` where :math:`c` is an indice to identify a load type.