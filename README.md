# Performance Insights: Ranking Binance Accounts with Key Financial Metrics
This repository offers an in-depth analysis of Binance trading accounts, leveraging key financial metrics to evaluate and rank account performance.

## Objective
The objective of this project is to analyze a dataset of Binance trade history, calculate essential financial metrics for each account, rank them based on performance, and present the top 20 accounts.

## Methodology
### 1. Data Import and Exploration
- **Data Source:** The dataset was imported from a CSV file containing trade history across various Binance accounts.
- **Exploration:** Initial exploration included examining the dataset's structure (shape, data types, statistical summaries) to gain a foundational understanding of its contents.
### 2. Data Cleaning
- **Parsing and Structuring:** Trade histories were parsed and flattened into a structured DataFrame (df_trades).
- **Integrity Checks:** Ensured no missing values in numeric columns; duplicate rows were identified and removed.
### 3. Data Visualization
- **Distributions:** Used box plots and count plots to visualize numeric and categorical variable distributions.
- **Correlation:** Generated a correlation matrix to explore relationships between numeric features.
### 4. Metrics Calculation
Key financial metrics were calculated for each account to gauge performance:

- **ROI (Return on Investment):** Calculated as the ratio of realized profit to investment.
- **PnL (Profit and Loss):** Total realized profit for each account.
- **Sharpe Ratio:** Calculated as the average return divided by the standard deviation of returns, representing risk-adjusted performance.
- **Maximum Drawdown (MDD):** Identified the largest peak-to-trough decline in cumulative returns.
- **Win Rate:** The ratio of profitable trades to total trades.
- **Win Positions:** Count of profitable trades.
- **Total Positions:** Total count of trades.
### 5. Feature Engineering
- **Feature Importance:** A Random Forest Regressor identified the importance of each metric.
- **Weighted Scoring System:** Feature importances were normalized and scaled, then combined to compute a final weighted score for each account.
### 6. Weight Adjustments
- **Impact of Weighting Schemes:** Analyzed how different weight combinations affect portfolio rankings and outcomes.
- **Key Metric Identification:** Explored the critical metrics for achieving investment goals and the effect of weight adjustments on rankings.
### 7. Visualizations
- **Performance:** Bar charts for weighted scores and scatter plots of ROI versus Sharpe Ratio to visualize returns and risk-adjusted performance.
- **Trends and Correlations:** Correlation heatmap to show relationships among metrics and time-series plots for PnL and ROI to reveal performance patterns over time.
### 8. Ranking Algorithm
- Accounts were ranked based on weighted scores, and the top 20 accounts were identified for further analysis and reporting.
## Findings
### 1. Data Overview
- **Trade Volume:** The dataset includes 211,277 trades across various accounts.
- **Average ROI:** Approximately 35.68% per trade, though an overall ROI of 0.00% suggests that losses often offset gains.
### 2. Performance Metrics
- **Win Rate:** Out of 200,026 positions, 79,473 were profitable, yielding a win rate of 39.73%.
- **Maximum Drawdown:** A peak-to-trough decline of -20.85%, indicating substantial risk in cumulative returns.
- **Sharpe Ratio:** Averaged at 0.043, suggesting relatively low risk-adjusted returns.
### 3. Top 20 Accounts
- **Top Accounts:** Ranked based on metrics like ROI, PnL, Sharpe Ratio, and Win Rate.
- **Leading Performance:** The highest-ranked account achieved a PnL of approximately 70,638.37, demonstrating significant profitability.
## Assumptions
- **Data Integrity:** Trade data accurately reflects account activity.
- **ROI Calculation:** Assumes all trades are closed and accurately represent realized profits.
- **Sharpe Ratio:** Considered a valid risk-adjusted metric, though it may not capture all trading risks.
- **Weighted Scoring:** The weights are subjective and could be refined with further analysis or domain expertise.
## Conclusion
This analysis provides a comprehensive ranking of Binance accounts, identifying top performers and key metrics such as win rate and drawdown. The findings can inform future trading strategies, highlighting areas for improvement in win rate and drawdown management. Further exploration could involve time series forecasting, deeper insight into trading strategies, and more granular metrics.
## Tools/Software:
### Data Handling and Visualization:
**Libraries -** numpy, pandas, ast, matplotlib, seaborn
### Machine Learning:
**Libraries -** Scikit-learn
## Files to be uploaded in the repository:
**1. Dataset -->** TRADES_CopyTr_90D_ROI.csv

**2. Code -->** Performance Insights- Ranking Binance Accounts with Key Financial Metrics.ipynb, TRADES_CopyTr_90D_ROI.csv, metrics_by_port_id.csv, Documentation Performance Insights - Ranking Binance Accounts with Key Financial Metrics.docx 
