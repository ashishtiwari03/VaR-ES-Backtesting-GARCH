# VaR-ES-Backtesting-GARCH
# Backtesting Value-at-Risk and Expected Shortfall with GARCH-family models (t & skew-t) in R

This project implements and evaluates **Value-at-Risk (VaR)** and **Expected Shortfall (ES)** forecasts using GARCH-family models.  
The focus is on **GARCH(1,1)**, **APARCH(1,1)**, and **EGARCH(1,1)** with both **t-distribution** and **skewed t-distribution**.  
The work was done as part of the course *W4451-FEQRM Project – Summer Semester 2025*.

---

##  Project Overview
- **Data**: Daily closing stock prices of a company (2020–2024) from Yahoo Finance.  
- **Models**:  
  - GARCH(1,1)  
  - APARCH(1,1)  
  - EGARCH(1,1)  
- **Distributions**: t and skewed t  
- **Risk Level**: 97.5%  
- **Backtest**: Traffic-light test and violation counts  

---

##  Methods
1. Load and clean stock price data (2020–2024).  
2. Compute daily log-returns.  
3. Fit models on training data, leaving the last 250 observations for testing.  
4. Generate one-step rolling forecasts of 97.5% VaR and ES.  
5. Backtest forecasts using violation counts and traffic-light zones.  
6. Visualize returns vs VaR and ES, marking violations.  

---

##  Visualization of VaR and ES Backtests
The figures show daily log-returns (black) with forecasted **97.5% VaR (red dashed)** and **97.5% ES (blue dashed)**.  
Violations (returns falling below the thresholds) are highlighted with markers.  

Each model-distribution combination has its own plot.  
Example below (illustrative):  

![Example Plot](plots_backtests/GARCH_1_1_std_VaR.png)

---

##  Results
- Expected number of violations at 97.5% over 250 days ≈ 6–7.  
- Some models under- or over-estimate tail risk.  
- Skewed-t distributions often provide a better fit compared to symmetric t.  

See `summary_backtests.csv` for the consolidated results.  

---

## 📁 Repository Structure
