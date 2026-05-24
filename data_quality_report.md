# Data Quality Report

## Missing Values
Some missing values were found in aggregated behavioral columns such as ticket_count and total_spend. Missing values were treated using fillna(0) where appropriate.

## Duplicate Records
No major duplicate customer records were found. Duplicate columns generated during merging (e.g., churn_x/churn_y) were resolved.

## Invalid Values
No negative gross_amount values were found.
No invalid future order dates were detected.

## Outliers
Outliers were observed in total_spend and total_orders, indicating a small group of highly active customers.

## Join/Key Issues
Transactional tables required aggregation before merging to avoid many-to-many duplication.

## Leakage Risks
Potential leakage risk may exist in precomputed snapshot/RFM features if they include post-churn information.
