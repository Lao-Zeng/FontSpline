## Cubic Font Spline

This site explains what *Cubic Font Spline* algorithm is all about and it's possible applications in real world.

## What is Cubic Font Spline?

*Cubic Font Spline* is an algorithm designed to generate cubic spline curves from TrueType font data. It is to be used in game industry to serve as a spline making tool in PCG (prodedural content generation) and other VFX that utilize cubic splines. The following is a glimpse of the principle mathematical methods that underly the alorithm.

### TrueType from a mathematical point of view

*TrueType* technology is powered by the quadratic *Bézier* curve defined by a parameterized function shown bellow.

$$B(t)=P_1+(1-t)^2(P_0-P_1)+t^2(P_2-P_1), \hspace{0.3cm} 0 \le t \le 1$$

Where $P_0$, $P_1$, and $P_2$ are the control points at different locations in space.

### Cubic Hermite Spline

In computer graphics related industries, cubic *Hermite* spline is widely used. It's defined by the following parametric function.

$$P(t)=(2P_0+m_0-2P_1+m_1)t^3+(-3P_0+3P_1-2m_0-m_1)t^2+m_0t+P_0, \hspace{0.3cm} 0 \le t \le 1$$

Where $P_0$ and $P_1$ are the control points of the curve, $m_0$ and $m_1$ are the tangents at $P_0$ and $P_1$ respectively.

*Bézier curve* and *Hermite spline* are different in nature. They have different pratical applications in real world, and cannot be used interchangeablely. [This link](https://graphics.stanford.edu/courses/cs148-09/lectures/splines.pdf) might be a good place to start with in case you want to know more about this topic.

