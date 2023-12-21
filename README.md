# SVLBI

SVLBI = Space Very Long Baseline Interferometry

A brief overview of my Master's project ( work in progress) :  **Concept Study of Radio Interferometry in Space using small Satellites**

To find u-v coverage of “N” number of satellites in space orbiting Earth, the position of each at
a particular instant of time is determined from the orbital parameters (like eccentricity, inclination,
semi-major axis, argument of periapsis, right ascension of ascending node, and the initial true
anomaly). In addition, satellite positions are traced with time using changes in true anomaly, which
is derived from the mean anomaly and eccentric anomaly.

```math
M(t) = M(t_o) + n (t-t_o)
```
```math
M(t) = E(t) - e sin[E(t)]
```
```math
tan(\frac{t_{anm}}{2}) = \sqrt{\frac{1+e}{1-e}} tan(\frac{E}{2})
```
```math
n = \sqrt{\frac{G M}{a^3}}
```
where, M(t) = mean anomaly,
E(t) = eccentric anomaly,
$t_{\text{anm}}(t)$ = true anomaly,
e = eccentricity of the orbit,
a = semi-major axis of the orbit,
M = mass of earth,
G = Gravitational constant, and
n = mean motion of the satellite.

To determine true anomalies at different points in time, the Newton-Raphson method is applied at each instance of time.
Using the above parameters and $t_{\text{anm}}(t)$ one can determine the coordinates in a Perifocal coordinate system and then is converted to celestial frame.

**Conversion of Perifocal to Celestial coordinates**
Let, the position vector in celestial coordinates and perifocal coordinates be denoted by ``` math \vec{r}}_{C}``` and ```math {\vec{r}}_{PQW} ```
respectively. Now,
```math
\vec{r}_{C} = R_1(\Omega)R_2(i)R_3(\omega) \vec{r}_{PQW}
```
```math
R_1(\Omega) =
\begin{bmatrix}
\cos \Omega & -\sin \Omega & 0 \\
\sin \Omega & \cos \Omega & 0 \\
0 & 0 & 1 \\    
\end{bmatrix}
;R_2(i) = 
\begin{bmatrix}
1 & 0 & 0 \\
0 & \cos i & -\sin i\\
0 & \sin  i & \cos i \\ 
\end{bmatrix}
;R_3(\omega) = 
\begin{bmatrix}
\cos \omega & -\sin \omega & 0 \\
\sin \omega & \cos \omega & 0 \\
0 & 0 & 1 \\    
\end{bmatrix}
```
Now, the (u-v-w) coordinate is defined where the w-axis(**$e_{\text{w}}$**) points towards the source of interest($\vec{s}$) or phase tracking center (defined in ECI  frame), u-axis($e_{\text{u}}$) points towards the east and the v-axis ($e_{\text{v}}$)points towards the north celestial pole ($\vec{n}$)
```math
S = \begin{bmatrix}
    cos\alpha cos\delta \\
    sin\alpha cos\delta \\
    sin\delta \\
\end{bmatrix}
```
In Celestial frame: $\alpha$ = right ascension , $\delta$ = declination of source, with $\hat{S}={\hat{e}_w}$, $\hat{n}=(0,0,1)$, ${\hat{e}_u}=\hat{n}\times {\hat{e}_w}$, ${\hat{e}_v}={\hat{e}_w}\times{\hat{e}_u}$, and $\vec{b}$ is the baseline vector. At every instant of time, it changes, thus the projections along (u-v-w) axes have been evaluated at every instant of time.
