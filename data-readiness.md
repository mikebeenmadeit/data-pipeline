# Data Readiness Report — Customer Churn

**Dataset:** Telco Customer Churn (CSV in S3)  
**Ingest:** S3 → Glue Crawler → Glue Data Catalog  
**Query:** Athena



## 1. Schema Summary (from Glue)
Columns (sample):  
- `customerid (string)`  
- `gender (string)`  
- `seniorcitizen (bigint)`  
- `partner (string)`  
- `dependents (string)`  
- `tenure (bigint)`  
- `phoneservice (string)`  
- `multiplelines (string)`  
- `internetservice (string)`  
- `onlinesecurity (string)`  
- `onlinebackup (string)`  
- `deviceprotection (string)`  
- `techsupport (string)`  
- `streamingtv (string)`  
- `streamingmovies (string)`  
- `contract (string)`  
- `paperlessbilling (string)`  
- `paymentmethod (string)`  
- `monthlycharges (double)`  
- `totalcharges (string | often needs cast to double)`  
- `churn (string: Yes/No)`

> Note: `totalcharges` is frequently ingested as **string** and may contain blanks — cast to double for analytics/ML.


## 2. Basic Quality Checks
- **Row count** (Athena):  
  ```sql
  SELECT COUNT(*) FROM customer_churn_data_michael;

