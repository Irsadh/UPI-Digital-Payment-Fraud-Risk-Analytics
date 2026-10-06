# DAX Measures

## Total Transactions

```DAX
Total Transactions =
COUNTROWS(Fact_Transactions)

Total Transaction Value
Total Transaction Value =
SUM(Fact_Transactions[amount (INR)])

Average Transaction Value
Average Transaction Value =
AVERAGE(Fact_Transactions[amount (INR)])

Successful Transactions
Successful Transactions =
CALCULATE(
    [Total Transactions],
    Fact_Transactions[transaction_status] = "Success"
)

Failed Transactions
Failed Transactions =
CALCULATE(
    [Total Transactions],
    Fact_Transactions[transaction_status] = "Failed"
)

Success Rate
Success Rate =
DIVIDE(
    [Successful Transactions],
    [Total Transactions],
    0
)

Fraud Transactions
Fraud Transactions =
CALCULATE(
    [Total Transactions],
    Fact_Transactions[fraud_flag] = 1
)

Non-Fraud Transactions
Non-Fraud Transactions =
CALCULATE(
    [Total Transactions],
    Fact_Transactions[fraud_flag] = 0
)

Fraud Rate
Fraud Rate =
DIVIDE(
    [Fraud Transactions],
    [Total Transactions],
    0
)
Fraud Transaction Value
Fraud Transaction Value =
CALCULATE(
    SUM(Fact_Transactions[amount (INR)]),
    Fact_Transactions[fraud_flag] = 1
)

Fraud Amount Rate
Fraud Amount Rate =
DIVIDE(
    [Fraud Transaction Value],
    [Total Transaction Value],
    0
)

Average Fraud Transaction Value
Average Fraud Transaction Value =
DIVIDE(
    [Fraud Transaction Value],
    [Fraud Transactions],
    0
)