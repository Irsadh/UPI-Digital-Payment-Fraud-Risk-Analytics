# UPI Digital Payment Fraud Detection & Transaction Risk Analytics

A Power BI data analytics project that analyzes 250,000 UPI/digital payment transactions to understand transaction performance, payment success, transaction value, and fraud-risk patterns.

## 📌 Project Overview

This project analyzes transaction-level digital payment data using Power BI, Power Query, DAX, and data modeling.

The project focuses on:

- Transaction volume and value
- Successful and failed transactions
- Fraudulent transactions
- Fraud rate and fraud amount rate
- Fraud by transaction type
- Fraud by merchant category
- Fraud by sender state
- Fraud by device type
- Business insights and recommendations

> **Note:** The dataset is used for analytical and educational purposes. The results should not be interpreted as official nationwide UPI statistics.

## 🎯 Project Objectives

- Analyze overall transaction performance
- Measure transaction volume and transaction value
- Evaluate transaction success and failure
- Identify fraudulent transaction patterns
- Analyze fraud across different dimensions
- Build an interactive Power BI dashboard
- Generate business insights and recommendations

## 📊 Dataset

- **Records:** 250,000 transactions
- **Period:** 2024
- **Minimum Timestamp:** 01-01-2024 00:05:10
- **Maximum Timestamp:** 30-12-2024 23:55:40
- **Minimum Transaction Amount:** ₹10
- **Maximum Transaction Amount:** ₹42,099
- **Average Transaction Amount:** ₹1,311.76
- **Fraud Transactions:** 480
- **Non-Fraud Transactions:** 249,520

## 🛠️ Tools & Technologies

- Power BI Desktop
- Power Query
- DAX
- Data Modeling
- Data Visualization

## 🔄 Project Workflow

```text

Raw Dataset
     ↓
Data Cleaning & Validation
     ↓
Power Query Transformation
     ↓
Calendar Table
     ↓
Data Modeling
     ↓
DAX Measures
     ↓
Power BI Dashboard
     ↓
Fraud Analysis
     ↓
Business Insights
     ↓
Recommendations

🧹 Data Cleaning & Validation
Power Query was used for data preparation and validation.
Key activities:
- Data type validation
- Missing-value checks
- Error checks
- Transaction ID validation
- Categorical-value validation
- Numeric-value validation
- Date/time validation
Data Quality Results
Check	Result
Valid values	100%
Errors	0%
Empty values	0%
Distinct Transaction IDs	250,000

🗂️ Data Model
A dedicated Calendar table was created for time-based analysis.
Calendar
    │
    │ 1 : *
    │
Fact_Transactions
The Calendar table supports:
- Year analysis
- Month analysis
- Chronological sorting
- Date filtering
- Time-based analysis

📐 DAX Measures
Key measures created:
- Total Transactions
- Total Transaction Value
- Average Transaction Value
- Successful Transactions
- Failed Transactions
- Success Rate
- Fraud Transactions
- Non-Fraud Transactions
- Fraud Rate
- Fraud Transaction Value
- Fraud Amount Rate
- Average Fraud Transaction Value

📊 Power BI Dashboard
Page 1 — UPI Transaction Overview
KPI Cards:
- Total Transactions: 250K
- Total Transaction Value: ₹81.98T
- Average Transaction Value: ₹1.31K
- Success Rate: 95.0%
Visuals:
- Monthly UPI Transaction Volume
- Transactions by Transaction Type
- Transactions by Merchant Category
Slicers:
- Sender State
- Transaction Type
- Month
Page 2 — Fraud & Risk Analysis
KPI Cards:
- Fraud Transactions: 480
- Fraud Rate: 0.192%
- Fraud Transaction Value: approximately ₹720K
- Average Fraud Transaction Value: approximately ₹1.50K
Visuals:
- Fraud Transactions by Transaction Type
- Fraud Transactions by Merchant Category
- Fraud Transactions by Sender State
- Fraud Transactions by Device Type
Slicers:
- Sender State
- Transaction Type
- Device Type

🔎 Key Findings
Fraud by Transaction Type
Transaction Type	Fraud Transactions
P2P	206
P2M	167
Bill Payment	77
Recharge	30


P2P represents approximately 42.9% of flagged fraud transactions.
P2P and P2M together represent approximately 77.7% of flagged fraud transactions.
Fraud by Merchant Category
- Grocery: 94
- Food: 73
- Shopping: 62
Fraud by Sender State
- Maharashtra: 71
- Karnataka: 69
- Uttar Pradesh: 52
- Delhi: 50
Fraud by Device Type
- Android: 364
- iOS: 90
- Web: 26
Android represents approximately 75.8% of flagged fraud transactions.
These findings describe patterns within this project dataset and should not be interpreted as evidence that a particular state, device, or transaction type is inherently fraudulent.

💡 Business Insights
1. P2P is the largest contributor to flagged fraud transactions.
2. P2P and P2M together account for approximately 77.7% of flagged fraud records.
3. Grocery has the highest flagged fraud count among merchant categories.
4. Maharashtra and Karnataka show the highest flagged transaction concentrations among the listed states.
5. Android accounts for the largest share of flagged fraud transactions.
6. The fraud amount rate (0.219%) is slightly higher than the fraud transaction rate (0.192%).

🚀 Business Recommendations
1. Strengthen risk monitoring for P2P transactions.
2. Prioritize additional risk controls for P2P and P2M transaction flows.
3. Increase monitoring of high-volume/high-fraud merchant categories such as Grocery and Food.
4. Use device-level information as one input for fraud risk scoring.
5. Use targeted risk-based monitoring rather than blanket transaction blocking.

🔮 Future Enhancements
- Real-time transaction monitoring
- Automated fraud alerts
- Risk scoring
- Machine learning-based fraud prediction
- Anomaly detection
- Behavioral transaction analysis
- Automated Power BI refresh

📁 Project Structure
UPI-Digital-Payment-Fraud-Risk-Analytics/
│
├── 01_Data/
│   ├── Raw/
│   └── Processed/
│
├── 02_PowerBI/
│   └── UPI_Digital_Payment_Fraud_Risk_Analytics.pbix
│
├── 03_DAX/
│
├── 04_Documentation/
│
├── 05_Presentation/
│
├── 06_Screenshots/
│
└── README.md
The raw dataset is not included in the public repository unless its distribution/license terms permit redistribution.

📌 Project Outcome
This project demonstrates an end-to-end data analytics workflow:
Data → Cleaning → ETL → Data Modeling → DAX → Visualization → Fraud Analysis → Business Insights → Recommendations
The project demonstrates practical experience with Power BI, Power Query, DAX, data modeling, data validation, interactive dashboards, and business-oriented data analysis.

👨‍💻 Author
Mohamed Irsadh
Artificial Intelligence and Data Science Graduate
Aspiring Data Analyst / Data Analytics Professional
