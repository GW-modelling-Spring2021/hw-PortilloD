
# The Challenge #1

#### Dalia Portillo

### 1. Steady state means constant head boundaries and a constant flux - in other words, q should be the same in each cell.

![HomogeneousModel](homogenous.jpg)

*Figure 1 Steady State Homogeneous Model*

![HeterogeneousModel](heterogenenous.jpg)

*Figure 2 Steady State Heterogeneous Model*

### 2. Show that the steady state flux agrees with the direct calculation based on the harmonic mean average K. Write the equation defining the direct calculation of the flux.


$K = \large \frac{L_tot}{\frac{l_a}{K_a}+\frac{l_b}{K_b}+\frac{l_c}{K_c}}$

$K = \large \frac{60}{\frac{60-20}{0.0004}+\frac{20}{0.01}+\frac{0}{0.0001}} = \normalsize 0.00058$

$q = \normalsize K* \frac{dH}{dz} = 0.00058*\frac{60-5}{60}=0.00051$

Using Figure 2 above, we see that the flux q can be calculated using the Harmonic Mean
Average. The values are very close but not exactly the same.


### 3. Show the steady state head profile for an aquifer with equal thickness layers that have different K values. Use the head profile to explain WHY the equivalent hydraulic conductivity, Keq, is closer to the lower of the two K values.

![LayeredModel](layeredModel.jpg)

*Figure 3 Steady State with equal thickness layers*

The equivalent hydraulic conductivity takes the harmonic average for a soil column in which flow is perpendicular to the layers. Because Keq is the average value over the entire soil column, Keq is smaller to represent the flow in the slowest zone/layer. 


```python

```
