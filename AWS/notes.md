# AWS Notes on Aurora DB and SageMaker

[Billing](https://console.aws.amazon.com/billing/home)  


[Getting Started Resource Center for Project Starters](https://aws.amazon.com/getting-started/projects/)  

Serverless Stack  
https://serverless-stack.com/  

Cognito for member management
https://aws.amazon.com/cognito/




## Aurora DB  

3/4 of top 100 customers use it. 5x faster than MySQL, 3x faster than PostgreSQL..  

Amazon Aurora DB - supports both PostgreSQL and MySQL, 10th the cost. (Used by Netflix and Dow Jones)

With Aurora DB, you can call Lambda events.  
Load data from S3. You can encrypt while moving.  

Turn on enhanced monitoring (when using). Use logs for specific query performance.  

Database Activity "Streams" - coming soon, for streaming logs
When you go into ASW you get a VPC (Virtual Private Cloud) - an isolated virtual network that you define  

OLTP (Online Transactional Processing), great for gaming performance. Consists of inserting, updating, and/or deleting small amounts of data in a database. OLTP mainly deals with large numbers of transactions by a large number of users.  

Snapshot ingestion and catch up via binlog replication

Aurora Serverless - for variable load sites. Scales down at night.
Good for dev and testing to save funds.
API, ideal for serverless Lambda and IoT

Performance Insights - See top queries. Turn on when installing Aurora.


Amazon Aurora Parallel Query - runs analytical workloads quickly in the storage layer
Turn on, Aurora query optimizer automatically decides when to use Parallel Query.  
Allow you to avoid impacting performance of transactional queries.

Serverless (Amazon used for their latest implementations)
Start with "step functions" to organize, these trigger Lambda functions.  


### Porting to Aurora

How to Port to Aurora (Migrated storm PostgreSQL database to Aurora)

https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/AuroraPostgreSQL.Migrating.RDSPostgreSQL.Replica.html

Aurora PostgreSQL DB clusters default to the default PostgreSQL port, 5432.
Frank says 7 days is typical Backup Retention Period.

Add your local machine IP (see tweetdata docs)  

Promote the Aurora Read Replica to a stand-alone DB cluster  


Amazon EMR (Elastic MapReduce) - My cluster "small cluster" existed for 1 day, 21 hours for Data Visualization HW3 before termination. Elapsed time was only 2 seconds for "setup hadoop debugging."

How to migrate in SQL Server - write Frank if hit snag
https://github.com/katgibbs/atlsummit/blob/master/ATL-Summit-2019-DMS-Workshop-Guide.pdf
https://github.com/aws-samples/aws-database-migration-samples

This might relate, migrating SQL Server to Aurora DB
https://docs.aws.amazon.com/dms/latest/sbs/CHAP_SQLServer2Aurora.html

Also, send storm data link (model.earth). Frank
fdarwesh@amazon.com


## SageMaker

For machine learning...
https://aws.amazon.com/sagemaker/

ML team uses Apache Airflow (recommends)
SageMaker notebook can reside on GitHub (Link GitHub)
SageMaker RL - Reinforcement Learning (RL) - real-world data simulator  

Sumerian is one of supported simulators - [Alternative VR Engines - Maya and Unity](https://www.vrfocus.com/2020/11/best-vr-engines-for-enterprise-applications/)    
DeepRacer League  
Use CloudWatch with Jupyter notebook to work offline  


ML Frameworks - Most use TensorFlow.  (Works with SageMaker)  
MX Net for speech models  
Add intelligence through an API call - AI Services  
Amazon Textract | Extract Text & Data  


## Courses / Certification

Cloud Guru - AWS Online Training and Certifications
independent, unlimited repeats.  
https://acloudguru.com/aws-cloud-training

[Terminology](terminology.html)  