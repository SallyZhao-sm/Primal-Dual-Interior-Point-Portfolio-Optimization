# MIE1621---Interior Point Method for Portfolio Optimization
Implemented a Predictor-Corrector Primal-Dual Interior Point Method to solve portfolio optimization as a convex quadratic program. Compared results with MATLAB quadprog/Python CVXPY. Demonstrated numerical stability on small cases with near-degenerate covariance and scalability to large dimensions (up to n=2000).

This project implements a Predictor-Corrector Primal-Dual Interior Point Method (IPM) to solve portfolio optimization formulated as a convex quadratic program. The algorithm was tested on both small and large-scale cases and compared with MATLAB `quadprog` and Python CVXPY solvers.

## Problem Setup
- Portfolio optimization with:
  - Risk aversion parameter (δ in [3.5, 4.5])
  - Non-negativity and budget constraints
- Objective: minimize risk-adjusted variance while meeting investment constraints

## Methods
- Part 1: Implemented IPM on a 3-asset portfolio with near-degenerate covariance to test numerical stability
- Part 2: Extended to larger portfolios (n = 5, 10, 20, 50, 100, 1000, 2000) with positive definite covariance matrices
- Benchmarked results against MATLAB `quadprog` and Python `cvxpy`

## Results
- Small-scale test: IPM and `quadprog` achieved close objective values, though solutions differed due to nearly singular covariance
- Large-scale test: IPM scaled efficiently and produced consistent solutions across all problem sizes
- Demonstrated robustness, accuracy, and computational efficiency for convex QP in financial optimization

## Skills Demonstrated
- Convex optimization and quadratic programming
- Implementation of advanced numerical algorithms (Predictor-Corrector IPM)
- Financial applications of optimization in portfolio selection
- Cross-validation using multiple solvers (MATLAB, Python)

