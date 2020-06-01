# Data Warehousing with Redshift

This project models song streaming data for warehousing in Amazon Redshift. There are two datasets, each initially stored in Amazon S3 buckets in JSON format: song data and log data. 

I want to model these two datasets as a star schema to store on a Redshift cluster. I then want to create an ETL pipeline that takes the data from the S3 buckets, stages it in Redshift, and then transforms it in conformity with the schema. This will accomplish three things:

1. It will logically connect both datasets so user data is related to song data through fact and dimension tables. This will allow for the tracking of user activity.

2. It will allow for horizontal scalability of the data.

3. It will provide MPP (massive parallel processing), which parallelizes the execution of a single queries. 

## Database Schema

![erd](files/sparkify-redshift-erd.png)