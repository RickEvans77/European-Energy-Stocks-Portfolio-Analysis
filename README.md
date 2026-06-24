# European Energy Stocks Portfolio Analysis

A quantitative portfolio analysis of major European energy companies using risk metrics, portfolio optimization, and volatility analysis.

## Motivation

This project was built to explore how quantitative portfolio management techniques can be applied to the European energy sector. The objective is to evaluate the risk-return characteristics of energy stocks, identify efficient portfolio allocations, and analyze how market shocks affect asset volatility over time.

## What the Project Does

The analysis is divided into four main stages:

### 1. Data Pipeline

Historical daily price data is collected using Yahoo Finance for a portfolio of major European energy companies:

* E.ON (EOAN.DE)
* Iberdrola (IBE.MC)
* TotalEnergies (TTE.PA)
* BP (BP.L)
* Engie (ENGI.PA)
* Equinor (EQNR.OL)

The dataset is cleaned by handling missing observations and transformed into daily logarithmic returns for further analysis.

### 2. Risk Metrics

Several standard portfolio risk measures are calculated:

* Daily logarithmic returns
* Value at Risk (VaR) at the 95% confidence level
* Annualized volatility
* Sharpe Ratio

These metrics provide insight into downside risk, return consistency, and risk-adjusted performance.

### 3. Portfolio Optimization

A Monte Carlo simulation generates thousands of random portfolios with different asset allocations.

For each portfolio, the following are computed:

* Expected annual return
* Annualized volatility
* Sharpe Ratio

The efficient frontier is constructed, and the portfolio with the highest Sharpe Ratio is identified as the optimal risk-adjusted allocation.


### 4. Rolling Volatility Analysis

A 30-day rolling volatility measure is calculated and annualized to examine how risk evolves over time.

This allows the identification of periods of market stress and comparison of the stability of different energy companies.

## Key Findings

* The COVID-19 market shock generated a clear volatility spike across all energy stocks, highlighting the sector's sensitivity to macroeconomic disruptions.
* Engie and BP exhibited some of the strongest return opportunities, but these gains were accompanied by higher volatility and risk.
* Iberdrola consistently displayed lower volatility than most peers, reflecting its more defensive risk profile within the energy sector.
* Portfolio diversification significantly reduced overall risk compared with holding individual stocks.
* The efficient frontier demonstrated that carefully chosen allocations can improve risk-adjusted returns relative to naive equal-weight portfolios.

## Tech Stack

* Python
* pandas
* numpy
* yfinance
* matplotlib

## How to Run

1. Clone the repository and open the Jupyter Notebook (`Asset Management Energy 06.2026.ipynb`).
2. Run all notebook cells sequentially to download the data, compute the risk metrics, generate the portfolio optimization results, and visualize rolling volatility.
