# 🚀 AWS Services Quick Reference Cheat Sheet

> **Essential AWS services at a glance for the Cloud Practitioner exam**

## 📋 Table of Contents

- [💻 Compute Services](#-compute-services)
- [💾 Storage Services](#-storage-services)
- [🌐 Networking & Content Delivery](#-networking--content-delivery)
- [🗄️ Database Services](#️-database-services)
- [🔒 Security & Identity Services](#-security--identity-services)
- [📊 Management & Monitoring](#-management--monitoring)
- [🔗 Integration & Messaging](#-integration--messaging)
- [📱 Application Services](#-application-services)
- [💰 Billing & Cost Management](#-billing--cost-management)
- [🎯 Quick Decision Matrix](#-quick-decision-matrix)

---

## 💻 Compute Services

### Amazon EC2 (Elastic Compute Cloud)
- **What it is**: Virtual servers in the cloud
- **When to use**: When you need virtual machines with full control
- **Key features**: Multiple instance types, auto scaling, various pricing models
- **Pricing**: On-Demand, Reserved, Spot, Dedicated
- **Exam tip**: Remember different instance families (General purpose, Compute optimized, Memory optimized, Storage optimized)

### AWS Lambda
- **What it is**: Serverless compute service
- **When to use**: Event-driven applications, short-running functions
- **Key features**: No server management, automatic scaling, pay per execution
- **Limits**: 15-minute max execution time, memory up to 10GB
- **Exam tip**: Ideal for microservices and event processing

### Amazon ECS (Elastic Container Service)
- **What it is**: Container orchestration service
- **When to use**: Running Docker containers at scale
- **Key features**: Integrates with AWS services, supports Fargate for serverless containers
- **Exam tip**: ECS with Fargate = serverless containers

### Amazon EKS (Elastic Kubernetes Service)
- **What it is**: Managed Kubernetes service
- **When to use**: When you need Kubernetes orchestration
- **Key features**: Fully managed Kubernetes control plane
- **Exam tip**: Use when you already know Kubernetes

### AWS Batch
- **What it is**: Batch computing service
- **When to use**: Running batch jobs at any scale
- **Key features**: Automatic provisioning, job queues, cost optimization
- **Exam tip**: For long-running batch processing workloads

### AWS Elastic Beanstalk
- **What it is**: Platform-as-a-Service for web applications
- **When to use**: Quick deployment without infrastructure management
- **Key features**: Supports multiple programming languages, automatic scaling
- **Exam tip**: Upload code and run - AWS handles the rest

---

## 💾 Storage Services

### Amazon S3 (Simple Storage Service)
- **What it is**: Object storage service
- **When to use**: Storing any type of data - websites, backups, archives
- **Storage classes**:
  - **Standard**: Frequently accessed data
  - **Standard-IA**: Infrequently accessed data
  - **One Zone-IA**: Lower cost for infrequently accessed data
  - **Glacier**: Long-term archival
  - **Glacier Deep Archive**: Lowest cost archival
  - **Intelligent Tiering**: Automatic optimization
- **Key features**: 99.999999999% (11 9's) durability, unlimited storage
- **Exam tip**: Know when to use each storage class

### Amazon EBS (Elastic Block Store)
- **What it is**: Block storage for EC2 instances
- **When to use**: Persistent storage for EC2 instances
- **Volume types**:
  - **gp3/gp2**: General purpose SSD
  - **io2/io1**: Provisioned IOPS SSD (high performance)
  - **st1**: Throughput optimized HDD
  - **sc1**: Cold HDD (lowest cost)
- **Key features**: Persistent, can be detached and reattached
- **Exam tip**: EBS persists beyond instance lifecycle

### Amazon EFS (Elastic File System)
- **What it is**: Managed NFS file system
- **When to use**: Shared file storage across multiple EC2 instances
- **Key features**: Scales automatically, concurrent access
- **Exam tip**: Use when multiple instances need shared file access

### AWS Storage Gateway
- **What it is**: Hybrid cloud storage service
- **When to use**: Connecting on-premises to AWS storage
- **Types**: File Gateway, Volume Gateway, Tape Gateway
- **Exam tip**: Bridge between on-premises and cloud storage

---

## 🌐 Networking & Content Delivery

### Amazon VPC (Virtual Private Cloud)
- **What it is**: Isolated virtual network in AWS
- **When to use**: Creating isolated network environments
- **Components**: Subnets, Route Tables, Internet Gateways, NAT Gateways
- **Key features**: Complete control over network configuration
- **Exam tip**: Foundation for most AWS architectures

### Amazon CloudFront
- **What it is**: Content Delivery Network (CDN)
- **When to use**: Delivering content globally with low latency
- **Key features**: Edge locations worldwide, caches content close to users
- **Exam tip**: Reduces latency by serving content from edge locations

### Elastic Load Balancing (ELB)
- **What it is**: Distributes incoming traffic across multiple targets
- **Types**:
  - **Application Load Balancer (ALB)**: Layer 7, HTTP/HTTPS
  - **Network Load Balancer (NLB)**: Layer 4, TCP/UDP
  - **Classic Load Balancer**: Legacy, Layer 4 & 7
- **Exam tip**: ALB for web apps, NLB for high performance

### Amazon Route 53
- **What it is**: DNS web service
- **When to use**: Domain name resolution, health checks, routing
- **Key features**: Global DNS, health checks, multiple routing policies
- **Exam tip**: More than just DNS - includes health monitoring

### AWS Direct Connect
- **What it is**: Dedicated network connection to AWS
- **When to use**: Consistent network performance, large data transfers
- **Key features**: Predictable bandwidth, reduced network costs
- **Exam tip**: Alternative to VPN for dedicated connectivity

---

## 🗄️ Database Services

### Amazon RDS (Relational Database Service)
- **What it is**: Managed relational database service
- **Supported engines**: MySQL, PostgreSQL, MariaDB, Oracle, SQL Server, Aurora
- **When to use**: Traditional relational database needs
- **Key features**: Automated backups, patching, scaling
- **Exam tip**: AWS manages infrastructure, you manage data and queries

### Amazon Aurora
- **What it is**: Cloud-native relational database
- **When to use**: High-performance relational database needs
- **Key features**: MySQL/PostgreSQL compatible, auto-scaling storage
- **Exam tip**: AWS's high-performance database engine

### Amazon DynamoDB
- **What it is**: NoSQL database service
- **When to use**: High-scale applications, need single-digit millisecond latency
- **Key features**: Serverless, automatic scaling, global tables
- **Exam tip**: Ideal for mobile, web, gaming applications

### Amazon Redshift
- **What it is**: Data warehouse service
- **When to use**: Business intelligence and analytics
- **Key features**: Columnar storage, parallel processing, petabyte scale
- **Exam tip**: For analytics and data warehousing, not operational databases

### Amazon ElastiCache
- **What it is**: In-memory caching service
- **When to use**: Improving application performance with caching
- **Engines**: Redis, Memcached
- **Exam tip**: Use to speed up database queries and application performance

---

## 🔒 Security & Identity Services

### AWS IAM (Identity and Access Management)
- **What it is**: Authentication and authorization service
- **Components**: Users, Groups, Roles, Policies
- **Key principles**: Least privilege, use roles for applications
- **Exam tip**: Foundation of AWS security

### AWS Organizations
- **What it is**: Account management service
- **When to use**: Managing multiple AWS accounts
- **Key features**: Consolidated billing, Service Control Policies (SCPs)
- **Exam tip**: Central management for multi-account environments

### AWS CloudTrail
- **What it is**: API logging and auditing service
- **When to use**: Compliance, security analysis, troubleshooting
- **Key features**: Logs all API calls, integrates with CloudWatch
- **Exam tip**: Essential for security auditing

### AWS Config
- **What it is**: Configuration monitoring and compliance service
- **When to use**: Tracking resource configurations and compliance
- **Key features**: Configuration history, compliance rules
- **Exam tip**: Monitors "what" changed, CloudTrail monitors "who" changed it

### AWS GuardDuty
- **What it is**: Threat detection service
- **When to use**: Automated security threat detection
- **Key features**: Machine learning-based threat detection
- **Exam tip**: Uses ML to detect anomalous behavior

### AWS Inspector
- **What it is**: Security assessment service
- **When to use**: Finding vulnerabilities in EC2 instances and container images
- **Key features**: Automated security assessments
- **Exam tip**: Focuses on application security vulnerabilities

### AWS WAF (Web Application Firewall)
- **What it is**: Web application protection service
- **When to use**: Protecting web applications from exploits
- **Key features**: SQL injection protection, XSS protection
- **Exam tip**: Layer 7 protection for web applications

### AWS Shield
- **What it is**: DDoS protection service
- **Levels**: Standard (free), Advanced (paid)
- **When to use**: Protecting against DDoS attacks
- **Exam tip**: Standard comes free with CloudFront and Route 53

---

## 📊 Management & Monitoring

### Amazon CloudWatch
- **What it is**: Monitoring and logging service
- **When to use**: Monitoring AWS resources and applications
- **Key features**: Metrics, logs, alarms, dashboards
- **Exam tip**: Central monitoring hub for AWS

### AWS Systems Manager
- **What it is**: Operational management service
- **When to use**: Managing EC2 instances and on-premises servers
- **Key features**: Patch management, configuration management
- **Exam tip**: Manages both cloud and on-premises infrastructure

### AWS CloudFormation
- **What it is**: Infrastructure as Code service
- **When to use**: Deploying infrastructure using templates
- **Key features**: JSON/YAML templates, stack management
- **Exam tip**: Declarative way to provision AWS resources

### AWS X-Ray
- **What it is**: Application performance monitoring
- **When to use**: Tracing requests in distributed applications
- **Key features**: Request tracing, performance analysis
- **Exam tip**: Helps identify bottlenecks in microservices

---

## 🔗 Integration & Messaging

### Amazon SQS (Simple Queue Service)
- **What it is**: Message queuing service
- **When to use**: Decoupling application components
- **Types**: Standard (at-least-once), FIFO (exactly-once, ordered)
- **Exam tip**: Use for asynchronous communication between services

### Amazon SNS (Simple Notification Service)
- **What it is**: Publish-subscribe messaging service
- **When to use**: Sending notifications to multiple subscribers
- **Key features**: Multiple delivery methods (email, SMS, HTTP, SQS)
- **Exam tip**: Fan-out messaging pattern

### Amazon Kinesis
- **What it is**: Real-time data streaming service
- **When to use**: Processing streaming data in real-time
- **Components**: Data Streams, Data Firehose, Analytics
- **Exam tip**: For real-time data processing and analytics

### AWS Step Functions
- **What it is**: Serverless workflow orchestration
- **When to use**: Coordinating multiple AWS services in workflows
- **Key features**: Visual workflows, error handling
- **Exam tip**: Orchestrates serverless applications

---

## 📱 Application Services

### Amazon API Gateway
- **What it is**: API management service
- **When to use**: Creating, deploying, and managing APIs
- **Key features**: REST/WebSocket APIs, throttling, authorization
- **Exam tip**: Front door for serverless applications

### Amazon SES (Simple Email Service)
- **What it is**: Email sending service
- **When to use**: Sending transactional or marketing emails
- **Key features**: High deliverability, cost-effective
- **Exam tip**: For application-generated emails

### Amazon Cognito
- **What it is**: User authentication and authorization service
- **When to use**: Mobile and web application user management
- **Key features**: User pools, identity pools, social login
- **Exam tip**: For customer-facing application authentication

---

## 💰 Billing & Cost Management

### AWS Cost Explorer
- **What it is**: Cost visualization and analysis tool
- **When to use**: Understanding and analyzing AWS costs
- **Key features**: Historical data, forecasting, recommendations
- **Exam tip**: Primary tool for cost analysis

### AWS Budgets
- **What it is**: Cost and usage budgeting service
- **When to use**: Setting spending limits and alerts
- **Key features**: Custom budgets, automated alerts
- **Exam tip**: Proactive cost management

### AWS Cost and Usage Report (CUR)
- **What it is**: Detailed billing data export
- **When to use**: Detailed cost analysis with external tools
- **Key features**: Comprehensive billing data, custom analysis
- **Exam tip**: Most detailed billing data available

### AWS Trusted Advisor
- **What it is**: Best practices recommendation service
- **Categories**: Cost optimization, performance, security, fault tolerance
- **Levels**: Basic (7 checks), Full (Business/Enterprise support)
- **Exam tip**: Provides optimization recommendations

---

## 🎯 Quick Decision Matrix

### Choose the Right Compute Service
| Need | Service | Why |
|------|---------|-----|
| Virtual machines | EC2 | Full control over instances |
| Serverless functions | Lambda | Event-driven, no server management |
| Container orchestration | ECS/EKS | Scalable container management |
| Quick web app deployment | Elastic Beanstalk | PaaS, just upload code |
| Batch processing | Batch | Optimized for batch workloads |

### Choose the Right Storage Service
| Need | Service | Why |
|------|---------|-----|
| Object storage | S3 | Unlimited, highly durable |
| Block storage for EC2 | EBS | Persistent, high performance |
| Shared file storage | EFS | Multi-instance access |
| Archival storage | S3 Glacier | Lowest cost for archives |

### Choose the Right Database Service
| Need | Service | Why |
|------|---------|-----|
| Relational database | RDS | Managed SQL databases |
| High-performance relational | Aurora | Cloud-native, auto-scaling |
| NoSQL database | DynamoDB | Serverless, single-digit latency |
| Data warehouse | Redshift | Analytics and BI |
| Caching | ElastiCache | In-memory performance |

### Choose the Right Security Service
| Need | Service | Why |
|------|---------|-----|
| Identity management | IAM | Users, roles, permissions |
| API logging | CloudTrail | Audit trail of API calls |
| Configuration monitoring | Config | Track resource configurations |
| Threat detection | GuardDuty | ML-based security monitoring |
| Web app protection | WAF | Application layer firewall |
| DDoS protection | Shield | Network/transport layer protection |

---

## 📚 Exam Tips

### 🎯 Service Selection Strategy
1. **Identify the use case** - What is the business need?
2. **Consider management level** - How much management do you want?
3. **Think about scale** - Current and future requirements
4. **Factor in cost** - Optimize for the appropriate pricing model

### 🔑 Key Relationships to Remember
- **EC2 + EBS**: Virtual machines with persistent storage
- **S3 + CloudFront**: Global content delivery
- **VPC + Subnets**: Network isolation and segmentation
- **ALB + Auto Scaling**: High availability and elasticity
- **Lambda + API Gateway**: Serverless web APIs
- **RDS + Read Replicas**: Database scaling
- **CloudTrail + CloudWatch**: Security monitoring
- **IAM + Organizations**: Identity and account management

### ⚠️ Common Exam Traps
- Don't confuse **CloudWatch** (monitoring) with **CloudTrail** (API logging)
- Remember **S3** is object storage, **EBS** is block storage
- **Lambda** has time limits (15 minutes max)
- **DynamoDB** is NoSQL, **RDS** is SQL
- **Security Groups** are stateful, **NACLs** are stateless

---

## 🚀 Quick Reference Links

- 🏠 [Main Study Guide](../README.md)
- 🌩️ [Domain 1: Cloud Concepts](../01-cloud-concepts/README.md)
- 🔒 [Domain 2: Security & Compliance](../02-security-compliance/README.md)
- ⚙️ [Domain 3: Technology & Services](../03-technology-services/README.md)
- 💰 [Domain 4: Billing & Support](../04-billing-support/README.md)
- 📝 [Practice Exams](../practice-exams/)
- 🎯 [Exam Tips](exam-tips.md)
- 📖 [Glossary](glossary.md)

---

*Use this cheat sheet for quick review before your exam! 🎯*
