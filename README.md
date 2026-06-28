# 📊 Market Risk Modelling using Value-at-Risk (VaR) and Expected Shortfall (ES)

## Overview

This project presents a comprehensive market risk modelling framework for estimating and comparing the downside risk of major Indian equity sectoral indices. It implements multiple Value-at-Risk (VaR) estimation techniques, Expected Shortfall (ES), volatility forecasting using GARCH models, and statistical backtesting to evaluate model performance.

In addition to analysing individual indices, the project constructs a diversified portfolio and compares its risk profile with the constituent sectors to study the impact of diversification.


## Dataset

Historical daily closing prices of the following indices were collected and used for analysis:

* Nifty Auto
* Nifty Financial Services
* Nifty IT

Daily logarithmic returns were computed and used for all risk modelling techniques.


## Objectives

* Estimate daily Value-at-Risk (VaR) using multiple methodologies.
* Calculate Expected Shortfall (ES) for tail-risk measurement.
* Forecast conditional volatility using GARCH models.
* Compare different VaR estimation techniques.
* Validate VaR models through statistical backtesting.
* Analyse sector-wise risk characteristics.
* Perform portfolio-level risk analysis and evaluate diversification benefits.


## Methodology

### 1. Historical Simulation

* Uses historical return distributions.
* Makes no assumption about return distribution.
* Estimates VaR directly from historical observations.

### 2. Parametric (Variance-Covariance) VaR

* Assumes returns follow a normal distribution.
* Uses estimated mean and standard deviation.
* Computes analytical VaR at specified confidence levels.

### 3. Monte Carlo Simulation

* Generates thousands of simulated return paths.
* Estimates VaR from simulated return distributions.
* Captures uncertainty through repeated random sampling.

### 4. GARCH-Based VaR

* Models time-varying market volatility.
* Forecasts conditional variance using GARCH.
* Produces dynamic VaR estimates that adapt to changing market conditions.


## Expected Shortfall (ES)

Expected Shortfall (Conditional VaR) measures the average loss when losses exceed the VaR threshold. Unlike VaR, ES captures the magnitude of extreme losses and provides a more informative measure of tail risk.

## Portfolio Risk Analysis

A diversified portfolio was constructed using the three sectoral indices.

Portfolio-level Value-at-Risk (VaR) and Expected Shortfall (ES) were calculated and compared with those of the individual sectors to assess the impact of diversification on downside risk.

## VaR Backtesting

The predictive performance of each VaR model was evaluated using industry-standard statistical tests:

### Kupiec's Proportion of Failures (POF) Test

Evaluates whether the observed number of VaR violations matches the expected number.

### Christoffersen's Conditional Coverage Test

Tests both the frequency and independence of VaR violations to assess overall model adequacy.


## Technologies Used

* Python
* Pandas
* NumPy
* SciPy
* Matplotlib
* Statsmodels
* ARCH
* Jupyter Notebook


## Project Workflow

1. Collect historical market data.
2. Calculate daily log returns.
3. Estimate VaR using:

   * Historical Simulation
   * Parametric Method
   * Monte Carlo Simulation
   * GARCH Model
4. Compute Expected Shortfall.
5. Perform VaR Backtesting.
6. Construct diversified portfolio.
7. Compute Portfolio VaR and ES.
8. Compare sector-wise and portfolio risk.
9. Interpret diversification benefits.


## Key Results

* Successfully estimated Value-at-Risk (VaR) using four different methodologies.
* Calculated Expected Shortfall (ES) for all sectoral indices.
* Forecasted market volatility using GARCH models.
* Validated VaR estimates using Kupiec's and Christoffersen's statistical backtesting methods.
* Compared downside risk across Nifty Auto, Nifty Financial Services, and Nifty IT.
* Constructed a diversified portfolio and evaluated its overall market risk.
* Observed that the portfolio exhibited lower VaR and Expected Shortfall than the most volatile individual sector, demonstrating the benefits of diversification in reducing downside risk.


## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/Market-Risk-Modelling.git
```

Install the required packages:

```bash
pip install -r requirements.txt
```

Run the Jupyter Notebook:

```bash
jupyter notebook
```


## Future Enhancements

* Extreme Value Theory (EVT)-based VaR estimation
* Multi-asset portfolio optimisation
* Rolling-window risk forecasting
* Stress testing under extreme market scenarios
* Interactive dashboard using Streamlit or Dash
* Real-time market risk monitoring
