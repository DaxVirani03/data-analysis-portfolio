<details>
  <summary><strong>💼 Portfolio Risk Analysis & Financial Metrics</strong></summary>

### 📘 Overview  
In this project, I analyzed a portfolio of five major tech stocks — **Tesla (TSLA), Apple (AAPL), Google (GOOGL), Microsoft (MSFT), and Amazon (AMZN)** — using historical price data from Jan 1, 2020 to May 29, 2025. My goal was to understand the portfolio's **financial risk** using metrics like Value at Risk (VaR), Expected Shortfall (ES), Sharpe Ratio, and more.

I also ran a **Monte Carlo simulation** to predict possible future outcomes and tested if the portfolio returns follow a normal distribution using the **Jarque-Bera test**.

---

### 🎯 Objectives  
- Get stock price data (via `yfinance`, with `pandas_datareader` as backup)  
- Build an **equally weighted portfolio** (20% per stock)  
- Calculate:
  - Log returns
  - **VaR** (Value at Risk)
  - **ES** (Expected Shortfall)
  - **Sharpe Ratio**
  - (Planned) **Maximum Drawdown (MDD)**
- Run a **Monte Carlo simulation** for forecasting  
- Perform a **normality test** on portfolio returns  
- Visualize 60-day rolling VaR

---

### 🛠️ Tools Used  
- **Environment**: Jupyter Notebook (Python 3.12.7)  
- **Libraries**: `numpy`, `pandas`, `matplotlib`, `seaborn`, `yfinance`, `pandas_datareader`, `scipy.stats`  
- **Data Source**: Yahoo Finance (fallback: Stooq)

---

### 📊 Methodology & Key Learnings

#### 📈 Data Handling  
- Used `yfinance` to pull stock prices  
- Switched to Stooq if yfinance failed  
- Filled missing values using forward and backward fill  

#### 📉 Risk Metrics  
- **Log Returns**: Calculated for daily price changes  
- **VaR (95%)**: Estimated portfolio losses in the worst 5% of cases  
- **Expected Shortfall (ES)**: ES was ~$12,540 for a $10K VaR  
- **Sharpe Ratio**: Calculated as 0.5556  
- **Monte Carlo Simulation**: Estimated a -15.61% return in one run  
- **Jarque-Bera Test**: Confirmed that returns **are not** normally distributed (p < 0.001)  

#### 📊 Visualization  
- Plotted **60-day rolling VaR** to monitor changing risk  
- Found minor bugs: `portR` and `VAR_norm` were undefined in the plot

---

### ⚠️ Issues & Fixes  
- `yfinance` error: was passing the whole list to `yf.Ticker` — fixed by looping each ticker individually  
- `portR` and `VAR_norm` were missing, which affected the VaR plot  
- Normality assumption (used for ES) may be invalid due to test results

---

### 🚀 Improvements & Future Work  
- Properly compute **Maximum Drawdown (MDD)**  
- Expand the Monte Carlo simulation to generate a distribution, not just one value  
- Consider using better risk models (like CVaR or t-distribution)  
- Validate consistency between Yahoo & Stooq data  
- Handle **non-trading days** more explicitly

---

### ▶️ How to Run  
1. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn yfinance pandas_datareader scipy
