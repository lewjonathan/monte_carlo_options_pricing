# Monte Carlo Option Pricing: GBM, Euler–Maruyama, and Milstein

This project summarizes a Monte Carlo derivatives-pricing study comparing numerical simulation methods for European and binary call options under Geometric Brownian Motion (GBM).

The project compares exact terminal GBM simulation, Euler–Maruyama discretization, and the Milstein scheme against Black–Scholes closed-form benchmarks. The research focus is on pricing error, RMSE, weak convergence intuition, bias behavior, Monte Carlo standard error, and runtime tradeoffs.

## Note on Redaction

This repository contains a public redacted summary. The original research notebook, plots, parameter sweeps, and detailed numerical outputs are omitted to avoid sharing assessment-specific materials.

The full notebook is not publicly distributed, but I can discuss the methodology, validation logic, and implementation decisions in an interview setting.

## Methods

- Black–Scholes closed-form benchmark
- Exact terminal GBM simulation
- Euler–Maruyama discretization
- Milstein discretization
- Monte Carlo standard error analysis
- Weak convergence diagnostics
- Bias and RMSE comparison
- Cost-accuracy analysis

## Option Types

- European call option
- Binary call option

## Key Findings

Exact terminal GBM simulation is preferred when available because it avoids time-discretization error.

For European options, higher-order schemes such as Milstein can improve accuracy relative to Euler–Maruyama, though any practical gain must be weighed against computational cost and Monte Carlo sampling error.

For binary options, the discontinuous payoff makes convergence behavior less stable. This reinforces that theoretical convergence order does not automatically translate into better practical pricing performance for nonsmooth payoffs.

## Technologies Used

- Python
- NumPy
- pandas
- Matplotlib
- SciPy
- Jupyter Notebook

## Project Files

- `README.md` — public redacted project summary

## References

This project draws on standard numerical finance and Monte Carlo methods, including Glasserman, Higham, Kloeden & Platen, and related work on Monte Carlo simulation and stochastic differential equations.
