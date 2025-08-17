# Portfolio Risk Analysis

This project performs a **risk analysis of a multi-asset portfolio** using both **historical simulation** and **parametric methods** to estimate **Value at Risk (VaR)** and **Expected Shortfall (ES)**.  

---

## 🔎 Analysis Overview
The notebook includes the following steps:

- **Data Loading and Preparation**  
  - Load stock price data  
  - Calculate daily returns for individual stocks and the overall portfolio  
  
- **Time Series Analysis**  
  - Check for stationarity using **ADF** and **KPSS** tests  

- **ARIMA Model Fitting**  
  - Identify and fit an appropriate **ARIMA model** based on AIC criteria  

- **Model Validation**  
  - Perform residual analysis  
  - Conduct **Ljung-Box tests** to check adequacy of the fitted model  

- **Volatility Modeling (GARCH)**  
  - Fit **GARCH-type models** to capture volatility clustering  
  - Forecast future volatility  

- **Value at Risk (VaR) and Expected Shortfall (ES) Estimation**  
  - 1-day and 10-day VaR & ES using **Historical Simulation**  
  - 10-day VaR & ES using **Parametric approach** (ARIMA for mean, GARCH for volatility)  

- **Diversification Benefit Analysis**  
  - Compare portfolio risk measures with the weighted sum of individual stock risks  
  - Quantify the benefits of diversification  

---

## 📂 Files
- `portfolio_risk_analysis.ipynb` → Jupyter Notebook containing the analysis code  
- `Portfolio_returns.xlsx` → Excel file with stock price data  

---

## ⚙️ Requirements
The following Python libraries are required:

```bash
pip install pandas numpy matplotlib statsmodels arch
