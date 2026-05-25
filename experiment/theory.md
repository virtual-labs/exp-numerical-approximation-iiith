Finding the area under a curve involves calculating the region between a given curve and the x-axis (the line $y=0$), within two specified limits, $x=a$ and $x=b$. Mathematically, this is typically solved by integrating the function and evaluating the result at these limits. The difference gives the exact area under the curve. However, not all functions can be integrated analytically, and this method works best for smooth, well-behaved functions.

In many practical situations, especially in computer programming, we use numerical approximation methods to estimate the area under a curve. These methods are essential when an exact analytical solution is not possible or is too complex to obtain.

The basic idea behind numerical approximation is to divide the interval $[a, b]$ into $n$ equal segments, each of width $l = \frac{b-a}{n}$. The area under the curve in each segment is approximated by a simple geometric shape, such as a rectangle or a trapezoid. The height of each rectangle can be taken as the value of the function at the start, end, or midpoint of the segment. The total area is then the sum of the areas of all these shapes.

For example, the **rectangle (midpoint) rule** estimates the area as:

$$
	ext{Area} \approx \sum_{i=0}^{n-1} f(x_i) \cdot l
$$

where $x_i$ is a sample point in the $i$-th segment.

As the number of segments $n$ increases (i.e., as the width $l$ decreases), the approximation becomes more accurate. In the limit as $n \to \infty$, the numerical approximation approaches the exact area.

On a computer, we are limited by finite precision, but by choosing a sufficiently large $n$, we can achieve highly accurate results for practical purposes. Numerical approximation techniques are widely used in scientific computing, engineering, and many fields where analytical solutions are not feasible.

<img src="images/arch.gif" alt="Area under a curve illustration">

In this experiment, you will learn how to implement and use numerical approximation methods in code to estimate the area under a curve. This approach demonstrates how computers can solve mathematical problems to a high degree of accuracy, even when exact solutions are not available.
