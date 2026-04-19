# NIFTY 50 Value-at-Risk (VaR) Modeling and Backtesting

## Overview
This repository implements and evaluates Value-at-Risk (VaR) models for the NIFTY 50 using daily logarithmic returns. The analysis examines model performance under non-normal return distributions, volatility clustering, and a rolling out-of-sample forecasting framework.

## Research Objective
To estimate and compare one-day 99% VaR for the NIFTY 50 using multiple established methodologies, evaluate their statistical calibration under real market conditions, and identify the models that most accurately capture downside risk in the Indian equity market.

## Data
- **Asset:** NIFTY 50 Index  
- **Market:** Indian large-cap equities  
- **Frequency:** Daily  
- **Sample Period:** 2014–2023  
- **Source Variable:** Closing prices  
- **Return Definition:** Logarithmic returns  

## Methodology
- **Risk Metric:** One-day Value-at-Risk (VaR)  
- **Confidence Level:** 99%  
- **Estimation Window:** 500 trading days  
- **Forecasting Scheme:** Rolling one-step-ahead  
- **Evaluation:** Out-of-sample backtesting  

## Models
1. **Variance–Covariance (Parametric VaR)**  
2. **Exponentially Weighted Moving Average (EWMA)**  
3. **GARCH(1,1)**  
4. **Historical Simulation**  
5. **Monte Carlo Simulation**  

## Empirical Analysis
- Data cleaning and logarithmic return construction  
- Exploratory analysis of return dynamics  
- Descriptive statistical analysis  
- Skewness and kurtosis diagnostics  
- D’Agostino–Pearson normality testing  
- Model-specific VaR estimation  
- Rolling-window one-step-ahead VaR forecasting  
- Comparative backtesting and calibration evaluation  

## Backtesting and Statistical Validation
- **Exception analysis**  
- **Kupiec Proportion of Failures (POF) test**  
- **Binomial Z-test**  

A model is considered statistically well-calibrated if the observed exception frequency is consistent with the theoretical 1% VaR level and the null hypothesis of correct coverage is not rejected by the applied statistical tests.

## Principal Findings
- NIFTY 50 daily logarithmic returns exhibit negative skewness and excess kurtosis  
- The return distribution is non-normal, characterized by fat tails and volatility clustering  
- Parametric VaR models based on normality assumptions underestimate downside tail risk  
- Historical Simulation demonstrates the most consistent empirical calibration among the models evaluated  

## Interpretation
The results indicate that accurate risk estimation is critically dependent on distributional specification. Under non-normal, fat-tailed, and heteroskedastic return dynamics, empirically driven approaches provide more reliable VaR estimates than Gaussian-based parametric models.

## Repository Structure
```
nifty50-var-modeling/
│
├── data/ # raw and processed data
├── notebooks/ # exploratory analysis and model development
├── src/ # model implementations and backtesting modules
├── results/ # figures, tables, and outputs
├── README.md
└── requirements.txt
```

## Technology Stack
- Python  
- pandas  
- numpy  
- scipy  
- statsmodels  
- arch  
- matplotlib  
- Jupyter Notebook  

## Scope
- NIFTY 50 index-level market risk  
- Daily frequency data  
- One-day VaR estimation  
- Rolling-window model comparison  

## Potential Extensions
The following extensions are prospective and are not implemented in the current study.

- Student-t and skewed distribution modeling  
- Expected Shortfall (CVaR)  
- Christoffersen conditional coverage testing  
- Stress testing frameworks  
- Multi-horizon VaR estimation  
- Portfolio-level risk aggregation  
- Machine learning-based risk modeling  

## Author
**Md Saif Akram**  
Quantitative Finance — Market Risk, VaR Modeling, and Volatility Analysis
