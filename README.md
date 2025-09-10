# Week 1 – Data Pipeline Project

## Day 2
- Created S3 bucket `customer-churn-data-michael`
- Uploaded churn dataset (CSV)
- Verified upload in S3

### Screenshots
![S3 Bucket](screenshots/bucket-list.png)
![Object URI](screenshots/object-uri.png)

---

## Day 3
- Set up AWS Glue Database `churn_db`
- Created Glue Crawler for S3 bucket
- IAM Role: `AWSGlueServiceRole-glue-crawler-role`
- Ran crawler and verified table schema

### Screenshots
![Crawler Run](screenshots/crawler-run.png)
![Crawler Summary](screenshots/crawler-summary.png)
![Table Schema](screenshots/table-schema.png)
