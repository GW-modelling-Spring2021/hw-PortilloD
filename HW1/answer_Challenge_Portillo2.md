
# The Challenge #1

#### Dalia Portillo

### 1. Steady state describes a constant head gradient - in other words, there is no change in the system with time and the flux in is equal to the flux out.

![HomogeneousModel](homogenous.jpg)

*Figure 1 Steady State Homogeneous Model*

![HeterogeneousModel](heterogenenous.jpg)

*Figure 2 Steady State Heterogeneous Model*

### 2. Show that the steady state flux agrees with the direct calculation based on the harmonic mean average K. Write the equation defining the direct calculation of the flux.


$K = \large \frac{L_tot}{\frac{l_a}{K_a}+\frac{l_b}{K_b}+\frac{l_c}{K_c}}$

$K = \large \frac{60}{\frac{60-20}{0.0004}+\frac{20}{0.01}+\frac{0}{0.0001}} = \normalsize 0.00058$

$q = \normalsize K* \frac{dH}{dz} = 0.00058*\frac{60-5}{60}=0.00051$

Using Figure 2 above, we see that the flux q can be calculated using the Harmonic Mean
Average equation. The values are very close but not exactly the same because I used the z elevation as the lengths of the each layer rather than the number of cells. Below I compare the equations using the number of cells occupied by the layer. And lo and behold, the values are exact!


```python
lyr1 = 8.5
lyr2 = 3.5
lyr3 = 0
k1 = 0.0004
k2 = 0.01
k3 = 0.0001
L_tot = lyr1 + lyr2 + lyr3
```


```python
K = L_tot/((lyr1/k1)+(lyr2/k2)+(lyr3/k3))
```


```python
print(K)
```

    0.0005555555555555556
    


```python
q = K*((60-5)/60)
print(q)
```

    0.0005092592592592592
    

$K = \large \frac{8.5 + 3.5}{\frac{8.5}{0.0004}+\frac{3.5}{0.01}+\frac{0}{0.0001}} = \normalsize 0.0005556$

$q = \normalsize K* \frac{dH}{dz} = 0.0005556*\frac{60-5}{60}=0.000509$

### 3. Show the steady state head profile for an aquifer with equal thickness layers that have different K values. Use the head profile to explain WHY the equivalent hydraulic conductivity, Keq, is closer to the lower of the two K values.

![LayeredModel](layeredModel.jpg)

*Figure 3 Steady State with equal thickness layers*

The equivalent hydraulic conductivity takes the harmonic average for a soil column in which flow is perpendicular to the layers. Because Keq is the average value over the entire soil column, Keq is smaller to represent the flow in the slowest zone/layer. Well why does this happen? We can argue that as water flows from a higher permeable layer to a lower permeable layer, the amount of energy used to push the flow through a much tortuous flow path is greater than the energy required to flow through a highly porous material. We see the slope of the head gradient is steep in the middle and at the top while the lowest part of the graph displays a much shallower slope. These sharp changes in gradient is related to the amount of energy released which is related the relative K for each layer.



```python

```
