# 🛡️ Core Security Services

> **"Defense in depth - AWS provides layers of security controls to protect your infrastructure"**

## 🎯 Chapter Overview

**Study Time:** ~6 hours  
**Difficulty:** Intermediate to Advanced  
**Importance:** ⭐⭐⭐⭐ (Many exam questions!)

AWS offers a comprehensive suite of security services that work together to provide defense in depth. This chapter covers the core security services you need to know for the Cloud Practitioner exam and real-world implementation.

---

## 📋 Table of Contents

- [🏰 Defense in Depth Strategy](#-defense-in-depth-strategy)
- [🔐 Data Protection Services](#-data-protection-services)
- [🌐 Network Security Services](#-network-security-services)
- [🔍 Monitoring & Logging Services](#-monitoring--logging-services)
- [🛡️ Threat Detection Services](#️-threat-detection-services)
- [📋 Compliance & Governance Services](#-compliance--governance-services)
- [🎯 Service Selection Guide](#-service-selection-guide)

---

## 🏰 Defense in Depth Strategy

### 🤔 **What is Defense in Depth?**
Defense in depth is a security strategy that uses **multiple layers of security controls** to protect information and systems. If one layer fails, other layers continue to provide protection.

### 🏰 **Castle Analogy**
Think of AWS security like a **medieval castle defense system**:

```
🏰 Castle Defense Layers:
1. 🌊 Moat (Network perimeter)
2. 🏛️ Outer walls (VPC, Security Groups)
3. 🚪 Gates (IAM, Access Controls)
4. 👥 Guards (Monitoring, Detection)
5. 🗝️ Vault (Encryption, Data Protection)
6. 📜 Records (Logging, Auditing)
```

### 📊 **AWS Security Service Categories**

| **Category** | **Purpose** | **Key Services** |
|--------------|-------------|------------------|
| **🔐 Data Protection** | Encrypt and protect data | KMS, CloudHSM, Certificate Manager |
| **🌐 Network Security** | Control network access | Security Groups, WAF, Shield |
| **🔍 Detection & Monitoring** | Find and track issues | CloudTrail, Config, GuardDuty |
| **🛡️ Threat Response** | Respond to threats | Inspector, Macie, Security Hub |
| **📋 Compliance** | Meet regulations | Artifact, Control Tower, Organizations |

---

## 🔐 Data Protection Services

### 🗝️ **AWS Key Management Service (KMS)**

#### 🤔 **What is KMS?**
AWS KMS is a **managed encryption service** that makes it easy to create, control, and use encryption keys to protect your data.

#### 🏠 **Real-World Analogy: Bank Safe Deposit Box**
KMS is like a **bank's safe deposit box system**:
- 🏦 **Bank (AWS)** provides the secure vault infrastructure
- 🗝️ **Your keys** control access to your specific box
- 🔒 **Dual control** - You need your key + bank security
- 📋 **Audit trail** - Bank tracks every access
- 🔄 **Key rotation** - Bank can help you change locks

#### 🔑 **KMS Key Types**

**Customer Managed Keys:**
- 👤 **You control** the key lifecycle
- 🔄 **You manage** rotation policies
- 📊 **You set** usage policies
- 💰 **Cost:** $1/month per key + usage

**AWS Managed Keys:**
- 🤖 **AWS manages** the key automatically
- 🔄 **Automatic rotation** every year
- 🔒 **Service-specific** - One per service per region
- 💰 **Cost:** Free (usage charges apply)

**AWS Owned Keys:**
- 🏢 **AWS owns and manages** completely
- 🔒 **Shared across customers** (but isolated)
- 🚫 **No direct access** or control
- 💰 **Cost:** Free

#### 🎯 **KMS Use Cases**
- 📁 **S3 bucket encryption** - Protect files at rest
- 💾 **EBS volume encryption** - Protect disk data
- 🗄️ **RDS database encryption** - Protect database content
- 📱 **Application secrets** - Encrypt API keys, passwords
- 📊 **Lambda environment variables** - Protect function secrets

#### 📊 **KMS Example: S3 Encryption**
```
When you upload a file to S3 with KMS encryption:

1. 📁 You upload file to S3
2. 🔑 S3 requests encryption key from KMS
3. 🔐 KMS generates data key using your master key
4. 🔒 S3 encrypts file with data key
5. 🗑️ S3 discards plain text data key
6. 💾 S3 stores encrypted file + encrypted data key

When you download:
1. 📥 S3 retrieves encrypted file + encrypted data key
2. 🔑 S3 asks KMS to decrypt data key
3. 🔓 KMS decrypts data key (if you have permission)
4. 🔐 S3 decrypts file with data key
5. 📱 You receive decrypted file
```

### 🔒 **AWS CloudHSM**

#### 🤔 **What is CloudHSM?**
AWS CloudHSM provides **hardware security modules (HSMs)** in the AWS cloud for generating and using your own encryption keys.

#### 🏦 **Real-World Analogy: Private Vault**
CloudHSM is like having your **own private vault**:
- 🏠 **Your own vault** (dedicated hardware)
- 🗝️ **Only you have keys** (single-tenant)
- 🔒 **Bank-grade security** (FIPS 140-2 Level 3)
- 👤 **You control everything** (full administrative control)

#### ⚖️ **KMS vs CloudHSM Comparison**

| **Aspect** | **KMS** | **CloudHSM** |
|------------|---------|--------------|
| **Tenancy** | Multi-tenant | Single-tenant |
| **Management** | AWS managed | Customer managed |
| **Cost** | Lower | Higher |
| **Performance** | Standard | High performance |
| **Compliance** | FIPS 140-2 Level 2 | FIPS 140-2 Level 3 |
| **Use Case** | General encryption | Specialized compliance |

### 📜 **AWS Certificate Manager (ACM)**

#### 🤔 **What is ACM?**
AWS Certificate Manager provisions, manages, and deploys **SSL/TLS certificates** for use with AWS services.

#### 🛡️ **Why SSL/TLS Certificates Matter**
- 🔐 **Encrypt data in transit** - Protect data moving between client and server
- ✅ **Authentication** - Prove you are who you say you are
- 🔒 **Data integrity** - Ensure data isn't modified in transit
- 🌐 **Browser trust** - Avoid security warnings

#### 🎯 **ACM Features**
- 🆓 **Free SSL certificates** for AWS services
- 🔄 **Automatic renewal** - No more expired certificates
- 🚀 **Easy deployment** - Automatic integration with CloudFront, ALB, API Gateway
- 🔒 **Wild card support** - Single certificate for multiple subdomains

#### 📊 **ACM Use Case Example**
```
E-commerce Website Security:

1. 🛒 Request certificate for shop.company.com
2. ✅ ACM validates domain ownership
3. 📜 ACM issues free SSL certificate
4. 🔗 Attach certificate to Application Load Balancer
5. 🔐 Customer traffic encrypted automatically
6. 🔄 ACM renews certificate before expiration
```

---

## 🌐 Network Security Services

### 🛡️ **Security Groups**

#### 🤔 **What are Security Groups?**
Security Groups act as **virtual firewalls** that control inbound and outbound traffic to AWS resources.

#### 🚪 **Real-World Analogy: Nightclub Bouncer**
Security Groups are like **nightclub bouncer**:
- 👥 **Check the list** - Only allow traffic that matches rules
- 🚪 **Guard the entrance** - Control who gets in
- 📋 **Different rules** - VIP list, general admission, staff
- 🔄 **Stateful** - If someone gets in, they can get out

#### 🎯 **Security Group Characteristics**
- 🔒 **Default deny** - All traffic blocked unless explicitly allowed
- ✅ **Allow rules only** - Cannot create deny rules
- 🔄 **Stateful** - Return traffic automatically allowed
- 🎯 **Instance level** - Applied to specific instances
- 🔗 **Rule references** - Can reference other security groups

#### 📊 **Security Group Example: Web Server**
```
Web Server Security Group:
┌─────────────────────────────────────┐
│ Inbound Rules:                      │
│ ✅ HTTP (80) from 0.0.0.0/0         │
│ ✅ HTTPS (443) from 0.0.0.0/0       │
│ ✅ SSH (22) from Admin-SG           │
│                                     │
│ Outbound Rules:                     │
│ ✅ All traffic (default)            │
└─────────────────────────────────────┘

Admin Security Group:
┌─────────────────────────────────────┐
│ Inbound Rules:                      │
│ ✅ SSH (22) from Office-IP          │
│ ✅ RDP (3389) from Office-IP        │
└─────────────────────────────────────┘
```

### 🌐 **Network Access Control Lists (NACLs)**

#### 🤔 **What are NACLs?**
Network ACLs provide **subnet-level security** that acts as an additional layer of firewall protection.

#### 🏢 **Real-World Analogy: Building Security vs Office Security**
- 🏢 **NACLs = Building security** - Controls who enters the building (subnet)
- 🚪 **Security Groups = Office security** - Controls who enters specific offices (instances)

#### ⚖️ **Security Groups vs NACLs**

| **Aspect** | **Security Groups** | **NACLs** |
|------------|-------------------|-----------|
| **Level** | Instance | Subnet |
| **Rules** | Allow only | Allow and Deny |
| **State** | Stateful | Stateless |
| **Evaluation** | All rules | Rules in order |
| **Default** | Deny all inbound | Allow all traffic |

### 🛡️ **AWS WAF (Web Application Firewall)**

#### 🤔 **What is AWS WAF?**
AWS WAF is a **web application firewall** that protects web applications from common web exploits and attacks.

#### 🛡️ **Real-World Analogy: Security Scanner**
WAF is like **airport security scanner**:
- 🔍 **Inspect everything** - Examines all web requests
- 🚫 **Block threats** - Stops dangerous items (malicious requests)
- 📋 **Rule-based** - Uses predefined and custom security rules
- 🚀 **Fast processing** - Minimal impact on legitimate traffic

#### 🎯 **Common WAF Protection Rules**
- 🚫 **SQL Injection** - Prevents database attacks
- 🚫 **Cross-Site Scripting (XSS)** - Blocks malicious scripts
- 🚫 **IP reputation** - Blocks known malicious IP addresses
- 🚫 **Geographic blocking** - Restricts access by country
- 🚫 **Rate limiting** - Prevents DDoS attacks
- 🚫 **Size restrictions** - Blocks oversized requests

#### 📊 **WAF Use Case: E-commerce Protection**
```
E-commerce Website Protection:

Incoming Request: POST /login
├── WAF Rule 1: Check for SQL injection patterns
├── WAF Rule 2: Validate request size
├── WAF Rule 3: Check IP reputation
├── WAF Rule 4: Rate limiting (max 10 requests/minute)
└── Decision: Allow/Block request

If ALLOWED: Request goes to application
If BLOCKED: Return 403 Forbidden error
```

### 🛡️ **AWS Shield**

#### 🤔 **What is AWS Shield?**
AWS Shield provides **DDoS (Distributed Denial of Service) protection** for applications running on AWS.

#### 🌊 **Real-World Analogy: Flood Protection**
Shield is like **flood protection system**:
- 🌊 **DDoS = Flood** - Overwhelming volume of malicious traffic
- 🛡️ **Shield = Levees** - Absorbs and redirects attack traffic
- 🏠 **Your app = House** - Protected behind the flood barriers
- 📊 **Monitoring = Weather system** - Detects attacks early

#### 🎯 **Shield Tiers**

**AWS Shield Standard:**
- 🆓 **Free for all customers**
- 🛡️ **Protection against common attacks** (Layer 3/4)
- 🚀 **Automatic protection** - Always on
- 📊 **Basic attack diagnostics**

**AWS Shield Advanced:**
- 💰 **$3,000/month per organization**
- 🛡️ **Enhanced protection** (Layer 3/4/7)
- 👥 **24/7 DRT support** (DDoS Response Team)
- 💰 **Cost protection** - Refund scaling charges during attacks
- 📊 **Advanced attack diagnostics**

---

## 🔍 Monitoring & Logging Services

### 📊 **AWS CloudTrail**

#### 🤔 **What is CloudTrail?**
AWS CloudTrail provides **governance, compliance, and audit** for your AWS account by logging all API calls.

#### 📚 **Real-World Analogy: Security Camera System**
CloudTrail is like **comprehensive security camera system**:
- 📹 **Records everything** - Every action in your AWS account
- ⏰ **Timestamp everything** - When, where, who, what
- 💾 **Stores recordings** - Keeps logs for investigation
- 🔍 **Searchable** - Find specific events quickly
- 🚨 **Alerts** - Notify when suspicious activity occurs

#### 🎯 **What CloudTrail Logs**
- 👥 **User activity** - Console logins, API calls
- 🔧 **Administrative actions** - Creating/deleting resources
- 🔒 **Security events** - Permission changes, failed logins
- 💰 **Billing events** - Cost allocation changes
- 🔄 **Configuration changes** - Resource modifications

#### 📊 **CloudTrail Log Example**
```json
{
  "eventTime": "2024-06-17T10:30:45Z",
  "eventName": "CreateBucket",
  "eventSource": "s3.amazonaws.com",
  "userIdentity": {
    "type": "IAMUser",
    "userName": "john.developer"
  },
  "sourceIPAddress": "203.0.113.12",
  "requestParameters": {
    "bucketName": "my-company-data-bucket"
  },
  "responseElements": {
    "location": "https://my-company-data-bucket.s3.amazonaws.com/"
  }
}
```

#### 🎯 **CloudTrail Best Practices**
- ✅ **Enable in all regions** - Don't miss any activity
- 🔐 **Encrypt log files** - Protect sensitive audit data
- 🔒 **Restrict access** - Only security team should access logs
- 📊 **Set up alerts** - Monitor for critical events
- 💾 **Long-term storage** - Keep logs for compliance requirements

### ⚙️ **AWS Config**

#### 🤔 **What is AWS Config?**
AWS Config continuously **monitors and records AWS resource configurations** and allows you to automate the evaluation of recorded configurations.

#### 📊 **Real-World Analogy: Home Security System**
Config is like **home security monitoring system**:
- 📹 **Continuous monitoring** - Always watching your house
- 📋 **Configuration inventory** - Knows every door, window, alarm
- 🚨 **Compliance alerts** - Alerts when something isn't right
- 📈 **Change tracking** - Records when anything changes
- 🔄 **Auto-remediation** - Can fix some issues automatically

#### 🎯 **Config Capabilities**
- 📊 **Configuration snapshots** - Point-in-time resource configurations
- 🔄 **Change tracking** - History of configuration changes
- 📋 **Compliance monitoring** - Check against rules and standards
- 🔧 **Auto-remediation** - Automatically fix non-compliant resources
- 📈 **Drift detection** - Identify configuration drift

#### 📊 **Config Rule Examples**
```
Compliance Rules:
├── S3-bucket-public-access-prohibited
├── EC2-security-group-attached-to-eni
├── RDS-storage-encrypted
├── IAM-password-policy
└── EIP-attached (Elastic IPs should be attached)

Remediation Actions:
├── Remove public access from S3 buckets
├── Stop unencrypted EC2 instances
├── Delete unused Elastic IPs
└── Send notifications to security team
```

---

## 🛡️ Threat Detection Services

### 🔍 **Amazon GuardDuty**

#### 🤔 **What is GuardDuty?**
Amazon GuardDuty is a **threat detection service** that uses machine learning to identify malicious activity and unauthorized behavior.

#### 🕵️ **Real-World Analogy: AI Security Detective**
GuardDuty is like **AI-powered security detective**:
- 🤖 **AI-powered** - Uses machine learning to detect patterns
- 🔍 **Always investigating** - Continuously analyzes your environment
- 📊 **Pattern recognition** - Identifies unusual behavior
- 🚨 **Raises alerts** - Notifies you of potential threats
- 📚 **Learns continuously** - Gets smarter over time

#### 🎯 **GuardDuty Detection Sources**
- 📊 **VPC Flow Logs** - Network traffic analysis
- 🌐 **DNS logs** - DNS query analysis
- 📋 **CloudTrail logs** - API call analysis
- 🌍 **Threat intelligence** - Known malicious IPs and domains

#### 🚨 **GuardDuty Finding Types**
- 🏴‍☠️ **Malware** - EC2 instances communicating with malware C&C
- 🕳️ **Backdoors** - Unusual network communication patterns
- 💣 **Cryptocurrency mining** - Unauthorized mining activity
- 🎣 **Reconnaissance** - Scanning and probing activities
- 🔓 **Compromised instances** - Instances exhibiting malicious behavior

#### 📊 **GuardDuty Finding Example**
```
Finding: UnauthorizedAPICall
┌─────────────────────────────────────────┐
│ Severity: HIGH                          │
│ Account: 123456789012                   │
│ Region: us-east-1                       │
│ Resource: IAM User (suspicious.user)    │
│ Description: Unusual API call pattern   │
│ detected from new geolocation          │
│                                         │
│ Evidence:                               │
│ - 50+ API calls in 5 minutes           │
│ - Never seen this IP before            │
│ - Geolocation: Unknown country         │
│ - Time: Outside normal hours           │
└─────────────────────────────────────────┘
```

### 🔍 **Amazon Inspector**

#### 🤔 **What is Inspector?**
Amazon Inspector is a **vulnerability assessment service** that automatically assesses applications for exposure, vulnerabilities, and deviations from best practices.

#### 🏥 **Real-World Analogy: Health Inspector**
Inspector is like **health inspector for your applications**:
- 🔍 **Scheduled inspections** - Regular vulnerability scans
- 📋 **Checklist-based** - Follows security best practices
- 📊 **Detailed reports** - Findings with severity levels
- 🎯 **Specific recommendations** - How to fix each issue
- 📈 **Trend tracking** - Security posture over time

#### 🎯 **Inspector Assessment Types**
- 🔒 **Network reachability** - Identifies network paths to EC2 instances
- 🛡️ **Security best practices** - Checks for common vulnerabilities
- 🔧 **Runtime behavior** - Analyzes application behavior
- 📦 **Software vulnerabilities** - Known CVEs in installed packages

### 📊 **Amazon Macie**

#### 🤔 **What is Macie?**
Amazon Macie is a **data security service** that uses machine learning to automatically discover, classify, and protect sensitive data.

#### 🕵️ **Real-World Analogy: Data Privacy Detective**
Macie is like **privacy detective for your data**:
- 🔍 **Scans all documents** - Examines your S3 buckets
- 📋 **Identifies sensitive data** - Finds PII, financial data, etc.
- 🚨 **Raises alerts** - Notifies about data exposure risks
- 📊 **Classification reports** - Detailed data inventory
- 🔒 **Suggests protection** - Recommends security measures

#### 🎯 **Macie Data Classifications**
- 👤 **Personally Identifiable Information (PII)** - Names, SSNs, emails
- 💳 **Financial data** - Credit card numbers, bank accounts
- 🏥 **Health information** - Medical records, patient data
- 📋 **Credentials** - API keys, passwords, certificates
- 📊 **Custom classifications** - Your organization's sensitive data types

---

## 📋 Compliance & Governance Services

### 📋 **AWS Artifact**

#### 🤔 **What is AWS Artifact?**
AWS Artifact provides **on-demand access to AWS security and compliance reports** and select online agreements.

#### 📚 **Real-World Analogy: Compliance Library**
Artifact is like **digital compliance library**:
- 📚 **Reference documents** - All compliance reports in one place
- 🔍 **Search capability** - Find specific certifications quickly
- 📥 **Download center** - Get reports for auditors
- 🔄 **Always updated** - Latest compliance status
- 🔒 **Secure access** - Controlled document distribution

#### 📋 **Available Reports**
- 🏆 **SOC reports** - SOC 1, SOC 2, SOC 3
- 🌍 **ISO certifications** - ISO 27001, ISO 27017, ISO 27018
- 🏛️ **Government** - FedRAMP, FISMA, FIPS 140-2
- 💳 **Payment** - PCI DSS attestation
- 🏥 **Healthcare** - HIPAA eligibility
- 🌍 **International** - C5, K-ISMS, MTCS

### 🏗️ **AWS Control Tower**

#### 🤔 **What is Control Tower?**
AWS Control Tower provides **the easiest way to set up and govern a secure, multi-account AWS environment** based on best practices.

#### 🏗️ **Real-World Analogy: Master Architect**
Control Tower is like **master architect for your AWS environment**:
- 📐 **Blueprint design** - Pre-designed security architecture
- 🏗️ **Automated construction** - Sets up accounts automatically
- 📋 **Building codes** - Enforces security and compliance standards
- 🔍 **Ongoing inspection** - Monitors for compliance drift
- 🎯 **Best practices** - Based on AWS Well-Architected Framework

#### 🎯 **Control Tower Features**
- 🏢 **Landing Zone** - Pre-configured multi-account setup
- 📋 **Guardrails** - Preventive and detective controls
- 🖥️ **Account Factory** - Standardized account provisioning
- 📊 **Dashboard** - Centralized governance view
- 🔄 **Drift detection** - Identifies configuration changes

---

## 🎯 Service Selection Guide

### 🤔 **When to Use Which Service**

#### 🔐 **Data Protection Scenarios**

| **Scenario** | **Use This Service** | **Why** |
|--------------|-------------------|---------|
| Encrypt S3 buckets | **KMS** | Managed encryption, easy integration |
| High-performance encryption | **CloudHSM** | Dedicated hardware, FIPS 140-2 Level 3 |
| SSL certificates for website | **ACM** | Free certificates, automatic renewal |
| Encrypt database passwords | **KMS** | Secure key management |

#### 🌐 **Network Security Scenarios**

| **Scenario** | **Use This Service** | **Why** |
|--------------|-------------------|---------|
| Control EC2 instance access | **Security Groups** | Instance-level firewall |
| Subnet-level restrictions | **NACLs** | Additional layer of protection |
| Protect web application | **WAF** | Application-layer filtering |
| DDoS protection | **Shield** | Absorbs attack traffic |

#### 🔍 **Monitoring Scenarios**

| **Scenario** | **Use This Service** | **Why** |
|--------------|-------------------|---------|
| Track who did what | **CloudTrail** | Complete audit trail |
| Monitor resource configurations | **Config** | Configuration compliance |
| Detect threats automatically | **GuardDuty** | ML-powered threat detection |
| Find vulnerable software | **Inspector** | Vulnerability assessment |
| Discover sensitive data | **Macie** | Data classification and protection |

### 🎯 **Security Architecture Patterns**

#### 🏢 **Small Business Pattern**
```
Essential Security Stack:
├── IAM (users, groups, MFA)
├── Security Groups (network controls)
├── CloudTrail (audit logging)
├── Config (compliance monitoring)
└── GuardDuty (threat detection)

Cost: ~$50-200/month
Complexity: Low
Coverage: Basic but solid foundation
```

#### 🏭 **Enterprise Pattern**
```
Comprehensive Security Stack:
├── IAM + Identity Federation
├── Security Groups + NACLs + WAF
├── CloudTrail + Config + GuardDuty
├── Inspector + Macie + Security Hub
├── KMS + CloudHSM (if needed)
├── Shield Advanced (if needed)
└── Control Tower (multi-account)

Cost: $1,000-10,000+/month
Complexity: High
Coverage: Enterprise-grade protection
```

#### 🏥 **Compliance-Heavy Pattern**
```
Compliance-Focused Stack:
├── All Enterprise services
├── Dedicated CloudHSM
├── Enhanced logging and monitoring
├── Automated compliance checking
├── Regular compliance reporting
└── 24/7 security operations

Cost: $10,000+/month
Complexity: Very High
Coverage: Meets strict regulations
```

---

## 🧠 Memory Aids

### 🎯 **Service Memory Tricks**

#### 🔐 **Data Protection**
- **KMS** = **K**ey **M**anagement **S**ervice (Keys for encryption)
- **ACM** = **A**utomated **C**ertificate **M**anagement (SSL certificates)
- **CloudHSM** = **H**ardware **S**ecurity **M**odule (Dedicated hardware)

#### 🌐 **Network Security**
- **WAF** = **W**eb **A**pplication **F**irewall (Protects web apps)
- **Shield** = Protection from DDoS (like a shield)
- **Security Groups** = Instance firewalls (guard each instance)

#### 🔍 **Monitoring & Detection**
- **CloudTrail** = **Trail** of breadcrumbs (audit logs)
- **Config** = **Configuration** monitoring
- **GuardDuty** = **Guard** on **Duty** (threat detection)
- **Inspector** = **Inspects** for vulnerabilities
- **Macie** = **M**achine learning for d**a**ta **c**lass**i**fication (**e**ncryption)

---

## ✅ Chapter Checklist

Before proceeding, ensure you can:

- [ ] Explain defense in depth strategy
- [ ] Choose appropriate encryption services (KMS vs CloudHSM)
- [ ] Understand network security layers (Security Groups, NACLs, WAF)
- [ ] Identify monitoring and logging requirements
- [ ] Select threat detection services for different scenarios
- [ ] Understand compliance and governance tools
- [ ] Design basic security architecture for different business sizes

---

## 🎯 Practice Questions

### Question 1
A company wants to encrypt data stored in S3 buckets using their own encryption keys that they fully control. Which AWS service should they use?

A) AWS KMS with AWS managed keys
B) AWS KMS with customer managed keys
C) AWS CloudHSM
D) AWS Certificate Manager

<details>
<summary>💡 Click for Answer</summary>

**Answer: C) AWS CloudHSM**

**Explanation:** CloudHSM provides dedicated hardware where customers have full control over their encryption keys. While KMS customer managed keys provide significant control, CloudHSM offers the highest level of customer control over encryption keys with dedicated, single-tenant hardware.
</details>

### Question 2
Which AWS service automatically monitors AWS accounts for malicious activity and unauthorized behavior using machine learning?

A) AWS Config
B) AWS CloudTrail
C) Amazon GuardDuty
D) Amazon Inspector

<details>
<summary>💡 Click for Answer</summary>

**Answer: C) Amazon GuardDuty**

**Explanation:** GuardDuty uses machine learning, anomaly detection, and integrated threat intelligence to identify threats like malicious IPs, malware, and compromised instances. It continuously monitors VPC Flow Logs, DNS logs, and CloudTrail events.
</details>

### Question 3
A web application needs protection against SQL injection and cross-site scripting attacks. Which AWS service provides this protection?

A) AWS Shield
B) AWS WAF
C) Security Groups
D) Network ACLs

<details>
<summary>💡 Click for Answer</summary>

**Answer: B) AWS WAF**

**Explanation:** AWS WAF (Web Application Firewall) protects web applications from common web exploits like SQL injection and cross-site scripting (XSS). Shield protects against DDoS attacks, while Security Groups and NACLs provide network-level protection.
</details>

---

## 🗺️ What's Next?

Now that you understand the comprehensive security services AWS provides, let's explore how to meet compliance requirements and implement governance frameworks.

**🎯 Next Chapter:** [Compliance & Governance](./compliance.md)

Learn how to navigate the complex world of regulatory compliance in the cloud!

---

**🎉 Fantastic progress!** You now understand the powerful security tools available in AWS and how to implement defense in depth strategies.

---

**← [Back to Domain 2 Overview](./README.md)**
