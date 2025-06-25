<details>
  <summary><strong>📘 Portfolio Risk Analysis & Financial Metrics</strong></summary>

### 🧭 About the Project  
In this project, I analyzed a portfolio made up of five big tech stocks — Tesla, Apple, Google, Microsoft, and Amazon. I worked with historical data (from Jan 1, 2020 to May 29, 2025) and focused on calculating important financial risk metrics like Value at Risk (VaR), Expected Shortfall (ES), Sharpe Ratio, and more. I also simulated possible future returns and tested how normally distributed the returns were.

### 🎯 Main Goals  
- Collect historical stock data using Python libraries  
- Create an equally weighted portfolio (each stock 20%)  
- Calculate log returns and key risk metrics:  
  - VaR (Value at Risk)  
  - ES (Expected Shortfall)  
  - Sharpe Ratio  
  - (Mentioned but not calculated: Maximum Drawdown)  
- Run a Monte Carlo simulation for possible future performance  
- Use a statistical test (Jarque–Bera) to check for normality  
- Visualize 60-day rolling VaR to show how risk changes over time

### 🛠️ Tools & Libraries  
- **Environment**: Jupyter Notebook (Python 3.12.7)  
- **Libraries**: numpy, pandas, matplotlib, seaborn, scipy, yfinance, pandas_datareader  
- **Data Sources**: Yahoo Finance (primary), Stooq (fallback)

### 📊 Key Insights  
- The portfolio returns aren’t normally distributed (confirmed by Jarque–Bera test), which means traditional models may underestimate risk  
- ES (~$12,500) is higher than VaR ($10,000), showing that extreme losses can be larger than expected  
- Sharpe Ratio (~0.56) suggests moderate returns compared to risk  
- The Monte Carlo simulation gave a sample result of –15.6%, which shows uncertainty in future performance

### 🧪 What Could Be Improved  
- The code needs small fixes:  
  - yfinance error was due to how tickers were passed  
  - `portR` and `VAR_norm` weren’t defined in the visualization part  
- Better consistency checks between Yahoo and Stooq data  
- Future improvements can include:  
  - Calculating Maximum Drawdown  
  - Running multiple Monte Carlo simulations  
  - Trying out more advanced risk models like CVaR

### ▶️ How to Run  
1. Install required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn yfinance pandas_datareader scipy
