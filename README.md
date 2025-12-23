# free-transform

```math
 \textbf{lerp}(v_{0}, v_{1}, t) = v_{0} + t\cdot(v_{1} - v_{0})\newline

```
```math
 \textbf{transform}(p_{0}, p_{1}, p_{2}, p_{3}, u, v)= \textbf{lerp}(\textbf{lerp}(p_{0}, p_{1}, u), \textbf{lerp}(p_{2}, p_{3}, u), v) \newline
```

```math
|x| = \left\{ \begin{array}{cl}
x & : \ x \geq 0 \\
-x & : \ x < 0
\end{array} \right.
```

```math
U\to -\frac{\sqrt{(\text{Px} (-\text{y0}+\text{y1}-\text{y2}+\text{y3})+\text{Py} (\text{x0}-\text{x1}+\text{x2}-\text{x3})+\text{x0} \text{y2}-2 \text{x0} \text{y3}+\text{x1} \text{y3}-\text{x2} \text{y0}+2 \text{x3} \text{y0}-\text{x3} \text{y1})^2+4 (\text{Px} (\text{y3}-\text{y0})+\text{Py} (\text{x0}-\text{x3})-\text{x0} \text{y3}+\text{x3} \text{y0}) ((\text{x2}-\text{x3}) (\text{y0}-\text{y1})-(\text{x0}-\text{x1}) (\text{y2}-\text{y3}))}+\text{x0} \text{y2}-2 \text{x0} \text{y3}+\text{x1} \text{y3}-\text{x2} \text{y0}+2 \text{x3} \text{y0}-\text{x3} \text{y1}}{2 (-(\text{x0}-\text{x1}) (\text{y2}-\text{y3})+\text{x2} (\text{y0}-\text{y1})+\text{x3} (\text{y1}-\text{y0}))}+\frac{\text{Px} (-\text{y0}+\text{y1}-\text{y2}+\text{y3})}{2 ((\text{x0}-\text{x1}) (\text{y2}-\text{y3})+\text{x2} (\text{y1}-\text{y0})+\text{x3} (\text{y0}-\text{y1}))}+\frac{\text{Py} (\text{x0}-\text{x1}+\text{x2}-\text{x3})}{2 ((\text{x0}-\text{x1}) (\text{y2}-\text{y3})+\text{x2} (\text{y1}-\text{y0})+\text{x3} (\text{y0}-\text{y1}))}

```

```math
V\to \frac{\sqrt{(\text{Px} (-\text{y0}+\text{y1}-\text{y2}+\text{y3})+\text{Py} (\text{x0}-\text{x1}+\text{x2}-\text{x3})+\text{x0} \text{y2}-2 \text{x0} \text{y3}+\text{x1} \text{y3}-\text{x2} \text{y0}+2 \text{x3} \text{y0}-\text{x3} \text{y1})^2+4 (\text{Px} (\text{y3}-\text{y0})+\text{Py} (\text{x0}-\text{x3})-\text{x0} \text{y3}+\text{x3} \text{y0}) ((\text{x2}-\text{x3}) (\text{y0}-\text{y1})-(\text{x0}-\text{x1}) (\text{y2}-\text{y3}))}+2 \text{x0} \text{y1}-\text{x0} \text{y2}-2 \text{x1} \text{y0}+\text{x1} \text{y3}+\text{x2} \text{y0}-\text{x3} \text{y1}}{2 ((\text{x0}-\text{x3}) (\text{y1}-\text{y2})+\text{x1} (\text{y3}-\text{y0})+\text{x2} (\text{y0}-\text{y3}))}+\frac{\text{Px} (\text{y0}-\text{y1}+\text{y2}-\text{y3})}{2 ((\text{x0}-\text{x3}) (\text{y1}-\text{y2})+\text{x1} (\text{y3}-\text{y0})+\text{x2} (\text{y0}-\text{y3}))}+\frac{\text{Py} (-\text{x0}+\text{x1}-\text{x2}+\text{x3})}{2 ((\text{x0}-\text{x3}) (\text{y1}-\text{y2})+\text{x1} (\text{y3}-\text{y0})+\text{x2} (\text{y0}-\text{y3}))}
```

```math
\left\{ \begin{array}\\
u = -\frac{\sqrt{(Px (-y0+y1-y2+y3)+Py (x0-x1+x2-x3)+x0 y2-2 x0 y3+x1 y3-x2 y0+2 x3 y0-x3 y1)^2+4 (Px (y3-y0)+Py (x0-x3)-x0 y3+x3 y0) ((x2-x3) (y0-y1)-(x0-x1) (y2-y3))}+x0 y2-2 x0 y3+x1 y3-x2 y0+2 x3 y0-x3 y1}{2 (-(x0-x1) (y2-y3)+x2 (y0-y1)+x3 (y1-y0))}+\frac{Px (-y0+y1-y2+y3)}{2 ((x0-x1) (y2-y3)+x2 (y1-y0)+x3 (y0-y1))}+\frac{Py (x0-x1+x2-x3)}{2 ((x0-x1) (y2-y3)+x2 (y1-y0)+x3 (y0-y1))}\\

v = \frac{\sqrt{(Px (-y0+y1-y2+y3)+Py (x0-x1+x2-x3)+x0 y2-2 x0 y3+x1 y3-x2 y0+2 x3 y0-x3 y1)^2+4 (Px (y3-y0)+Py (x0-x3)-x0 y3+x3 y0) ((x2-x3) (y0-y1)-(x0-x1) (y2-y3))}+2 x0 y1-x0 y2-2 x1 y0+x1 y3+x2 y0-x3 y1}{2 ((x0-x3) (y1-y2)+x1 (y3-y0)+x2 (y0-y3))}+\frac{Px (y0-y1+y2-y3)}{2 ((x0-x3) (y1-y2)+x1 (y3-y0)+x2 (y0-y3))}+\frac{Py (-x0+x1-x2+x3)}{2 ((x0-x3) (y1-y2)+x1 (y3-y0)+x2 (y0-y3))}

\end{array} \right.
```
