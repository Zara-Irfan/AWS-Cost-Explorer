# FinOps AI - Cloud Cost Explosion Predictor

FinOps AI is a predictive analytics project designed to monitor and forecast cloud spending, detect anomalies, and alert users about potential cost spikes in cloud infrastructure. It can use either simulated billing data or real billing data exported from cloud providers like AWS, allowing both testing and production use.

Project Overview

The project contains a single main Python program that performs the following:

Data Generation and Loading:

Generates simulated billing data across multiple accounts and cloud services (like EC2, S3, Lambda) to mimic realistic daily costs.

Optionally loads real billing data from CSV exports from cloud providers for live analysis.

Feature Engineering:

Calculates rolling sums of costs over 7-day and 30-day windows to identify trends.

Computes daily and weekly percentage changes in costs to detect sudden increases.

Adds time-based features such as day-of-week and day-of-year to capture seasonal patterns.

Forecasting:

Forecasts future costs per account and per service using historical trends.

Accounts for trend and seasonal patterns, providing a 7- to 14-day prediction horizon.

Anomaly Detection:

Uses statistical or machine learning models to detect unusual spending behavior.

Flags days with sudden spikes or deviations from typical trends.

Alerting:

Generates human-readable alerts in two types:

Forecast Spike Alerts when predicted future costs exceed recent trends by a configurable factor.

Anomaly Alerts when recent spending behavior deviates significantly from normal patterns.

Alerts include which account or service triggered the warning and provide relevant cost context.

Logging:

All generated alerts are logged to a CSV file for record-keeping and review.

Provides summaries of total cloud spending per service and overall changes in spending.

Key Features

Multi-account and multi-service support.

Rolling sums and percentage changes for trend detection.

Forecasting future costs with trend and seasonal adjustments.

Statistical anomaly detection and machine learning-based detection.

Configurable thresholds for alerts.

Logging of alerts for audit and monitoring purposes.

Works with both simulated and real cloud billing data.

Benefits

Proactive management of cloud spending to avoid unexpected bills.

Insight into which accounts or services are driving costs.

Early detection of cost spikes to enable corrective actions.

Data-driven decision-making for optimizing cloud resources.

Easy integration into existing FinOps workflows.

Typical Usage Scenario

A user runs the program to analyze daily cloud spending. If simulated data is used, it generates patterns similar to real cloud billing for testing. With real cloud billing data, the system processes actual account costs. Alerts are generated when anomalies are detected or when forecasts indicate a future spike in costs. A summary report provides a quick overview of total spending per service, overall trends, and flagged anomalies.

Example summary:

Overall spend: $3120.25 (change -0.1%)

EC2: $2768.87 (change -0.4%)

Lambda: $68.41 (change 0.2%)

S3: $282.97 (change 2.5%)

No major spikes detected

Conclusion

FinOps AI combines forecasting and anomaly detection to provide organizations with actionable insights into cloud spending. By monitoring accounts and services, predicting future costs, and highlighting unusual behavior, it empowers teams to manage budgets proactively, optimize cloud usage, and prevent cost overruns.

This project serves as both a tool for real-world cloud cost monitoring and a learning resource for financial operations (FinOps) in cloud computing.
