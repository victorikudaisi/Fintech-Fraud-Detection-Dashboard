# Fintech Fraud Detection Dashboard
## Project Overview

This project presents a comprehensive fraud detection analysis built entirely in Microsoft Excel. It explores 50,000 financial transactions to uncover patterns, risk indicators, and behavioral trends associated with fraudulent activity — providing actionable insights for fraud analysts, fintech teams, and data-driven decision-makers.

The dashboard was designed with interactivity in mind, featuring slicers for transaction type and size, enabling dynamic filtering across all visual components.


## Dashboard Preview
Key Insights
1. Fraud by Transaction Type
- **CASH_OUT** had the highest volume (25,456 transactions) with 57 fraud cases
- **TRANSFER** transactions showed a disproportionately high fraud-to-volume ratio; 55 fraud cases out of only 7,219 transactions, making it the **highest-risk transaction type per volume**
- **CASH_IN** recorded zero fraud cases, consistent with the low-risk nature of inbound transactions

2. Fraud by Transaction Size
- **Large transactions** account for **42%** of all fraud cases
- Medium transactions represent **58%**, and Small just **12%**
- This pattern suggests fraudsters deliberately target medium-value transactions to maximize gain per incident

3. Fraud by Time Step
- Fraud activity peaks at **time steps 1, 6, and 8–9**, indicating non-random, cyclical fraud patterns
- These spikes could correlate with specific business hours, batch processing windows, or system vulnerabilities worth investigating further

4. Financial Impact
- Despite a low 0.22% fraud rate, the dollar impact is severe at **$61.6M lost**
- This highlights that frequency alone is not a reliable indicator of risk — transaction value must be weighted in any fraud scoring model


## Tools & Techniques Used
- Microsoft Excel: Dashboard design, data modeling, and visualization
- Pivot Tables & Pivot Charts: Dynamic data aggregation
- Slicers: Interactive filtering by transaction type (CASH_IN, CASH_OUT, TRANSFER) and transaction size (Large, Medium, Small)
- Conditional Formatting: Visual emphasis on anomalies
- KPI Cards: Summary metrics for executive-level readability
- Line, Bar & Pie Charts: Multi-dimensional fraud pattern visualization


## Recommendations
Based on the analysis, the following actions are suggested:

1. Prioritize TRANSFER monitoring: Implement stricter verification for transfer transactions given their high fraud ratio relative to volume
2. Flag medium transactions automatically: Since 58% of fraud involves large amounts, real-time alerts for high-value transactions should be a baseline control
3. Investigate time step spikes: Analyze what occurs at steps 1, 6, and 8–9 operationally; consider tighter controls or additional authentication during these windows
4. Build a fraud scoring model: Combine transaction type, size, and time step as features in a predictive risk model


## Dataset

The dataset simulates financial transactions from **Paysim**, a mobile money fraud simulation tool based on real anonymized transaction data. It is widely used in fraud detection research and data analytics portfolios.

- Source: Paysim Synthetic Financial Dataset
- Records: 50,000 transactions
- Fields include: Transaction type, amount, origin/destination account balances, fraud label, time step


## License

This project is open for portfolio and educational use. Feel free to fork, reference, or build upon it with attribution.
