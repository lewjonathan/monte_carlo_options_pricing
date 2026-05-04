# Monte Carlo Option Pricing: GBM, Euler–Maruyama, and Milstein

This project implements and compares Monte Carlo methods for pricing European and binary call options under Geometric Brownian Motion (GBM).

The project compares exact terminal GBM simulation, Euler–Maruyama discretization, and the Milstein scheme against Black–Scholes closed-form benchmarks. It evaluates each method using pricing error, RMSE, weak convergence diagnostics, bias behavior, Monte Carlo standard error, and runtime tradeoffs.

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

For European options, Milstein can improve accuracy relative to Euler–Maruyama, although the gain comes with additional computational cost.

For binary options, the discontinuous payoff makes convergence behavior less stable. Euler–Maruyama showed more reliable weak convergence behavior in the tested setup, while Milstein sometimes achieved slightly lower RMSE at higher runtime cost.

## Technologies Used

- Python
- NumPy
- pandas
- Matplotlib
- SciPy
- Jupyter Notebook

## Project Files

- `Monte_Carlo_Option_Pricing.ipynb` — main notebook
- `README.md` — project overview
- `requirements.txt` — required Python packages

## References

This project draws on standard numerical finance and Monte Carlo methods, including Glasserman, Higham, Kloeden & Platen, and related work on Monte Carlo simulation and stochastic differential equations.
