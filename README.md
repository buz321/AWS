# AWS_Studying_Note (Amazon Practitioner) - Achieved 23/11/2022
![aws-certified-cloud-practitioner](https://user-images.githubusercontent.com/107760647/203555681-6d13f3a5-2483-4b67-b247-ab0c3297ab8b.png)



# 2.3 Scaling Amazon EC2

## 2.3.1 Scalability 
Scalability involves beginning with only the resources you need and designing your architecture to automatically respond to changing demand by scaling out or in.

## 2.3.2 Amazon EC2 Auto Scaling
Amazon EC2 Auto Scaling enables you to automatically add or remove Amazon EC2 instances in response to changing application demand.

# 2.4 Directing traffic with Elastic Load Balancing

## 2.4.1 Elastic Load Balancing
Elastic Load Balancing is the AWS service that automatically distributes incoming application traffic across multiple resources, such as Amazon EC2 instances. 

## 3.2 Edge locations

An edge location is a site that Amazon CloudFront uses to store cached copies of your content closer to your customers for faster delivery.

(accerlations the communication and content delivery)

* Edge location is separate from "Regions"

* Do not confuse with Regions! 

### 3.2.1 Amazon CloundFront
A service that helps deliver data, video, application, APIs to customers around the world with "Low Latency" and "High-Transfer-Speed"

* Low Latency

* High-Transfer-Speed

### 3.2.2 Amazon Route 53
domain name service 
helping direct cusomters to certain web location

* Low Latency !

* High-Transfer-Speed

### 3.2.3 AWS Outposts
Install a fully operational mini Region, right inside your own data center. That's owned and operated by AWS, using 100% of AWS functionality, but isolated within your own building. 


## Regions are geographically isolated areas !!!!!!!

## 3.3 Ways to interact with AWS services
- How to provision AWS resources - 

### 3.3.1 AWS Management Console (point and click style)
The AWS Management Console is a web-based interface for accessing and managing AWS services. You can quickly access recently used services and search for other services by name, keyword, or acronym. The console includes wizards and automated workflows that can simplify the process of completing tasks.

* Test environments
* View AWS bills
* View monitoring 
* Work with non-technical resources

### 3.3.2 AWS Command Line Interface (CLI)

- Make API calls using the terminal on your machine 


To save time when making API requests, you can use the AWS Command Line Interface (AWS CLI). AWS CLI enables you to control multiple AWS services directly from the command line within one tool. AWS CLI is available for users on Windows, macOS, and Linux. 

### 3.3.3 AWS Software Development Kits (SDKs)
Another option for accessing and managing AWS services is the software development kits (SDKs). SDKs make it easier for you to use AWS services through an API designed for your programming language or platform. SDKs enable you to use AWS services with your existing applications or create entirely new applications that will run on AWS.

### 3.3.4 AWS Elastic Beanstalk
With AWS Elastic Beanstalk, you provide code and configuration settings, and Elastic Beanstalk deploys the resources necessary to perform the following tasks:

* Adjust capacity 
* Laod balancing
* Automatic scaling
* Application health monitoring

(do it automatically and efficiently !!)


### 3.3.5 AWS CloudFormation
With AWS CloudFormation, you can treat your infrastructure as code. This means that you can build an environment by writing lines of code instead of using the AWS Management Console to individually provision resources.

(do it automatically !!!!)

# 4.1 Connectivity to AWS
## 4.1.1 Amazon Virtual Private Cloud (Amazon VPC)

## 4.1.2 Internet Gateway
- To allow public traffic from the internet to access your VPC, you attach an internet gateway to the VPC.
- 
- An internet gateway is a connection between a VPC and the internet. You can think of an internet gateway as being similar to a doorway that customers use to enter the coffee shop. Without an internet gateway, no one can access the resources within your VPC.
<img width="869" alt="스크린샷 2022-11-09 오전 7 18 35" src="https://user-images.githubusercontent.com/107760647/200687980-5b674af7-8a94-4085-964c-ffe14d5effb7.png">

## 4.1.2 Virtual Private Gateway
- To access private resources in a VPC, you can use a virtual private gateway. 
- The virtual private gateway is the component that allows protected internet traffic to enter into the VPC.
<img width="863" alt="스크린샷 2022-11-09 오전 7 21 07" src="https://user-images.githubusercontent.com/107760647/200688409-3a0ee468-b273-410c-bfc5-ad7ac55184ac.png">

## 4.1.3 AWS Direct Connect
- AWS Direct Connect is a service that enables you to establish a dedicated private connection between your data center and a VPC.  

* The private connection that AWS Direct Connect provides helps you to reduce network costs and increase the amount of bandwidth that can travel through your network.

<img width="865" alt="스크린샷 2022-11-09 오전 7 22 12" src="https://user-images.githubusercontent.com/107760647/200688591-8c67e9bf-de2f-402c-a5b6-d38137ba8980.png">

# 4.2 Subnets and network access control lists

## 4.2.1 Subnets
A subnet is a section of a VPC in which you can group resources based on security or operational needs. Subnets can be public or private. 

* Public subnets: contain resources that need to be accessible by the public, such as an online store’s website.

* Private subnets:  contain resources that should be accessible only through your private network, such as a database that contains customers’ personal information and order histories. 
<img width="454" alt="스크린샷 2022-11-10 오전 6 46 09" src="https://user-images.githubusercontent.com/107760647/200948554-4654d0f0-3767-4fdf-ac0c-882a59a009b1.png">

## 4.2.2 Network access control lists (ACLs)
A network access control list (ACL) is a virtual firewall that controls inbound and outbound traffic at the subnet level.
<img width="344" alt="스크린샷 2022-11-10 오전 6 47 02" src="https://user-images.githubusercontent.com/107760647/200948704-d58fdf7e-f5d9-4efd-9fbd-dfdb17b19bf3.png">

## 4.2.3 Security groups
A security group is a virtual firewall that controls inbound and outbound traffic for an Amazon EC2 instance.

<img width="852" alt="스크린샷 2022-11-10 오전 6 47 54" src="https://user-images.githubusercontent.com/107760647/200948867-8356027d-cda3-4257-8894-6ec2e241c4d7.png">

-------------------------------------------------------------------------------------------------------------------------------------------------
- Network Hardening

- Request = packet
Security Group is Stateful (remember when the data enters, so doesn't check when it leaves) 

Stateless is Stateless (remembers nothing!)
-------------------------------------------------------------------------------------------------------------------------------------------------
# 4.3 Global Networking

## 4.3.1 Domain Name System (DNS)
web address - DNS translate it
DNS resolution involves a customer DNS resolver communicating with a company DNS server.

## 4.3.2 Amazon Route 53
- Amazon Route 53 is a DNS web service. It gives developers and businesses a reliable way to route end users to internet applications hosted in AWS. 

Amazon Route 53 routing policies:
* Latency-based routing
* Geolocation DNS
* Geoproximity routing
* Weighted round robin

## 4.3.3 Amazon Cloudfront
- Deliver contents (low latency)

## 5.1 Amazon Elastic Block Store (Amazon EBS)

Amazon Elastic Block Store (Amazon EBS) is a service that provides block-level storage volumes that you can use with Amazon EC2 instances. 

If you stop or terminate an Amazon EC2 instance, all the data on the attached EBS volume remains available (Unlike 'Instant Store Volume', which cannot keep the data consistantly).

<img width="451" alt="스크린샷 2022-10-29 오전 7 32 30" src="https://user-images.githubusercontent.com/107760647/198745648-19695c2b-71b2-4724-86a1-54d324a84ae2.png">

### 5.1.1 Amazon EBS Snapshot

* An EBS snapshot is an incremental **backup**. This means that the first backup taken of a volume copies all the data. For subsequent backups, only the blocks of data that have changed since the most recent snapshot are saved. 

<img width="971" alt="스크린샷 2022-10-29 오전 7 32 56" src="https://user-images.githubusercontent.com/107760647/198745691-41da6ae8-14f9-46f8-be11-1ebc051693e7.png">

## 5.2 Amazon Simple Storage Service (Amazon S3)
Amazon Simple Storage Service (Amazon S3) is a service that provides object-level storage. !Amazon S3 stores data as objects in buckets.!

### 5.2.1 Amazon S3 storage classes

* Amazon S3 Standard

Designed for frequently accessed data

Stores data in a minimum of three Availability Zones

* Amazon S3 Standard-Infrequent Access (S3 Standard-IA)

Ideal for infrequently accessed data

Similar to Amazon S3 Standard but has a lower storage price and higher retrieval price

* Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)

Stores data in a single Availability Zone (cold-data, 중요하긴 하지만 절대 열어보질 않은 데이터 콜드 데이터)

Has a lower storage price than Amazon S3 Standard-IA

* Amazon S3 Intelligent-Tiering

Ideal for data with unknown or changing access patterns

Requires a small monthly monitoring and automation fee per object

*  Amazon S3 Glacier Instant Retrieval

Works well for #archived data# that requires immediate access

Can retrieve objects within a few milliseconds

* Amazon S3 Glacier Flexible Retrieval

Low-cost storage designed for data archiving

Able to retrieve objects within a few minutes to hours

* Amazon S3 Glacier Deep Archive

Lowest-cost object storage class ideal for archiving

Able to retrieve objects within 12 hours

* Amazon S3 Outposts

Creates S3 buckets on Amazon S3 Outposts

Makes it easier to retrieve, store, and access data on AWS Outposts


### 5.2.1 Amazon EBS VS Amazon S3

Amazon EBS:

* Sizes up to 16 TiB
* Survive termination of their EC2 instance
* Solid state by default
* HDD options

Amazon S3:

* Unlimited storage
* Individual objects up to 5 TBs
* Write once/read many
* 99.9999999% durability 

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

## 5.6 Redshift
Amazon Redshift is a data warehousing service that you can use for big data analytics. It offers the ability to collect data from many sources and helps you to understand relationships and trends across your data.

**It's a 'Data Warehouse'**

## 5.7 AWS Database Migration Service 
AWS Database Migration Service (AWS DMS) enables you to migrate relational databases, nonrelational databases, and other types of data stores.

* The source database remains fully operational during the migration.
* Downtime is minimised for applications that rely on that database.
* The source and target databases don't have to be of the same type.

### 5.7.1 Homogenous databases
On-premises, Amazon EC2, Amazon RDS >>>>> Amazon EC2, Amazon RDS

### 5.7.2 Heterogeneous databases

2 step process:
1. Using #AWS Schema Converter# to convert the source schema and code to match the target database. 
2. Then, DMS to migrate from the source to target database.

More function!
* Development and test database migrations
* Database consolidation
* Continous replication 

## 5.8 Additional database services

* Amazon DocumentDB 

Amazon DocumentDB is a document database service that supports #MongoDB# workloads. (MongoDB is a document database program.

Note: it is grate for content management, cataloges, user profiles

* Amazon Neptune (Graph database)

Amazon Neptune is a graph database service. 
You can use Amazon Neptune to build and run applications that work with highly connected datasets, such as recommendation engines, fraud detection, and knowledge graphs.

* Amazon Quantum Ledger Database (Amazon QLDB)

Amazon Quantum Ledger Database (Amazon QLDB) is a ledger database service. 

You can use Amazon QLDB to review a complete history of all the changes that have been made to your application data.

* Amazon Mnaged Blockchain

Amazon Managed Blockchain is a service that you can use to create and manage blockchain networks with open-source frameworks. 

Blockchain is a distributed ledger system that lets multiple parties run transactions and share data without a central authority.

* Amazon ElastiCache

Amazon ElastiCache is a service that adds caching layers on top of your databases to help improve the read times of common requests. 

It supports two types of data stores: Redis and Memcached.

Note: it can accerlate the options for database by adding cache layers. 

* Amazon DynamoDB Accelerator (DAX)

Amazon DynamoDB Accelerator (DAX) is an in-memory cache for DynamoDB. 

It helps improve response times from single-digit milliseconds to microseconds.

- make sure to understand each feature's functions

## 6.1 Shared responsibility model
<img width="854" alt="스크린샷 2022-11-01 오전 7 34 54" src="https://user-images.githubusercontent.com/107760647/199122808-dfc304d5-c017-402b-8998-01f20c160d5e.png">



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

* it gives you an alert!!!! (notification)

## 8.6 AWS Cost Explorer
AWS Cost Explorer is a tool that enables you to visualize, understand, and manage your AWS costs and usage over time.

* Visualisation !!!!

## 8.7 AWS Support Plans

### 8.7.1 Basic Support

* 24/7 customer service
* Doumentation
* Whitepapers
* Support forums
* AWS Trusted Advisor
* AWS Personal Health Dashboard - a tool that provides alerts and remediation guidance when AWS is experiencing events that may affect you

### 8.7.2 Developer Support
* Basic Support 
* Email to customer support (12 h)

### 8.7.3 Business Support

* Basic and Developer support
* AWS Trusted Advisor provides full set of bset practice checks
* Direct phone access to cloud support engineers
* Infrastructure event management

### 8.7.4 Enterprise Support

* Basic, Developer, and Business support
* 15- minue SLA for business critical workloads
* Tehnical Account Manager (TAM) - part of Concierge support team, monitoring environment, archtective and operational reviews. 

- Five Pillars
* Operational Excellence
* Security
* Reliability
* Performance Efficiency
* Cost Optimisation


## 9.2 Migration strategies

The application migration strategies are:

* rehosting 
* replatforming
* refactoring/re-architecting
* repurchasing
* retaining 
* retiring

## 9.3 Snow Family
The **AWS Snow Family** is a collection of physical devices that help to physically transport up to exabytes of data into and out of AWS. 
<img width="864" alt="스크린샷 2022-11-04 오전 8 01 06" src="https://user-images.githubusercontent.com/107760647/199851142-14bfb580-1ff6-4519-822d-dccce9748fca.png">


### AWS SNOWCONE
* AWS Snowcone is a small, rugged, and secure edge computing and data transfer device. 
* It features 2 CPUs, 4 GB of memory, and 8 TB of usable storage.

### AWS SNOWBALL

** Snowball Edge Storage Optimized == devices are well suited for large-scale data migrations and recurring transfer workflows, in addition to local computing with higher capacity needs. 

* Storage: 80 TB of hard disk drive (HDD) capacity for block volumes and Amazon S3 compatible object storage, and 1 TB of SATA solid state drive (SSD) for block volumes. 

* Compute: 40 vCPUs, and 80 GiB of memory to support Amazon EC2 sbe1 instances (equivalent to C5).

** Snowball Edge Compute Optimized == provides powerful computing resources for use cases such as machine learning, full motion video analysis, analytics, and local computing stacks. 

* Storage: 42-TB usable HDD capacity for Amazon S3 compatible object storage or Amazon EBS compatible block volumes and 7.68 TB of usable NVMe SSD capacity for Amazon EBS compatible block volumes. 

* Compute: 52 vCPUs, 208 GiB of memory, and an optional NVIDIA Tesla V100 GPU. Devices run Amazon EC2 sbe-c and sbe-g instances, which are equivalent to C5, M5a, G3, and P3 instances.

### AWS SNOWMOBILE

* AWS Snowmobile is an exabyte-scale data transfer service used to move large amounts of data to AWS. 

* You can transfer up to 100 petabytes of data per Snowmobile, a 45-foot long ruggedized shipping container, pulled by a semi trailer truck.

Note!: AWS Snow Family is 'Secure and Tamper-resistant'
       It's important to know which situation is appropriate to use each feature. 
# Reference:
https://explore.skillbuilder.aws
