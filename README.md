# Spectral Methods in Scientific Computing

## Overview

Spectral methods are a class of numerical techniques used to solve differential equations, integral equations, and other types of mathematical problems. These methods are highly effective for problems with smooth solutions and involve representing the solution as a sum of basis functions, typically polynomials or trigonometric functions. The coefficients of these basis functions are determined by transforming the original problem into a system of algebraic equations.

This repository contains implementations of various weighted residual methods, including collocation, Galerkin, least squares, subdomain methods, and the Ritz method for handling initial conditions. These methods are valuable tools in scientific computing for their accuracy and efficiency in solving complex problems.

## Weighted Residual Methods

Weighted residual methods are based on the idea of minimizing the residual (the error) of the approximation over the domain. The general form of a weighted residual method can be written as:

$\int_{\Omega} w_i(x) R(x) \, dx = 0$

where ( $w_i(x)$ ) are the weight functions, ( $R(x)$ ) is the residual, and ( $\Omega$ ) is the domain of the problem.

### Methods Included

1. **Collocation Method:**
   - The collocation method involves choosing specific points (collocation points) in the domain and enforcing that the residual is zero at these points. This method is straightforward and easy to implement but may not be as accurate as other methods for certain types of problems.

2. **Galerkin Method:**
   - The Galerkin method uses the basis functions themselves as the weight functions. This method ensures that the residual is orthogonal to the space spanned by the basis functions, often leading to highly accurate solutions.

3. **Least Squares Method:**
   - The least squares method minimizes the integral of the square of the residual over the domain. This approach can be more stable and accurate for problems where the residual may not be uniformly small.

4. **Subdomain Method:**
   - The subdomain method divides the domain into smaller subdomains and minimizes the residual in each subdomain separately. This approach can be particularly effective for problems with varying behavior across the domain.

5. **Ritz Method:**
   - The Ritz method is similar to the Galerkin method but is specifically used for variational problems. It involves choosing trial functions that satisfy boundary conditions and minimizing a functional, often leading to highly accurate solutions.

## Repository Structure

The repository is structured as follows:

```
├── ODE
   ├── collocation.py
   ├── galekin.py
   ├── least_squares.py
   ├── subdomain.py
   ├── ritz_collocation.py
├── PDE
   ├── collocation.py
   ├── galekin.py
   ├── least_squares.py
   ├── subdomain.py
   ├── ritz_collocation.py
├── README.md
```

Each Python script contains an implementation of the respective method, along with examples demonstrating how to use the method to solve differential equations.

## Contributing

Contributions to this repository are welcome. If you have an improvement or a new method to add, please fork the repository and create a pull request.

## License

This repository is licensed under the MIT License. See the `LICENSE` file for more details.

## References

- Boyd, J. P. (2001). Chebyshev and Fourier Spectral Methods. Dover Publications.
- Canuto, C., Hussaini, M. Y., Quarteroni, A., & Zang, T. A. (2006). Spectral Methods: Fundamentals in Single Domains. Springer.
- Trefethen, L. N. (2000). Spectral Methods in MATLAB. SIAM.
