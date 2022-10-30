# AWS_Studying_Note

## 5.1 Amazon Elastic Block Store (Amazon EBS)

Amazon Elastic Block Store (Amazon EBS) is a service that provides block-level storage volumes that you can use with Amazon EC2 instances. 

If you stop or terminate an Amazon EC2 instance, all the data on the attached EBS volume remains available (Unlike 'Instant Store Volume', which cannot keep the data consistantly).

<img width="451" alt="스크린샷 2022-10-29 오전 7 32 30" src="https://user-images.githubusercontent.com/107760647/198745648-19695c2b-71b2-4724-86a1-54d324a84ae2.png">

### 5.1.1 Amazon EBS Snapshot

* An EBS snapshot is an incremental **backup**. This means that the first backup taken of a volume copies all the data. For subsequent backups, only the blocks of data that have changed since the most recent snapshot are saved. 

<img width="971" alt="스크린샷 2022-10-29 오전 7 32 56" src="https://user-images.githubusercontent.com/107760647/198745691-41da6ae8-14f9-46f8-be11-1ebc051693e7.png">

## 5.3 Amazon Elastic File System (Amazon EFS)

Amazon Elastic File System (Amazon EFS) is a scalable file system used with AWS Cloud services and on-premises resources. 
As you add and remove files, Amazon EFS grows and shrinks automatically. It can scale on demand to petabytes without disrupting applications. 

Multiple instances can access the data in **EFS** at the same time.

## EBS VS EFS (differences)

### EBS:

* Volumes attached to EC2 instances
* Availability Zone level resource
* Need to be in the same Availability Zone to attache EC2 instances
* Volumes do not automatically scale

### EFS:
* Multiple instances reading and writing simultaneously
* Linus file system
* Regional resource
* Automatically scales

## 5.4 Amazon Relational Database Service (Amazon RDS)
Amazon Relational Database Service (Amazon RDS) is a service that enables you to run relational databases in the AWS Cloud.
(Relational databases (data is stored in a way that relates it to other pieces of data) use structured query language (SQL) to store and query data. This approach allows data to be stored in an easily understandable, consistent, and scalable way.)

### 5.4.1 Amazon RDS database engines 

* Amazon Aurora
* PostgreSQL
* MySQL
* MariaDB
* Oracle Database
* Microsoft SQL Server

### 5.4.2 Amazon Aurora
Amazon Aurora is an enterprise-class relational database. *It is compatible with MySQL and PostgreSQL relational databases.* 
It is up to *five* times faster than standard MySQL databases and up to three times faster than standard PostgreSQL databases.

## 5.5 Amazon DynamoDB
Amazon DynamoDB is a key-value database service. It delivers single-digit millisecond performance at any scale.

Key Features:
* Non-relational, NoSQL database (Serverless)
* Purpose built
* Millisecond response time
* Fully managed
* Highly scalable (Automatic Scaling)

## RDS VS DynamoDB

RDS:
* Automatic high availability; recovery provided
* Customer ownership of data
* Customer ownership of schema
* Customer control of network

DynamoDB:
* Key-value
* Massive throughput capabilities
* PB size potential
* Gradnular API access

## 7.3 AWS Trusted Advisor

It is a AWS service that evaluates your resources against five pillarts:
1. Cost optimization
2. Performance
3. Security
4. Fault tolerance
5. Service limits


<img width="938" alt="스크린샷 2022-09-30 오전 7 15 46" src="https://user-images.githubusercontent.com/107760647/193151815-9d7cbe01-e3aa-4a45-b822-87ce38b63a03.png">

For each category:

*The green check indicates the number of items for which it detected no problems.

*The orange triangle represents the number of recommended investigations.

*The red circle represents the number of recommended actions.


## 8.1 AWS Free Tier

AWS offers three free services:
- Always Free
- 12 months Free: free for 12 months following your initial sign-up date to AWS
- Trials: short-term free trial 

## 8.2 AWS pricing concepts

- Pay for what you use
- pay less when you reserve
- Pay less with volume-based discounts when you use more

## 8.3 Billing dashboard
- Compare your current month-to-date balance with the previous month, and get a forecast of the next month based on current usage.
- View month-to-date spend by service.
- View Free Tier usage by service.
- Access Cost Explorer and create budgets.
- Purchase and manage Savings Plans.
- Publish AWS Cost and Usage Reports.

## 8.4 Consolidated billing
- Simplifies billing process
- Share savings across accounts
- Free feature

<img width="812" alt="스크린샷 2022-10-02 오전 7 45 34" src="https://user-images.githubusercontent.com/107760647/193430968-e0546636-97b7-4336-ac97-f46f281856a8.png">

Each account may not be eligible for a discount (exceeding 10gb). However, using Consolidated Billing, you can add them into one account, and take advantage of the discount price. 

## 8.5 AWS Budgets
You can create budgets to plan your service usage, service costs, and instance reservations.

The information in AWS Budgets updates three times a day!!!!!





# Reference:
https://explore.skillbuilder.aws
