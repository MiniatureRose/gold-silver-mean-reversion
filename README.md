# Gold-Silver Mean Reversion Strategy

This project implements a statistical arbitrage strategy using mean reversion between gold and silver prices. It relies on linear regression to model the relationship and identify trading opportunities based on deviations from the expected spread.

## Features

- Download historical data from Yahoo Finance
- Model gold-silver price relationship using linear regression
- Calculate residuals and derive z-scores
- Generate trading signals based on threshold crossings
- Walk-forward backtesting with rolling train/test windows
- Optimize Sharpe ratio by tuning signal threshold
- Visualizations of spread, signals, positions, and returns

## Strategy Logic

1. Fit a linear regression: Silver ~ β * Gold
2. Compute residuals (spread): Silver - β * Gold
3. When residuals exceed ±k * std:
   - Go long silver / short gold (if residual < -threshold)
   - Go short silver / long gold (if residual > threshold)
4. Exit position when residual crosses zero
5. Evaluate performance using Sharpe Ratio and cumulative return

## Getting Started

### 1. Clone the repository

git clone https://github.com/MiniatureRose/gold-silver-mean-reversion.git
cd gold-silver-mean-reversion

### 2. Install dependencies

pip install -r requirements.txt

Or install manually:

pip install pandas numpy matplotlib yfinance scikit-learn

### 3. Run the notebook

Launch the Jupyter Notebook and open:

mean_reversion_strategy.ipynb

## Requirements

- Python 3.7+
- pandas
- numpy
- matplotlib
- yfinance
- scikit-learn

## Author

Achraf JDIDI
