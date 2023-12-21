# SVLBI

SVLBI = Space Very Long Baseline Interferometry

A brief overview of my Master's project ( work in progress) :  **Concept Study of Radio Interferometry in Space using small Satellites**

To find u-v coverage of “N” number of satellites in space orbiting Earth, the position of each at
a particular instant of time is determined from the orbital parameters (like eccentricity, inclination,
semi-major axis, argument of periapsis, right ascension of ascending node, and the initial true
anomaly). In addition, satellite positions are traced with time using changes in true anomaly, which
is derived from the mean anomaly and eccentric anomaly.

\begin{equation}\label{eq1}
  M(t) = M(t_o) + n (t-t_o);
  \end{equation}
\begin{equation}\label{eq2}
  M(t) = E(t) - e sin[E(t)]
  \newline
  \end{equation}
  \begin{equation}
 tan(\frac{t_{anm}}{2}) = \sqrt{\frac{1+e}{1-e}} tan(\frac{E}{2});
 \newline
 \end{equation}
  \begin{equation}\label{eq3}
  n = \sqrt{\frac{G M}{a^3}}
  \end{equation}
