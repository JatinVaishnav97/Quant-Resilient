# Quant Resilient
A Computational Risk Analytics Engine for Quantitative Portfolio Stress Testing

---

## Overview

Quant Resilient is a research-oriented quantitative finance project designed to model portfolio risk under uncertain market conditions.  
The system combines statistical analysis, Monte Carlo simulation, and Conditional Value at Risk (CVaR) optimization to evaluate portfolio robustness and tail-risk exposure.

The goal of this project is to demonstrate how computational methods and mathematical modeling can be applied to financial risk management problems. It provides a modular architecture for analyzing historical price data, computing risk metrics, simulating stochastic market scenarios, and optimizing portfolio allocation.

This repository is intended as an educational and research-oriented implementation of core techniques used in quantitative finance and algorithmic risk analysis.

---

## Research Motivation

Financial markets exhibit complex dynamics characterized by volatility clustering, heavy-tailed distributions, and stochastic behavior. Traditional portfolio optimization approaches often underestimate extreme market risks.

This project explores computational approaches for evaluating **portfolio resilience**, focusing on:

- Modeling uncertainty using Monte Carlo simulation
- Measuring tail risk using Conditional Value at Risk (CVaR)
- Evaluating portfolio stability under simulated stress scenarios

Such techniques are widely used in **quantitative finance, hedge funds, and financial risk management systems**.

---

## Key Features

• Historical market data processing  
• Return and volatility computation  
• Monte Carlo simulation of asset price paths  
• Tail risk estimation  
• Conditional Value at Risk (CVaR) optimization  
• Portfolio risk statistics and analysis  
• Web-based interface for visualization  

---

## System Architecture

The project follows a modular architecture separating **data processing, quantitative engines, and interface components**.


Quant-Resilient
  │
  ├── frontend/
  
  │   ├── index.html
  
  │   ├── profile.html
  
  │   └── dashboard.html
  │
  ├── data/
  │   ├── prices.csv
  │   └── returns.csv
  │
  ├── engine/
  │   ├── cvar_optimization.py
  │   ├── get_data.py
  │   ├── monte_carlo.py
  │   ├── returns.py
  │   ├── risk_stats.py
  │   └── tail_risk.py
  │
  ├── main.py
  ├── requirements.txt
  └── README.md 


### Module Overview

**Data Layer**

Handles financial datasets used for analysis.

- `prices.csv` – historical asset prices
- `returns.csv` – computed return series

**Quantitative Engine**

Implements mathematical models and financial computations.

- `returns.py` – return calculations
- `risk_stats.py` – statistical risk metrics
- `monte_carlo.py` – stochastic simulation of asset prices
- `tail_risk.py` – tail-risk estimation methods
- `cvar_optimization.py` – portfolio optimization under CVaR constraints
- `get_data.py` – data loading and preprocessing

**Application Layer**

- `main.py` orchestrates the pipeline
- `frontend/` provides simple visualization dashboards

---

## Mathematical Concepts Used

The system relies on several fundamental quantitative finance concepts:

### Return Modeling
Asset returns are computed as:
                                      r_t = (P_t - P_{t-1}) / P_{t-1}

### Monte Carlo Simulation

Future asset prices are simulated using stochastic processes such as Geometric Brownian Motion:
                                            dS = μS dt + σS dW

Where:

- μ = drift
- σ = volatility
- dW = Wiener process

### Value at Risk (VaR)

VaR estimates the potential loss over a given time horizon at a specified confidence level.

### Conditional Value at Risk (CVaR)

CVaR measures the **expected loss beyond the VaR threshold**, providing a more robust tail-risk metric.
                                        CVaR = E[Loss | Loss > VaR]

This approach is widely used in **risk-sensitive portfolio optimization**.

---

## Installation
Clone the repository:
git clone https://github.com/yourusername/quant-resilient.git
cd quant-resilient

Install dependencies:
pip install -r requirements.txt

---

## Running the Project

Execute the main pipeline:
python main.py


This will:

1. Load financial data
2. Compute asset returns
3. Perform risk metric calculations
4. Run Monte Carlo simulations
5. Evaluate portfolio risk statistics

---

## Example Workflow

Typical workflow within the system:

1. Load historical price data
2. Compute asset return distributions
3. Estimate statistical risk measures
4. Simulate future market scenarios
5. Evaluate portfolio losses
6. Optimize allocations using CVaR

This workflow reflects the general structure of many **quantitative risk management pipelines**.

---

## Future Improvements

Possible extensions to this project include:

• Implementation of stochastic volatility models (Heston model)  
• Reinforcement learning for portfolio allocation  
• GPU acceleration for large-scale simulations  
• Integration with real-time financial APIs  
• Advanced optimization techniques (robust optimization, Bayesian portfolio models)  
• Interactive dashboards for visualization  

---

## Contributions

Contributions, improvements, and research discussions are welcome.  
Please open an issue or submit a pull request.

---

## License

This project is intended for educational and research purposes.
