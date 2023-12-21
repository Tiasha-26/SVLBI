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
t_{anm} = true anomaly,
e = eccentricity of the orbit,
a = semi-major axis of the orbit,
M = mass of earth,
G = Gravitational constant, and
n = mean motion of the satellite.

To determine true anomalies at different points in time, the Newton-Raphson method is applied at each instance of time.
Using the above parameters and $t_{\text{anm}}(t)$ one can determine the coordinates in a Perifocal coordinate system and then is converted to celestial frame.


```math
```math
```math
