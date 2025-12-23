# free-transform

```math
 \textbf{lerp}(v_{0}, v_{1}, t) = v_{0} + t\cdot(v_{1} - v_{0})\newline

```
```math
 \textbf{transform}(p_{0}, p_{1}, p_{2}, p_{3}, u, v)= \textbf{lerp}(\textbf{lerp}(p_{0}, p_{1}, u), \textbf{lerp}(p_{2}, p_{3}, u), v) \newline
```
