# AWS Terminology

Amazon Elastic Compute Cloud (EC2) is a part of Amazon.com's cloud-computing platform, Amazon Web Services (AWS), that allows users to rent virtual computers on which to run their own computer applications.  Supports Docker. With EC2, ECS is managed for you.
-- Not needed with an Elastic Container Service (ECS)

Amazon Elastic Block Store (EBS) - provides persistent block level storage volumes for use with Amazon EC2 instances.
<!--
We are using Elastic Block Store for two volumes (drive letters), one for the websites and another for the databases.
-->

Elastic Container Service (ECS)

Relational Database Service (RDS) - Used by Strapi

Identity and Access Management (IAM)

List of users:
https://console.aws.amazon.com/iam/home#/roles


We created an Image of our Windows instance.

Amazon Machine Images (AMI) includes:
- Related Amazon Elastic Block Store (EBS) snapshots - for the related drives
- Launch permissions for which AWS accounts can use the AMI to launch instances
- A block device mapping indicating the volumes to attach to the instance


AWS Comprehend - Natural language processing (NLP)  

Amazon EMR (Elastic MapReduce) = Spark/Hadoop  


Secrets can be stored using AWS SSM parameter store in AWS Systems Manager Parameter Store
(Simple System Manager)


[Serverless.com CLI Commands](https://www.serverless.com/framework/docs/providers/aws/cli-reference/deploy/)

	sls deploy


Use `serverless deploy function -f myFunction` to quickly upload your updated code changes to AWS Lambda or just change function configuration.



Elastic Container Service (ECS)
Elastic Container Registry (ECR) - A fully managed container registry that makes it easy to store, manage, share, and deploy your container ECR images and artifacts anywhere.

Amazon ECR works with:
 Amazon Elastic Kubernetes Service (EKS), 
 Amazon Elastic Container Service (ECS), 
 and AWS Lambda
 and Docker CLI
 and AWS Fargate for one-click deployments.

ECR scans images for a broad range of operating system vulnerabilities and lets us build tools to act on the results.

S3 - Includes audio and video storage

Lustre, the world's most popular high-performance file system

Amazon FSx for Luster - can be linked to Amazon S3 buckets


Beanstalk - A single process to commit code, review with the team, and deploy the final result to your customers. Includes FTP

Beanstalk feels like CloudFormation "lite" for webapps. A post "I do appreciate that Beanstalk leaves its architecture out in the open for you, but I've never found it to be much of a time saver."

---

INCLUDED IN VS CODE AWS TOOLKIT

AWS CloudFormation - use a template to create, update, and delete an entire stack as a single unit. Manage and provision stacks across multiple AWS accounts and AWS Regions.

AWS Serverless Applications Model (SAM) - you define using YAML.  SAM syntax is expanded into AWS CloudFormation syntax, enabling you to build serverless applications faster.
(Similar Google Cloud Composer is built atop the open-source Apache Airflow with workflow definitions via Python)

---
<br>


Elastic Container Service (Amazon ECS) - a container management service that supports Docker.  With EC2 ECS is managed for you.  Managed Kubernetes Service (EKS) best way to manage Kubernetes - has VPC as first-class network.

Use Glue with S3 then SageMaker.  Lambda with API endpoints.
Glue prepares and loads data for analytics.

AWS Glue generates ETL code (Extract, Transform, Load) in Scala or Python to extract data from the source, transform the data to match the target schema, and load it into the target.

You can use the AWS Glue Data Catalog as your external Hive metastore for Apache Spark, Apache Hive, and Presto workloads. Select the AWS Glue Data Catalog for table metadata when creating your cluster (under EMR I assume).

Microservices

1. Instances - 190, including Elastic GPU
2. Containers - Resource isolate regardless of environment
3. Serverlets (Lambda) - integrates with 47 services

Microservices is driving transition to "Purpose Built" databases.  Amazon DynamoDB (multi-region). (Lyft)

Amazon Managed Blockchain includes Ethereum

Amazon RedShift - most popular data warehouse
"Cloud data lakes" - Unstructured.  Raw form, the compliment to data warehouse.  Data store for large quantities of data.
Amazon S3 - most popular choice for data lakes. Set up tiers to lower class storage.
AWS Lake Formation - in preview - build, secure and manage data lake. Crawl and catalog.


