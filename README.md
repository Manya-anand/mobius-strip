# mobius-strip
Parametric modelling of a Möbius strip in Python with surface area and edge length calculation.

*CODE STRUCTURE

1) mobius_strip() : Generates a mesh of (x, y, z) points based on the Mobius strip parametric equations.
2) plot() : Uses Matplotlib's 3D plotting to visualize the strip.
3) surface_area() : Numerically integrates the surface using the magnitude of the cross product of partial derivatives.
4) edge_length() : Approximates the length of the boundary curve by summing Euclidean distances between mesh points.


*SURFACE AREA 

The area is computed using:
- Cross product of ∂r/∂u and ∂r/∂v (gives the infinitesimal surface area element `dA`)
- 2D numerical integration over the `u-v` parameter grid using `scipy.integrate.simpson`


*EDGE LENGTH

- The boundary at `v = ±w/2` is extracted.
- The length of each boundary curve is estimated via distance between successive 3D points.
- The final length is the average of both curves, due to MObius strip's topological twist.


*CHALLENGES THAT I FACED

1) Understanding the Mobius strip (one surface, one edge)
2) Ensuring correct computation of cross products for the surface area
3) Handling edge detection since the strip appears to have two edges in the parameter grid







---
