# Numerical Computation – WS26

Exercise solutions for the *Numerical Computation* course (Data Science Master, winter semester 2026).
Each exercise sheet is a Jupyter notebook with the implementation, plots and written answers.

Author: Nico Reiterer

## Contents

| File | Topic |
| --- | --- |
| [ex1.ipynb](ex1.ipynb) | Exercise 1: quadrature, error estimation, convergence plots, polynomial interpolation |
| [ex1_14_b.jpg](ex1_14_b.jpg) | Handwritten solution for Exercise 1.4 b (embedded in the notebook) |
| [ex2.ipynb](ex2.ipynb) | Exercise 2 (in progress) |
| [main.py](main.py) | Placeholder entry point from the project template (not used) |

### Exercise 1 overview

- **1.1 Approximation of the integral:** trapezoidal and box rule; checks that the error behaves like $Ch^2$ (trapezoidal) and $Ch$ (box).
- **1.2 Error estimator:** an a-posteriori error estimate built from $T(h)$ and $T(h/2)$, compared against the true error.
- **1.3 Functions to inspect:** which plot (log-log or semilog) turns algebraic and exponential convergence into straight lines, and how to read off the rate.
- **1.4 Interpolating polynomials:** Lagrange form by hand, checked with `np.polyfit` / `np.polyval`.
- **1.5 Interpolating polynomials II:** extrapolation to $h = 0$ (Neville-type scheme) for $f(h) = (e^h - 1)/h$ and the convergence order of each column.
- **1.6 Interpolating polynomials III:** linear vs. cubic interpolation of $x^2/(1+x^2)$ and the resulting quadrature errors on $[0, 3]$.

## Setup

The project targets Python 3.12 (see [.python-version](.python-version)) and uses [uv](https://docs.astral.sh/uv/).

```bash
uv venv
uv sync
```

> The notebook dependencies are declared in [pyproject.toml](pyproject.toml).

