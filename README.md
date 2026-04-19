# NIFTY 50 Value-at-Risk (VaR) Modeling and Backtesting

## Overview
This repository develops an empirical market risk framework for the NIFTY 50 through Value-at-Risk (VaR) estimation and backtesting on daily log returns. The study evaluates the calibration and reliability of alternative VaR methodologies under non-normal return distributions, volatility clustering, and rolling out-of-sample forecasting.

## Research Objective
To estimate and compare one-day 99% VaR for the NIFTY 50 using multiple established methodologies, assess their statistical validity under real market conditions, and identify which framework most accurately captures downside risk in the Indian equity market.

## Data
- **Asset:** NIFTY 50 Index  
- **Market:** Indian large-cap equities  
- **Frequency:** Daily  
- **Sample Period:** 2014–2023  
- **Input Series:** Daily closing prices  
- **Transformation:** Logarithmic returns  

## Methodological Framework
- **Risk Measure:** One-day Value-at-Risk (VaR)  
- **Confidence Level:** 99%  
- **Estimation Window:** 500 trading days  
- **Forecast Design:** Rolling one-step-ahead forecasting  
- **Evaluation Horizon:** Out-of-sample backtesting  

## Models Implemented
1. **Variance–Covariance (Parametric VaR)**  
2. **Exponentially Weighted Moving Average (EWMA)**  
3. **GARCH(1,1)**  
4. **Historical Simulation**  
5. **Monte Carlo Simulation**  

## Empirical Analysis
- Data cleaning and return construction  
- Exploratory analysis of return dynamics  
- Descriptive statistics  
- Skewness and kurtosis diagnostics  
- Formal normality testing  
- Model-specific VaR estimation  
- Rolling out-of-sample forecasting  
- Comparative backtesting and calibration assessment  

## Backtesting and Statistical Validation
- **Exception (breach) analysis**  
- **Kupiec Proportion of Failures (POF) test**  
- **Binomial Z-test**  

A model is considered well-calibrated when the observed exception frequency is consistent with the theoretical 1% benchmark and statistical tests fail to reject the model.

## Principal Findings
- Return distributions exhibit negative skewness and excess kurtosis  
- Financial returns display fat tails and volatility clustering  
- Normality-based parametric VaR models systematically underestimate tail risk  
- Historical Simulation demonstrates superior empirical calibration under fat-tailed conditions  

## Interpretation
Distributional realism dominates analytical convenience in market risk measurement. Under asymmetric, heavy-tailed, and heteroskedastic return dynamics, empirically grounded approaches provide more reliable VaR estimates than Gaussian-based parametric models.

## Repository Structure<img width="950" height="421" alt="image" src="https://github.com/user-attachments/assets/f861a4c8-b218-4cab-bce4-aabfeaa09cb4" />
nifty50-var-modeling/
│
├── data/ # raw and processed datasets
├── notebooks/ # exploratory analysis, model development, validation
├── src/ # model implementations and backtesting logic
├── results/ # figures, tables, outputs
├── README.md
└── requirements.txt


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
