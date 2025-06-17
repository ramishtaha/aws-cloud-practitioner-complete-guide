# 📖 AWS Cloud Practitioner Glossary

> **Comprehensive definitions of key AWS and cloud computing terms**

## 📋 Table of Contents

- [🌩️ Cloud Computing Fundamentals](#️-cloud-computing-fundamentals)
- [🏗️ AWS Infrastructure](#️-aws-infrastructure)
- [💻 Compute Terms](#-compute-terms)
- [💾 Storage Terms](#-storage-terms)
- [🌐 Networking Terms](#-networking-terms)
- [🗄️ Database Terms](#️-database-terms)
- [🔒 Security Terms](#-security-terms)
- [📊 Monitoring & Management](#-monitoring--management)
- [💰 Billing & Cost Terms](#-billing--cost-terms)
- [🔗 Integration & Messaging](#-integration--messaging)
- [📱 Application & Development](#-application--development)

---

## 🌩️ Cloud Computing Fundamentals

### **Auto Scaling**
The automatic adjustment of computing resources based on demand. AWS Auto Scaling monitors applications and automatically adjusts capacity to maintain steady, predictable performance at the lowest possible cost.

### **Broad Network Access**
One of the five essential characteristics of cloud computing. Cloud capabilities are available over the network and accessed through standard mechanisms that promote use by heterogeneous client platforms.

### **Capital Expenditure (CapEx)**
Money spent on acquiring or maintaining fixed assets, such as buildings and equipment. Traditional IT infrastructure requires significant upfront CapEx for servers, data centers, and networking equipment.

### **Cloud Computing**
The on-demand delivery of IT resources and applications through the internet with pay-as-you-go pricing. It eliminates the need to invest in and maintain physical infrastructure.

### **Elasticity**
The ability to acquire resources as you need them and release resources when you no longer need them. In the cloud, you want to do this automatically.

### **High Availability**
A system design approach and associated service implementation that ensures a prearranged level of operational uptime. AWS provides high availability through multiple data centers and fault tolerance.

### **Hybrid Cloud**
A cloud deployment model that combines on-premises infrastructure with cloud services, allowing data and applications to be shared between them for greater flexibility and optimization.

### **Infrastructure as a Service (IaaS)**
A cloud computing model where a provider offers computer infrastructure (servers, storage, networks) as a service. AWS EC2 is an example of IaaS.

### **Measured Service**
Cloud systems automatically control and optimize resource use by leveraging a metering capability. Resource usage can be monitored, controlled, and reported.

### **On-Demand Self-Service**
The ability for users to provision computing capabilities automatically without requiring human interaction with service providers.

### **Operational Expenditure (OpEx)**
An ongoing expense for running a business. Cloud computing typically converts IT costs from CapEx to OpEx through pay-as-you-go pricing.

### **Pay-as-you-go**
A pricing model where you only pay for the resources you actually use, with no upfront costs or long-term commitments unless you choose them.

### **Platform as a Service (PaaS)**
A cloud computing model that provides a platform allowing customers to develop, run, and manage applications without dealing with the infrastructure. AWS Elastic Beanstalk is an example.

### **Private Cloud**
Cloud infrastructure operated solely for a single organization, whether managed internally or by a third party and hosted internally or externally.

### **Public Cloud**
Cloud services offered over the public internet and available to anyone who wants to purchase them. AWS is a public cloud provider.

### **Resource Pooling**
The cloud provider's computing resources are pooled to serve multiple consumers using a multi-tenant model, with physical and virtual resources dynamically assigned and reassigned according to demand.

### **Scalability**
The ability of a system to handle increased load by adding resources to the system. Can be vertical (scaling up) or horizontal (scaling out).

### **Software as a Service (SaaS)**
A cloud computing model where applications are hosted by a service provider and made available to customers over the internet. Examples include Office 365 and Salesforce.

---

## 🏗️ AWS Infrastructure

### **Availability Zone (AZ)**
One or more discrete data centers with redundant power, networking, and connectivity in an AWS Region. Each AZ is isolated from failures in other AZs.

### **AWS Local Zones**
A type of AWS infrastructure deployment that places compute, storage, database, and other select AWS services closer to large population and industry centers.

### **AWS Outposts**
A fully managed service that extends AWS infrastructure, services, APIs, and tools to customer premises for a truly consistent hybrid experience.

### **AWS Region**
A physical location around the world where AWS clusters data centers. Each Region consists of multiple, isolated, and physically separate AZs.

### **AWS Wavelength**
Infrastructure deployments that embed AWS compute and storage services within communications service providers' (CSP) 5G networks.

### **Edge Location**
Data centers owned by AWS or a trusted partner that are part of the CloudFront content delivery network (CDN). Used to cache content closer to users.

### **Global Infrastructure**
AWS's worldwide network of Regions, Availability Zones, and edge locations that provides high availability, fault tolerance, and scalability.

---

## 💻 Compute Terms

### **Amazon EC2 (Elastic Compute Cloud)**
A web service that provides secure, resizable compute capacity in the cloud. Virtual servers that can be quickly scaled up or down.

### **Amazon ECS (Elastic Container Service)**
A highly scalable container orchestration service that supports Docker containers and allows you to run and scale containerized applications on AWS.

### **Amazon EKS (Elastic Kubernetes Service)**
A managed Kubernetes service that makes it easy to run Kubernetes on AWS without needing to install and operate your own Kubernetes control plane.

### **Auto Scaling Group**
A collection of EC2 instances that are treated as a logical grouping for the purposes of automatic scaling and management.

### **AWS Batch**
A service that enables you to run batch computing workloads on AWS. It automatically provisions the optimal quantity and type of compute resources.

### **AWS Elastic Beanstalk**
A service for deploying and scaling web applications and services. You upload your code, and Elastic Beanstalk handles the deployment.

### **AWS Fargate**
A serverless compute engine for containers that works with both Amazon ECS and Amazon EKS. It eliminates the need to provision and manage servers.

### **AWS Lambda**
A serverless compute service that runs your code in response to events and automatically manages the underlying compute resources.

### **Dedicated Host**
A physical EC2 server dedicated for your use. Can help reduce costs by allowing you to use your existing server-bound software licenses.

### **Dedicated Instance**
EC2 instances that run in a VPC on hardware that's dedicated to a single customer. They may share hardware with other instances from the same AWS account.

### **EC2 Instance Types**
- **General Purpose**: Balanced compute, memory, and networking (t3, m5, a1)
- **Compute Optimized**: High-performance processors (c5, c5n)
- **Memory Optimized**: Fast performance for memory-intensive workloads (r5, x1e)
- **Storage Optimized**: High sequential read/write access to large datasets (i3, d2)

### **Elastic Load Balancer (ELB)**
Distributes incoming application traffic across multiple targets, such as EC2 instances, containers, and IP addresses.

### **Spot Instance**
EC2 instances that use spare capacity and can offer up to 90% cost savings compared to On-Demand prices. Can be interrupted by AWS with two-minute notice.

---

## 💾 Storage Terms

### **Amazon EBS (Elastic Block Store)**
Provides block-level storage volumes for use with EC2 instances. EBS volumes persist independently from the life of an instance.

### **Amazon EFS (Elastic File System)**
A managed NFS file system that can be mounted on multiple EC2 instances simultaneously. Provides shared storage for applications.

### **Amazon S3 (Simple Storage Service)**
Object storage service that offers industry-leading scalability, data availability, security, and performance for storing and retrieving any amount of data.

### **Block Storage**
Storage that breaks files into evenly-sized blocks of data, each with its own address but without additional metadata. EBS provides block storage.

### **Durability**
The likelihood that data will remain intact and accessible. Amazon S3 provides 99.999999999% (11 9's) durability.

### **File Storage**
A method of storing data in a hierarchical structure of files and folders. Amazon EFS provides file storage.

### **Instance Store**
Provides temporary block-level storage for instances. Data persists during the lifetime of the instance but is lost when the instance stops or terminates.

### **Lifecycle Policy**
Rules that define actions that S3 applies to objects during their lifetime, such as transitioning objects to different storage classes or deleting them.

### **Object Storage**
A storage architecture that manages data as objects, as opposed to file systems or block storage. Each object includes data, metadata, and a unique identifier.

### **S3 Storage Classes**
- **Standard**: Frequently accessed data
- **Standard-IA**: Infrequently accessed data
- **One Zone-IA**: Infrequently accessed data in a single AZ
- **Glacier**: Long-term archive with retrieval times from minutes to hours
- **Glacier Deep Archive**: Lowest-cost storage for long-term retention
- **Intelligent Tiering**: Automatically moves data to most cost-effective tier

### **Versioning**
The practice of keeping multiple variants of an object in the same S3 bucket. Used to preserve, retrieve, and restore every version of every object.

---

## 🌐 Networking Terms

### **Amazon CloudFront**
A content delivery network (CDN) service that securely delivers data, videos, applications, and APIs to customers globally with low latency.

### **Amazon Route 53**
A scalable DNS web service that translates domain names to IP addresses and routes users to internet applications.

### **Amazon VPC (Virtual Private Cloud)**
A logically isolated section of the AWS cloud where you can launch AWS resources in a virtual network that you define.

### **Content Delivery Network (CDN)**
A network of distributed servers that deliver web content and services to users based on their geographic location to minimize latency.

### **AWS Direct Connect**
A dedicated network connection between your premises and AWS that can reduce network costs and increase bandwidth throughput.

### **Internet Gateway**
A horizontally scaled, redundant, and highly available VPC component that allows communication between instances in your VPC and the internet.

### **NAT Gateway**
A managed service that enables instances in a private subnet to connect to the internet or other AWS services while preventing the internet from initiating connections with those instances.

### **Network Access Control List (NACL)**
An optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets.

### **Peering Connection**
A networking connection between two VPCs that enables you to route traffic between them using private IPv4 addresses or IPv6 addresses.

### **Private Subnet**
A subnet where instances cannot communicate directly with the internet. Typically used for backend servers and databases.

### **Public Subnet**
A subnet where instances can communicate directly with the internet through an internet gateway.

### **Security Group**
A virtual firewall that controls inbound and outbound traffic for EC2 instances. Acts at the instance level and is stateful.

### **Subnet**
A range of IP addresses in your VPC. You can launch AWS resources into a subnet that you select.

---

## 🗄️ Database Terms

### **Amazon Aurora**
A MySQL and PostgreSQL-compatible relational database built for the cloud that combines performance and availability of high-end commercial databases with cost-effectiveness of open source databases.

### **Amazon DynamoDB**
A fully managed NoSQL database service that provides fast and predictable performance with seamless scalability.

### **Amazon ElastiCache**
A web service that makes it easy to deploy, operate, and scale an in-memory cache in the cloud to improve application performance.

### **Amazon RDS (Relational Database Service)**
A managed service that makes it easy to set up, operate, and scale a relational database in the cloud.

### **Amazon Redshift**
A fully managed data warehouse service that makes it simple and cost-effective to analyze data using standard SQL and business intelligence tools.

### **Database Migration Service (DMS)**
A service that helps you migrate databases to AWS quickly and securely while keeping the source database fully operational during migration.

### **Multi-AZ Deployment**
A deployment option for RDS that automatically provisions and maintains a synchronous standby replica in a different Availability Zone.

### **NoSQL Database**
A database that provides a mechanism for storage and retrieval of data modeled in means other than tabular relations. DynamoDB is AWS's NoSQL offering.

### **Read Replica**
A read-only copy of your database that can be created in the same AZ, different AZ, or different Region to improve read performance.

### **Relational Database**
A database that organizes data into tables with rows and columns, where relationships between different tables can be established. Uses SQL for queries.

---

## 🔒 Security Terms

### **AWS Certificate Manager (ACM)**
A service that lets you easily provision, manage, and deploy SSL/TLS certificates for use with AWS services and internal connected resources.

### **AWS CloudTrail**
A service that enables governance, compliance, operational auditing, and risk auditing of your AWS account by logging API calls.

### **AWS Config**
A service that enables you to assess, audit, and evaluate the configurations of your AWS resources for compliance and security analysis.

### **AWS GuardDuty**
A threat detection service that uses machine learning, anomaly detection, and integrated threat intelligence to identify threats.

### **AWS IAM (Identity and Access Management)**
A service that enables you to manage access to AWS services and resources securely through users, groups, roles, and policies.

### **AWS Inspector**
An automated security assessment service that helps improve the security and compliance of applications deployed on AWS.

### **AWS Organizations**
A service that enables you to centrally manage and govern your environment as you grow and scale your AWS resources.

### **AWS Shield**
A managed DDoS protection service that safeguards applications running on AWS against network and transport layer DDoS attacks.

### **AWS WAF (Web Application Firewall)**
A web application firewall that helps protect web applications from common web exploits that could affect application availability or compromise security.

### **Business Associate Agreement (BAA)**
A contract between a HIPAA-covered entity and a business associate that establishes permitted uses and disclosures of protected health information.

### **Compliance**
Adherence to laws, regulations, guidelines, and specifications relevant to business operations. AWS provides compliance certifications and attestations.

### **Defense in Depth**
A security strategy that employs multiple layers of security controls throughout an information system to reduce risk.

### **Encryption at Rest**
The encryption of data when it is stored on a storage device, protecting it from unauthorized access if the storage medium is compromised.

### **Encryption in Transit**
The encryption of data while it is being transmitted over a network, protecting it from interception during transmission.

### **IAM Policy**
A document that defines permissions and specifies what actions are allowed or denied for specific AWS resources.

### **IAM Role**
An AWS identity with permission policies that determine what the identity can and cannot do in AWS. Roles are assumed by trusted entities.

### **Least Privilege**
A security principle that gives users the minimum levels of access needed to perform their job functions.

### **Multi-Factor Authentication (MFA)**
An additional layer of security that requires users to provide two or more verification factors to gain access to a resource.

### **Principle of Least Privilege**
A security concept where users are granted the minimum permissions necessary to complete their tasks, reducing security risks.

### **Root User**
The email address used to create an AWS account. Has complete access to all AWS services and resources in the account.

### **Shared Responsibility Model**
AWS's security model that defines the division of security responsibilities between AWS and the customer.

---

## 📊 Monitoring & Management

### **Amazon CloudWatch**
A monitoring and management service that provides data and actionable insights for AWS resources and applications.

### **AWS Systems Manager**
A collection of capabilities that helps you automate management tasks such as collecting system inventory, applying OS patches, creating system images, and configuring Windows and Linux operating systems.

### **AWS Trusted Advisor**
An online resource that provides real-time guidance to help you provision your resources following AWS best practices for cost optimization, security, fault tolerance, and performance.

### **AWS X-Ray**
A service that collects data about requests that your application serves and provides tools you can use to view, filter, and gain insights into that data.

### **Alarm**
A feature of CloudWatch that watches a single metric and sends notifications when the metric breaches a threshold you specify.

### **Dashboard**
A customizable home page in the CloudWatch console that you can use to monitor your resources in a single view.

### **Log Group**
A group of log streams that share the same retention, monitoring, and access control settings in CloudWatch Logs.

### **Metric**
A time-ordered set of data points published to CloudWatch. Represents a variable to monitor over time.

---

## 💰 Billing & Cost Terms

### **AWS Budgets**
A service that allows you to set custom cost and usage budgets that alert you when you exceed or are forecasted to exceed your thresholds.

### **AWS Cost and Usage Report (CUR)**
A service that provides comprehensive cost and usage data for AWS services, enabling detailed analysis of AWS costs.

### **AWS Cost Explorer**
A tool that enables you to view and analyze your costs and usage over time using interactive charts and tables.

### **AWS Pricing Calculator**
A web-based planning tool that you can use to create estimates for your AWS use cases.

### **Consolidated Billing**
A billing feature in AWS Organizations that enables you to receive a single bill for multiple AWS accounts.

### **Cost Allocation Tags**
Labels that you assign to AWS resources to organize and track your costs. Tags appear in cost reports to help you categorize expenses.

### **Free Tier**
A program that offers free usage of certain AWS services for 12 months from account creation, plus some services that are always free.

### **On-Demand Pricing**
A pricing model where you pay for compute capacity by the hour or second with no long-term commitments or upfront payments.

### **Reserved Instance (RI)**
A pricing model that provides significant discounts (up to 75%) compared to On-Demand pricing in exchange for a 1 or 3-year commitment.

### **Savings Plans**
A flexible pricing model that provides significant savings on AWS usage in exchange for a commitment to a consistent amount of usage for a 1 or 3-year term.

### **Spot Instance**
A pricing model that allows you to request spare Amazon EC2 computing capacity for up to 90% off the On-Demand price.

### **Total Cost of Ownership (TCO)**
A financial estimate that helps you understand both direct and indirect costs of a product or system over its entire lifecycle.

---

## 🔗 Integration & Messaging

### **Amazon API Gateway**
A fully managed service that makes it easy for developers to create, publish, maintain, monitor, and secure APIs at any scale.

### **Amazon Kinesis**
A platform for streaming data on AWS, offering powerful services to make it easy to load and analyze streaming data.

### **Amazon SNS (Simple Notification Service)**
A publish-subscribe messaging service that enables you to decouple microservices, distributed systems, and serverless applications.

### **Amazon SQS (Simple Queue Service)**
A fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications.

### **AWS Step Functions**
A serverless workflow service that lets you coordinate multiple AWS services into serverless workflows using visual workflows.

### **Dead Letter Queue**
A queue that other queues can target for messages that can't be processed successfully, helping with error handling and debugging.

### **Event-Driven Architecture**
An architecture pattern where components communicate through events, enabling loose coupling and scalability.

### **FIFO Queue**
First-In-First-Out queues that preserve the exact order in which messages are sent and received, and ensure exactly-once processing.

### **Message Queue**
A communication method used in software systems to enable asynchronous communication between different components or services.

### **Publish-Subscribe (Pub/Sub)**
A messaging pattern where senders (publishers) send messages to multiple receivers (subscribers) without knowing who the subscribers are.

---

## 📱 Application & Development

### **Amazon Cognito**
A service that provides authentication, authorization, and user management for web and mobile applications.

### **Amazon SES (Simple Email Service)**
A cost-effective email sending service that enables you to send transactional emails, marketing messages, or any other type of content.

### **AWS CodeCommit**
A fully managed source control service that hosts secure Git-based repositories.

### **AWS CodeDeploy**
A deployment service that automates application deployments to Amazon EC2 instances, on-premises instances, or serverless Lambda functions.

### **AWS CodePipeline**
A continuous integration and continuous delivery service for fast and reliable application and infrastructure updates.

### **Continuous Integration (CI)**
A development practice where developers integrate code into a shared repository frequently, with each integration verified by automated build and tests.

### **Continuous Deployment (CD)**
A software engineering approach where code changes are automatically deployed to production after passing through automated testing phases.

### **DevOps**
A set of practices that combines software development and IT operations to shorten the development lifecycle and provide continuous delivery.

### **Infrastructure as Code (IaC)**
The practice of managing and provisioning computing infrastructure through machine-readable definition files, rather than physical hardware configuration.

### **Microservices**
An architectural approach where applications are built as a collection of loosely coupled services that can be developed, deployed, and scaled independently.

### **Serverless**
A cloud computing model where the cloud provider manages the infrastructure, and developers can focus on writing code without managing servers.

---

## 🔍 Additional Terms

### **Bandwidth**
The maximum rate of data transfer across a given path, typically measured in bits per second (bps).

### **Cache**
A hardware or software component that stores data temporarily to serve future requests faster.

### **Container**
A lightweight, standalone, executable package that includes everything needed to run an application: code, runtime, system tools, libraries, and settings.

### **Data Lake**
A centralized repository that allows you to store all your structured and unstructured data at any scale.

### **Docker**
A platform that uses containers to package applications and their dependencies for consistent deployment across different environments.

### **Kubernetes**
An open-source container orchestration platform that automates deployment, scaling, and management of containerized applications.

### **Latency**
The time delay between a request and response, typically measured in milliseconds (ms).

### **Load Balancer**
A device or service that distributes network or application traffic across multiple servers to ensure high availability and reliability.

### **Throughput**
The amount of data processed or transmitted in a given amount of time, typically measured in transactions per second or requests per second.

### **Virtual Machine (VM)**
A software-based emulation of a computer system that provides the functionality of a physical computer.

---

## 📚 Study Tips for Glossary

### 🎯 How to Use This Glossary
1. **Regular Review**: Read 10-15 terms daily during your study period
2. **Context Learning**: Don't just memorize - understand how terms relate to each other
3. **Practical Application**: Try to use these terms when discussing AWS concepts
4. **Cross-Reference**: Link terms back to the main study materials

### 🔤 Acronym Quick Reference
- **AWS**: Amazon Web Services
- **EC2**: Elastic Compute Cloud
- **S3**: Simple Storage Service
- **IAM**: Identity and Access Management
- **VPC**: Virtual Private Cloud
- **RDS**: Relational Database Service
- **CDN**: Content Delivery Network
- **DNS**: Domain Name System
- **API**: Application Programming Interface
- **SDK**: Software Development Kit
- **CLI**: Command Line Interface
- **AZ**: Availability Zone
- **SLA**: Service Level Agreement
- **TCO**: Total Cost of Ownership
- **ROI**: Return on Investment

### 🎯 Priority Learning Levels

#### **🔥 Must Know (Exam Critical)**
- Cloud Computing, IaaS/PaaS/SaaS, Region, AZ, EC2, S3, IAM, VPC

#### **⭐ Should Know (Frequently Tested)**
- Lambda, RDS, DynamoDB, CloudFront, Auto Scaling, ELB, Security Groups

#### **📚 Good to Know (Context Understanding)**
- ECS, EKS, Kinesis, SNS, SQS, CloudTrail, Config, GuardDuty

---

**💡 Pro Tip**: Create your own definitions in your words after reading the official ones. This helps with retention and understanding!

---

## 🔗 Quick Navigation
- 🏠 [Main Study Guide](../README.md)
- 🚀 [Service Cheat Sheet](service-cheatsheet.md)
- 🎯 [Exam Tips](exam-tips.md)
- 📝 [Practice Exams](../practice-exams/)

---

*Use this glossary as your quick reference guide throughout your AWS certification journey! 📖*
