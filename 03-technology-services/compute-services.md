# 🖥️ Compute Services

> **"The foundation of cloud computing - where your applications come to life"**

## 🎯 Chapter Overview

**Study Time:** ~6 hours  
**Difficulty:** Beginner to Intermediate  
**Importance:** ⭐⭐⭐⭐⭐ (Core foundation!)

Compute services are the **engines of the cloud** - they provide the processing power that runs your applications. Understanding compute services is fundamental because every cloud application needs somewhere to run.

---

## 📋 Table of Contents

- [🏗️ Understanding Cloud Compute](#️-understanding-cloud-compute)
- [🖥️ Amazon EC2 (Elastic Compute Cloud)](#️-amazon-ec2-elastic-compute-cloud)
- [⚡ AWS Lambda (Serverless Computing)](#-aws-lambda-serverless-computing)
- [📦 Container Services](#-container-services)
- [🌟 Specialized Compute Services](#-specialized-compute-services)
- [🎯 Choosing the Right Compute Service](#-choosing-the-right-compute-service)
- [📝 Real-World Scenarios](#-real-world-scenarios)

---

## 🏗️ Understanding Cloud Compute

### 🤔 **What is Cloud Compute?**
Cloud compute provides **on-demand processing power** for running applications, without the need to buy, install, or maintain physical servers.

### 🏠 **Real-World Analogy: Housing Options**
Think of compute services like **different housing options**:

```
🏠 EC2 = Renting an Apartment
├── You get the whole space
├── You furnish and maintain it
├── You choose the size and location
└── You pay monthly rent

⚡ Lambda = Hotel Room Service
├── You just use what you need
├── Everything is provided
├── You pay per use
└── No maintenance required

📦 Containers = Furnished Apartment
├── Pre-configured environment
├── Portable between locations
├── Consistent setup everywhere
└── Shared building resources
```

### 📊 **Compute Service Categories**

| **Service Type** | **Management Level** | **Use Case** | **Billing** |
|------------------|-------------------|--------------|-------------|
| **Virtual Machines (EC2)** | High control | General applications | Per hour |
| **Serverless (Lambda)** | No infrastructure management | Event-driven functions | Per execution |
| **Containers** | Medium control | Microservices | Per resource used |
| **Specialized** | Varies | Specific workloads | Service-specific |

---

## 🖥️ Amazon EC2 (Elastic Compute Cloud)

### 🤔 **What is Amazon EC2?**
Amazon EC2 provides **resizable virtual servers in the cloud**. Think of it as renting computers in Amazon's data centers that you can configure and control remotely.

### 🏠 **Real-World Analogy: Apartment Rental**
EC2 is like **renting an apartment**:
- 🏠 **Choose apartment size** (instance type)
- 📍 **Pick location** (availability zone)
- 🏢 **Select building** (instance family)
- 🔑 **Get your keys** (key pairs)
- 🪑 **Furnish it yourself** (install software)
- 💰 **Pay monthly rent** (hourly billing)

### 🏗️ **EC2 Core Concepts**

#### **Instance Types**
EC2 offers different **"sizes" of virtual machines** optimized for different use cases:

**General Purpose (T3, M5, M6i):**
- 🎯 **Balanced** compute, memory, and networking
- 💼 **Use cases:** Web servers, small databases, development environments
- 💰 **Cost:** Moderate
- 📊 **Example:** t3.medium (2 vCPUs, 4 GB RAM)

**Compute Optimized (C5, C6i):**
- 🚀 **High-performance processors**
- 💼 **Use cases:** CPU-intensive applications, gaming servers, scientific computing
- 💰 **Cost:** Higher CPU focus
- 📊 **Example:** c5.large (2 vCPUs, 4 GB RAM, optimized CPU)

**Memory Optimized (R5, R6i, X1):**
- 🧠 **Large amounts of RAM**
- 💼 **Use cases:** In-memory databases, real-time analytics, caching
- 💰 **Cost:** Higher memory focus
- 📊 **Example:** r5.large (2 vCPUs, 16 GB RAM)

**Storage Optimized (I3, D2, D3):**
- 💾 **High-speed local storage**
- 💼 **Use cases:** NoSQL databases, data warehousing, file systems
- 💰 **Cost:** Higher storage focus
- 📊 **Example:** i3.large (2 vCPUs, 15.25 GB RAM, NVMe SSD)

#### **Instance Families Naming Convention**
```
Example: m5.large
├── m = Instance family (general purpose)
├── 5 = Generation (5th generation)
└── large = Size (small, medium, large, xlarge, etc.)
```

### 💰 **EC2 Pricing Models**

#### **On-Demand Instances**
- 💳 **Pay by the hour/second** with no long-term commitments
- 🎯 **Best for:** Unpredictable workloads, development, testing
- 📊 **Pricing:** Highest per-hour cost
- ✅ **Pros:** Maximum flexibility, no commitments
- ❌ **Cons:** Most expensive option

**Example Use Case:**
```
Development Environment:
- Developers work 8 hours/day, 5 days/week
- Instances running only when needed
- Usage varies based on project phases
- On-demand perfect for flexible usage
```

#### **Reserved Instances (RIs)**
- 🏷️ **1 or 3-year commitment** for significant discounts
- 🎯 **Best for:** Steady, predictable workloads
- 📊 **Savings:** Up to 75% compared to on-demand
- ✅ **Pros:** Major cost savings for consistent usage
- ❌ **Cons:** Commitment required, less flexibility

**RI Payment Options:**
- **All Upfront:** Pay everything upfront, maximum discount
- **Partial Upfront:** Pay some upfront, monthly payments
- **No Upfront:** No upfront payment, monthly payments only

**Example Use Case:**
```
Production Web Server:
- Runs 24/7/365
- Consistent traffic patterns
- 3-year business plan
- Reserved Instance saves 60% vs on-demand
```

#### **Spot Instances**
- 💰 **Bid on unused capacity** at up to 90% discount
- 🎯 **Best for:** Fault-tolerant, flexible workloads
- 📊 **Savings:** Up to 90% compared to on-demand
- ✅ **Pros:** Massive cost savings
- ❌ **Cons:** Can be terminated with 2-minute notice

**Example Use Case:**
```
Data Processing Job:
- Process large datasets overnight
- Job can restart if interrupted
- Not time-critical
- Spot instances provide 80% cost savings
```

#### **Dedicated Hosts**
- 🏠 **Physical server dedicated** to your use
- 🎯 **Best for:** Compliance requirements, licensing
- 📊 **Cost:** Most expensive option
- ✅ **Pros:** Full control, compliance, bring your own licenses
- ❌ **Cons:** Highest cost, fixed capacity

### 🔄 **Auto Scaling**

#### 🤔 **What is Auto Scaling?**
Auto Scaling automatically **adjusts the number of EC2 instances** based on demand, ensuring you have the right capacity at the right time.

#### 🎢 **Real-World Analogy: Restaurant Staffing**
Auto Scaling is like **smart restaurant staffing**:
- 📈 **Busy dinner rush** → Call in more waiters (scale up)
- 📉 **Slow Tuesday afternoon** → Send waiters home (scale down)
- 📊 **Monitor customer flow** → Adjust staff levels automatically
- 💰 **Cost optimization** → Pay for staff only when needed

#### 📊 **Auto Scaling Example**
```
E-commerce Website Auto Scaling:

Normal Traffic (100 users):
├── 2 EC2 instances running
├── CPU usage: 30%
└── Response time: 200ms

Black Friday (10,000 users):
├── Auto Scaling detects high CPU (80%)
├── Launches 8 additional instances
├── Traffic distributed across 10 instances
├── CPU usage: 35%
└── Response time: 220ms

After Black Friday:
├── Traffic returns to normal
├── Auto Scaling terminates extra instances
├── Back to 2 instances
└── Cost optimized automatically
```

### 🏷️ **EC2 Use Cases**

#### 🌐 **Web Hosting**
- **Scenario:** Company website with varying traffic
- **Solution:** Auto Scaling Group with Application Load Balancer
- **Benefits:** Handle traffic spikes, cost optimization
- **Instance type:** General purpose (t3.medium)

#### 🎮 **Game Servers**
- **Scenario:** Multiplayer online game
- **Solution:** Compute optimized instances in multiple regions
- **Benefits:** Low latency, high performance
- **Instance type:** Compute optimized (c5.large)

#### 📊 **Data Analysis**
- **Scenario:** Processing large datasets
- **Solution:** Memory optimized instances with spot pricing
- **Benefits:** High memory, cost-effective for batch jobs
- **Instance type:** Memory optimized (r5.xlarge)

---

## ⚡ AWS Lambda (Serverless Computing)

### 🤔 **What is AWS Lambda?**
AWS Lambda lets you **run code without managing servers**. You upload your code, and AWS handles everything else - servers, scaling, patching, monitoring.

### 🏨 **Real-World Analogy: Hotel Room Service**
Lambda is like **hotel room service**:
- 📞 **Call when you need something** (trigger function)
- 🍽️ **Service provided instantly** (code executes)
- 💰 **Pay only for what you order** (pay per execution)
- 🧹 **No cleanup required** (AWS handles everything)
- ⏰ **Available 24/7** (always ready to respond)

### 🎯 **Lambda Core Concepts**

#### **Function**
- 📝 **Your code** packaged with dependencies
- ⏱️ **Runs for maximum 15 minutes**
- 💾 **Memory allocation:** 128 MB to 10,008 MB
- 🔧 **Runtime environments:** Python, Node.js, Java, C#, Go, Ruby

#### **Event-Driven Execution**
Lambda functions are **triggered by events**:
```
Common Triggers:
├── 📁 S3 file upload
├── 🌐 API Gateway request
├── 📧 SNS notification
├── ⏰ CloudWatch scheduled event
├── 🗄️ DynamoDB table change
└── 📱 Alexa skill invocation
```

#### **Pay-Per-Use Pricing**
- 💰 **No servers to pay for** when not running
- 📊 **Charged per request** and compute time
- 🆓 **Free tier:** 1 million requests/month
- 💵 **Cost example:** $0.20 per 1 million requests

### 🎯 **Lambda Use Cases**

#### 📸 **Image Processing**
```
Scenario: Photo sharing app

Workflow:
1. 📱 User uploads photo to S3
2. 🔔 S3 triggers Lambda function
3. 🖼️ Lambda resizes image to multiple sizes
4. 💾 Saves thumbnails back to S3
5. 📱 Updates database with image metadata

Benefits:
- No servers to manage
- Scales automatically with uploads
- Pay only when processing images
- Responds in real-time
```

#### 🔔 **Real-Time Notifications**
```
Scenario: E-commerce order processing

Workflow:
1. 🛒 Customer places order in app
2. 📨 Order data sent to Lambda
3. 📧 Lambda sends confirmation email
4. 📱 Pushes notification to mobile app
5. 📊 Updates analytics dashboard

Benefits:
- Instant response to orders
- No infrastructure to maintain
- Scales with order volume
- Cost-effective for sporadic events
```

#### 🤖 **API Backend**
```
Scenario: Mobile app backend

Architecture:
API Gateway → Lambda Functions → DynamoDB

Functions:
├── User authentication
├── Data retrieval
├── Business logic processing
└── Third-party integrations

Benefits:
- Serverless API endpoints
- Automatic scaling
- Pay per API call
- Focus on business logic
```

### ⚖️ **EC2 vs Lambda Comparison**

| **Aspect** | **EC2** | **Lambda** |
|------------|---------|------------|
| **Management** | You manage servers | AWS manages everything |
| **Scaling** | Manual/Auto Scaling | Automatic and instant |
| **Pricing** | Pay for server time | Pay per execution |
| **Runtime** | Always running | Runs only when triggered |
| **Use Case** | Long-running applications | Event-driven functions |
| **Cold Start** | Always warm | Potential cold start delay |
| **Execution Time** | Unlimited | Maximum 15 minutes |

---

## 📦 Container Services

### 🤔 **What are Containers?**
Containers package your **application with all its dependencies** into a portable unit that runs consistently across different environments.

### 📦 **Real-World Analogy: Shipping Containers**
Containers are like **standardized shipping containers**:
- 📦 **Standardized packaging** - Same size and interface everywhere
- 🚢 **Portable** - Move from ship to truck to train
- 🔒 **Isolated** - Contents don't affect each other
- 📋 **Inventory control** - Know exactly what's inside
- ⚡ **Efficient loading** - Quick to move and deploy

### 🐳 **Container vs Virtual Machine**

```
Virtual Machine:
┌─────────────────────────────┐
│ Application                 │
├─────────────────────────────┤
│ Guest Operating System      │
├─────────────────────────────┤
│ Hypervisor                  │
├─────────────────────────────┤
│ Host Operating System       │
├─────────────────────────────┤
│ Physical Infrastructure     │
└─────────────────────────────┘

Container:
┌─────────────────────────────┐
│ Application                 │
├─────────────────────────────┤
│ Container Runtime           │
├─────────────────────────────┤
│ Host Operating System       │
├─────────────────────────────┤
│ Physical Infrastructure     │
└─────────────────────────────┘
```

### 🎯 **AWS Container Services**

#### **Amazon ECS (Elastic Container Service)**
- 🎯 **AWS-native container orchestration**
- 🔧 **Fully managed** by AWS
- 💰 **No additional charges** for ECS itself
- 🎮 **Easy to use** with AWS services

**ECS Use Case:**
```
Microservices Web Application:
├── Frontend container (React app)
├── API container (Node.js)
├── Authentication container (Java)
└── Database container (PostgreSQL)

Benefits:
- Each service scales independently
- Easy deployment and updates
- Integrated with AWS services
- Cost-effective operation
```

#### **Amazon EKS (Elastic Kubernetes Service)**
- ☸️ **Managed Kubernetes service**
- 🌍 **Industry-standard** container orchestration
- 🔧 **AWS-managed control plane**
- 🔗 **Compatible with existing Kubernetes tools**

**EKS Use Case:**
```
Enterprise Application Migration:
├── Existing Kubernetes applications
├── Multi-cloud strategy requirements
├── Advanced orchestration needs
└── Large development teams

Benefits:
- Use existing Kubernetes expertise
- Portable across cloud providers
- Advanced scheduling and networking
- Rich ecosystem of tools
```

#### **AWS Fargate**
- 🚫 **Serverless containers** - No server management
- 💰 **Pay only for resources used**
- 🔄 **Works with both ECS and EKS**
- ⚡ **Instant scaling**

**Fargate Use Case:**
```
Event-Driven Processing:
├── Container triggered by events
├── Processes data and exits
├── No servers to manage
└── Pay only during execution

Benefits:
- No infrastructure management
- Perfect for batch jobs
- Automatic scaling
- Cost optimization
```

---

## 🌟 Specialized Compute Services

### 🏢 **Amazon Lightsail**

#### 🤔 **What is Lightsail?**
Amazon Lightsail provides **simple virtual private servers** with predictable pricing for small-scale applications.

#### 🎯 **Real-World Analogy: Studio Apartment**
Lightsail is like a **furnished studio apartment**:
- 🏠 **Everything included** - Server, storage, networking
- 💰 **Fixed monthly price** - Predictable costs
- 🎯 **Simple setup** - No complex configuration
- 📊 **Perfect for small needs** - Personal projects, small businesses

#### 💼 **Lightsail Use Cases**
- 🌐 **Simple websites** - WordPress, static sites
- 🛒 **Small e-commerce** - Basic online stores
- 👨‍💻 **Development environments** - Testing and prototyping
- 📚 **Learning projects** - Students and beginners

### ⚙️ **AWS Batch**

#### 🤔 **What is AWS Batch?**
AWS Batch **manages batch computing workloads**, automatically provisioning and scaling compute resources.

#### 🏭 **Real-World Analogy: Factory Production Line**
Batch is like an **automated factory**:
- 📋 **Job queue** - Orders waiting to be processed
- 🏭 **Production line** - Compute resources doing work
- 🔄 **Automatic scaling** - Add/remove production lines based on orders
- 📊 **Quality control** - Monitor and manage job completion

#### 💼 **Batch Use Cases**
- 🧬 **Scientific computing** - Genome analysis, climate modeling
- 📊 **Financial analysis** - Risk calculations, portfolio optimization
- 🎬 **Media processing** - Video rendering, image analysis
- 📈 **Data processing** - ETL jobs, log analysis

### 🏢 **AWS Outposts**

#### 🤔 **What is AWS Outposts?**
AWS Outposts brings **AWS services to your on-premises data center**, providing hybrid cloud capabilities.

#### 🏠 **Real-World Analogy: Home Office Extension**
Outposts is like **extending your office to your home**:
- 🏢 **Same tools** - Use same AWS services on-premises
- 🔗 **Connected** - Seamless integration with AWS cloud
- 🔒 **Local control** - Keep sensitive data on-premises
- 📊 **Consistent experience** - Same APIs and management tools

#### 💼 **Outposts Use Cases**
- 🏥 **Healthcare** - Keep patient data on-premises for compliance
- 🏭 **Manufacturing** - Low-latency processing for factory automation
- 🏛️ **Government** - Data sovereignty requirements
- 💰 **Financial services** - Ultra-low latency trading applications

---

## 🎯 Choosing the Right Compute Service

### 🤔 **Decision Framework**

#### **Ask These Questions:**

1. **🏗️ How much control do you need?**
   - **Full control** → EC2
   - **No server management** → Lambda or Fargate
   - **Simple setup** → Lightsail

2. **⏰ How long does your code run?**
   - **Always running** → EC2
   - **Short tasks (< 15 min)** → Lambda
   - **Batch jobs** → Batch or Spot instances

3. **📈 How predictable is your workload?**
   - **Steady usage** → Reserved Instances
   - **Variable/spiky** → Auto Scaling or Lambda
   - **Unpredictable/interruptible** → Spot Instances

4. **💰 What's your cost priority?**
   - **Lowest cost** → Spot Instances or Lambda
   - **Predictable cost** → Reserved Instances or Lightsail
   - **Pay per use** → Lambda or Fargate

### 📊 **Service Selection Matrix**

| **Use Case** | **Best Service** | **Why** |
|--------------|------------------|---------|
| **Corporate website** | EC2 + Auto Scaling | Consistent performance, cost optimization |
| **Image processing** | Lambda | Event-driven, pay per use |
| **Microservices app** | ECS/EKS + Fargate | Container benefits, no server management |
| **Personal blog** | Lightsail | Simple, predictable pricing |
| **Data analysis** | Batch + Spot | Cost-effective batch processing |
| **Gaming server** | EC2 Dedicated | Consistent performance, full control |

### 🏗️ **Architecture Patterns**

#### **Simple Web Application**
```
Internet → ALB → EC2 (Auto Scaling) → RDS
├── Application Load Balancer distributes traffic
├── Auto Scaling adjusts capacity
├── EC2 instances run application
└── RDS provides database backend
```

#### **Serverless API**
```
Mobile App → API Gateway → Lambda → DynamoDB
├── API Gateway handles HTTP requests
├── Lambda functions process business logic
├── DynamoDB stores application data
└── Pay only for actual usage
```

#### **Microservices Platform**
```
Users → ALB → ECS/Fargate Services → Various Backends
├── Load balancer routes to appropriate services
├── Each microservice runs in containers
├── Services scale independently
└── Fargate eliminates server management
```

---

## 📝 Real-World Scenarios

### 🛒 **Scenario 1: E-commerce Startup**

**Situation:**
- New online store launching
- Expecting variable traffic
- Limited budget and technical expertise
- Need to scale quickly if successful

**Requirements:**
- Handle traffic spikes during sales
- Cost-effective solution
- Easy to manage
- Quick deployment

**Recommended Solution:**
```
Architecture:
├── Lightsail for initial simple website
├── Migrate to EC2 + Auto Scaling when growth starts
├── Lambda for order processing functions
└── Consider containers as app complexity grows

Migration Path:
Phase 1: Lightsail (simple, predictable)
Phase 2: EC2 + Auto Scaling (handle growth)
Phase 3: Containerized microservices (scale complexity)
```

**Benefits:**
- Start simple and cost-effective
- Scale architecture with business growth
- Pay for what you actually use
- Focus on business, not infrastructure

### 🏥 **Scenario 2: Healthcare Data Processing**

**Situation:**
- Process medical imaging data
- Large files, intensive computation
- Batch processing overnight
- Strict compliance requirements

**Requirements:**
- High compute power when needed
- Cost optimization for batch workloads
- Compliance with healthcare regulations
- Reliable processing of critical data

**Recommended Solution:**
```
Architecture:
├── S3 for medical image storage
├── Batch for orchestrating processing jobs
├── Spot Instances for cost-effective compute
├── Lambda for triggering and monitoring
└── CloudTrail for compliance auditing

Workflow:
1. Medical images uploaded to S3
2. Lambda triggers Batch job
3. Batch provisions Spot Instances
4. Images processed overnight
5. Results stored back to S3
6. Instances terminated automatically
```

**Benefits:**
- 70% cost savings with Spot Instances
- Automatic scaling for variable workloads
- Built-in compliance features
- No infrastructure management overhead

### 🎮 **Scenario 3: Mobile Gaming Backend**

**Situation:**
- Multiplayer mobile game
- Global player base
- Real-time interactions required
- Unpredictable player activity

**Requirements:**
- Low latency worldwide
- Handle concurrent players
- Real-time data processing
- Cost optimization for varying load

**Recommended Solution:**
```
Architecture:
├── API Gateway for global API endpoints
├── Lambda for game logic functions
├── DynamoDB for player data (global tables)
├── ECS for real-time game sessions
└── CloudFront for content delivery

Scaling Strategy:
- Lambda handles player authentication/stats
- ECS manages real-time game sessions
- Auto Scaling adjusts to player count
- Global deployment for low latency
```

**Benefits:**
- Serverless scales automatically
- Global low latency
- Pay per player activity
- Focus on game development

---

## 🧠 Memory Aids

### 🎯 **Service Memory Tricks**

#### **EC2 = Elastic Compute Cloud**
- **E**lastic = Scales up and down
- **C**ompute = Processing power
- **C**loud = Virtual servers in AWS

#### **Lambda = Serverless Functions**
- **λ (Lambda symbol)** = Mathematical function
- **Event-driven** = Responds to triggers
- **Pay per execution** = No idle costs

#### **Container Services**
- **ECS** = **E**lastic **C**ontainer **S**ervice (AWS native)
- **EKS** = **E**lastic **K**ubernetes **S**ervice (industry standard)
- **Fargate** = **Far**away **gate** = No servers to see

### 📊 **Decision Tree**
```
Need compute? Start here:
├── Always running? 
│   ├── Yes → EC2 (with Auto Scaling)
│   └── No → Event-driven?
│       ├── Yes → Lambda
│       └── No → Batch processing?
│           ├── Yes → AWS Batch
│           └── No → Consider containers
├── Need containers?
│   ├── Simple → ECS
│   ├── Kubernetes → EKS
│   └── No servers → Fargate
└── Want simplicity? → Lightsail
```

---

## ✅ Chapter Checklist

Before proceeding, ensure you can:

- [ ] Explain when to use EC2 vs Lambda vs containers
- [ ] Understand EC2 pricing models (On-Demand, Reserved, Spot)
- [ ] Identify Auto Scaling benefits and use cases
- [ ] Recognize serverless computing advantages
- [ ] Choose appropriate container services
- [ ] Match compute services to business scenarios
- [ ] Understand cost optimization strategies

---

## 🎯 Practice Questions

### Question 1
A company has a web application that experiences predictable traffic during business hours but very little traffic at night and weekends. Which compute solution would be most cost-effective?

A) EC2 Reserved Instances
B) EC2 On-Demand with Auto Scaling
C) AWS Lambda
D) EC2 Dedicated Hosts

<details>
<summary>💡 Click for Answer</summary>

**Answer: B) EC2 On-Demand with Auto Scaling**

**Explanation:** Auto Scaling with On-Demand instances allows the application to scale down during low-traffic periods and scale up during business hours, paying only for the capacity actually needed. Lambda would be better for unpredictable, event-driven workloads, while Reserved Instances are better for consistent 24/7 usage.
</details>

### Question 2
A startup needs to process uploaded images by resizing them and applying filters. The processing is triggered when images are uploaded to S3. Which service is best suited for this use case?

A) Amazon EC2
B) AWS Lambda
C) Amazon ECS
D) AWS Batch

<details>
<summary>💡 Click for Answer</summary>

**Answer: B) AWS Lambda**

**Explanation:** Lambda is perfect for event-driven processing triggered by S3 uploads. It automatically scales, requires no server management, and you pay only when images are processed. The short-duration image processing task fits well within Lambda's execution time limits.
</details>

### Question 3
Which EC2 pricing model offers the largest discount but requires a 1-3 year commitment?

A) On-Demand Instances
B) Spot Instances
C) Reserved Instances
D) Dedicated Hosts

<details>
<summary>💡 Click for Answer</summary>

**Answer: C) Reserved Instances**

**Explanation:** Reserved Instances offer up to 75% savings compared to On-Demand pricing in exchange for a 1 or 3-year commitment. While Spot Instances can offer up to 90% savings, they don't require commitments but can be terminated with little notice.
</details>

---

## 🗺️ What's Next?

Now that you understand how to run applications in the cloud, let's explore where and how to store the data your applications need.

**🎯 Next Chapter:** [Storage Services](./storage-services.md)

Learn about the various storage options AWS provides and when to use each one!

---

**🎉 Excellent foundation!** You now understand the compute services that power applications in the cloud. Next, we'll explore where all that data lives.

---

**← [Back to Domain 3 Overview](./README.md)**
