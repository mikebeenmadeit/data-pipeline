Week 1 – AWS Data Pipeline (S3 → Glue → Athen
a)
📌 Project Overview
This project demonstrates building a serverless data pipeline on AWS as part of my cloud engineering portfolio. The goal is to ingest raw customer churn data, catalog it for querying, and prepare it for future analytics and machine learning.

Key AWS Services:
Amazon S3 – raw data storage
AWS Glue – crawler & Data Catalog for schema inference
Amazon Athena – query engine for analysis


 Accomplishments

Day 1 — Secure & Cost Control Setup
Created AWS Budgets & billing alerts
Enabled IAM best practices: no root use, MFA enabled, created admin IAM user

Deliverables: Budget alerts active, IAM admin user secured

Day 2 — S3 Bucket & Data Upload
Created S3 bucket customer-churn-data-michael
Uploaded Telco Customer Churn dataset (CSV)
Verified dataset upload in S3 console

Deliverables: Dataset stored securely in S3

Day 3 — Glue Database & Crawler
Created Glue database churn_db
Built Glue Crawler to scan S3 bucket and infer schema
Verified schema creation in Glue Data Catalog

Deliverables: customer_churn_data_michael table available for Athena queries

Day 4 — Query Data with Athena
Connected Athena to Glue Data Catalog
Created Athena results bucket athena-query-results-michael1
Ran SQL queries against churn dataset
Verified queries and results saved in S3

Deliverables: Athena queries + results

Day 5 — Data Readiness & Cleanup
Wrote Data Readiness Report (data-readiness.md) documenting schema, nulls, type issues, and imbalance in churn labels
Created clean view (churn_clean) with proper numeric casting and categorical handling for ML readiness

Deliverables:
data-readiness.md
Athena view churn_clean created and validated
## Architecture

![Architecture Diagram](architecture.png)

