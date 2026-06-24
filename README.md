# Complexity-Based Market Regime Detection for Dynamic Asset Allocation

## Overview
This repository outlines a complexity-based market regime detection framework for dynamic asset allocation between Indian equities (NIFTYBEES) and 5-year Government Securities (GILT5YBEES). Moving beyond traditional stationary models and mean-variance optimization, this project characterizes the underlying geometry and computational structure of market dynamics using nonlinear invariants. 

## Mathematical Framework & Methodology
The classification framework is grounded in computational universality, mapping financial time series into three distinct regimes based on a multidimensional state vector. The core complexity metrics include:

* **Hurst Exponent (H):** Quantifies long-range dependence and fractional dimensionality via Rescaled Range (R/S) analysis.
* **Largest Lyapunov Exponent (LLE):** Measures the mean exponential rate of phase-space trajectory divergence to detect the collapse of the predictability horizon.
* **Sample Entropy (SampEn):** Evaluates sequential irregularity, functioning as a robust indicator of structural disorder and crash-entropy collapses.
* **Lag-1 Autocorrelation (Rho):** Captures short-term linear memory and market microstructure shifts.

### Regime Taxonomy
Instead of traditional directional labels (bull/bear), the market is classified into actionable dynamical structures:
1. **State 0 (Equilibrium):** Mean-reverting, low complexity.
2. **State 1 (Complete Chaos):** High entropy, weak predictability. Triggers a sharp reduction in equity exposure and a rotation into defensive sovereign bonds.
3. **State 2 (Edge-of-Chaos / Momentum):** Persistent, information-rich dynamics. Signals maximum equity exposure.

## Out-of-Sample Performance (Jan 2023 – May 2026)
The model was calibrated entirely in-sample (2014–2022) with a strict 6-month embargo period to prevent information leakage. The out-of-sample walk-forward test includes a volatility-targeting overlay, a regime-persistence filter, and a highly realistic NSE transaction-cost model (incorporating STT, Stamp Duty, GST, and Exchange charges).

| Performance Metric | Regime-Aware Strategy | Buy & Hold (NIFTYBEES) |
| :--- | :--- | :--- |
| **Annualized Return** | 13.53% | 9.62% |
| **Annualized Sharpe Ratio** | 1.33 | 0.83 |
| **Maximum Drawdown** | -10.51% | -15.23% |
| **Calmar Ratio** | 1.29 | 0.63 |

**Key Findings:** The strategy successfully mitigated risk by autonomously reducing NIFTYBEES exposure during detected "State 1" chaotic regimes, halving the maximum drawdown and significantly boosting risk-adjusted returns (Sharpe ratio of 1.33) relative to a passive benchmark.

## Intellectual Property Notice
**Note:** This repository serves as a high-level research showcase. To protect the author's intellectual property, the core algorithmic pipeline, proprietary scoring classification thresholds, and complete backtesting engine code have been restricted or abstracted. 

**Author:** Ritik Rakesh  
**Contact:** ritik.r@ahduni.edu.in | ritikrakesh111@gmail.com | realritikrakesh@gmail.com
