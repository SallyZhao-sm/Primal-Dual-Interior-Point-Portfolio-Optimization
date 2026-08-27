# Primal-Dual Interior-Point Portfolio Optimization

## Overview

This project implements a predictor-corrector primal-dual interior-point method to solve portfolio optimization as a convex quadratic program. The custom solver is tested for numerical stability and scalability, then benchmarked against MATLAB `quadprog` and Python CVXPY.

## Problem Formulation

The portfolio model includes:

- A risk-aversion parameter between 3.5 and 4.5
- Nonnegative portfolio weights
- A full-investment budget constraint
- A risk-adjusted quadratic objective

## Methodology

- Implemented the predictor-corrector primal-dual algorithm
- Tested a three-asset case with a nearly singular covariance matrix
- Extended the solver to dimensions of 5, 10, 20, 50, 100, 1,000, and 2,000 assets
- Generated positive-definite covariance matrices for large-scale tests
- Compared objective values and solutions with `quadprog` and CVXPY

## Key Results

- The custom solver and `quadprog` produced close objective values in the small, nearly degenerate case.
- Different allocations in the small case illustrated the sensitivity created by a nearly singular covariance matrix.
- The implementation produced consistent solutions across problem sizes up to 2,000 assets.
- Benchmarking validated the accuracy and scalability of the numerical method.

## Technologies

Python, MATLAB, NumPy, CVXPY, quadratic programming, convex optimization, numerical algorithms
