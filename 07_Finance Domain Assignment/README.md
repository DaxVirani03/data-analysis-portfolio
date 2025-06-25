<details>
  <summary><strong>📘 Portfolio Risk Analysis & Financial Metrics</strong></summary>

### 🧭 What I Did  
I analyzed a portfolio of five tech giants—Tesla, Apple, Alphabet (Google), Microsoft, and Amazon—using historical data from January 1, 2020, to May 29, 2025. I computed key risk and return metrics like Value at Risk (VaR), Expected Shortfall (ES), Maximum Drawdown (MDD), and Sharpe Ratio. I also ran a Monte Carlo simulation to forecast future returns and performed a Jarque–Bera test to check if the return distribution was normal. The goal was to offer insights for smarter portfolio management.

### 🎯 Objectives  
- Retrieve historical stock data (using `yfinance`, fallback to `pandas_datareader`)  
- Build an equally weighted portfolio (20% each)  
- Calculate log returns and key risk metrics (VaR, ES, Sharpe, MDD)  
- Run a Monte Carlo simulation to explore future returns  
- Perform the Jarque–Bera test  
- Visualize rolling 60-day VaR over time

### 🛠️ Tools & Environment  
Python 3.12.7 with numpy, pandas, matplotlib, seaborn, SciPy, yfinance, pandas_datareader (in Jupyter Notebook)

### 💡 Key Insights  
- Returns **aren’t normally distributed**, highlighting modeling limits  
- **ES (~$12.5K)** exceeds VaR ($10K), showing greater tail risk  
- **Sharpe (~0.56)** indicates moderate risk-adjusted performance  
- Monte Carlo highlights outcome uncertainty

### 🚀 Next Steps  
- Calculate **Maximum Drawdown (MDD)**  
- Run **multiple Monte Carlo simulations**  
- Explore **advanced risk models (e.g., CVaR)**  
- Improve data validation for non-trading days

### 📋 How to Run  
```bash
pip install pandas numpy matplotlib seaborn yfinance pandas_datareader scipy
