# AWS Support Plans

## 🎯 Learning Objectives
By the end of this chapter, you will be able to:
- Compare and contrast AWS Support plan features and pricing
- Understand the appropriate use cases for each support plan
- Know response times and coverage for different support tiers
- Understand AWS Support services and tools available
- Make informed decisions about support plan selection

---

## 📖 Introduction

AWS Support is like having different levels of insurance for your car - from basic coverage to comprehensive protection with 24/7 roadside assistance. Each plan offers different levels of support, response times, and access to AWS experts.

### 🧠 Memory Aid: The BASIC-DEVELOPER-BUSINESS-ENTERPRISE Ladder
Each level builds upon the previous, adding more features, faster response times, and dedicated support.

---

## 🏢 AWS Support Plans Overview

### Support Plan Comparison

| Feature | Basic | Developer | Business | Enterprise On-Ramp | Enterprise |
|---------|-------|-----------|----------|-------------------|------------|
| **Price** | Free | $29+/month | $100+/month | $5,500+/month | $15,000+/month |
| **Use Case** | Learning | Development | Production | Large scale | Mission critical |
| **Response Time** | None | 12-24 hours | 1-24 hours | 30 min - 24 hours | 15 min - 24 hours |
| **Support Channels** | Documentation | Email | Email, Chat, Phone | Email, Chat, Phone | Email, Chat, Phone |

---

## 📋 Detailed Support Plans

### 1. Basic Support Plan

**Cost**: **FREE** with all AWS accounts

**What's Included**:
- ✅ **24/7 access** to customer service
- ✅ **Documentation and whitepapers**
- ✅ **AWS Trusted Advisor** (7 core checks)
- ✅ **AWS Personal Health Dashboard**
- ✅ **Support forums**

**What's NOT Included**:
- ❌ Technical support cases
- ❌ Phone or chat support
- ❌ Architecture guidance
- ❌ Best practice recommendations

**Best For**: 
- Learning AWS
- Personal projects
- Non-critical applications

**Analogy**: Like having a car with basic warranty - you get manuals and recall notices, but no roadside assistance.

### 2. Developer Support Plan

**Cost**: **$29/month** or 3% of monthly AWS usage (whichever is greater)

**Additional Features**:
- ✅ **Email support** during business hours
- ✅ **General architectural guidance**
- ✅ **Best practice recommendations**
- ✅ **Client-side diagnostic tools**

**Response Times**:
- **General guidance**: < 24 hours
- **System impaired**: < 12 hours

**Support Scope**:
- ✅ **1 primary contact** can open cases
- ✅ **Development environment** support

**Best For**:
- Individual developers
- Testing environments
- Early development stages

**Analogy**: Like having basic roadside assistance - help during business hours when you're stuck.

### 3. Business Support Plan

**Cost**: **$100/month** or 10% of monthly AWS usage for first $0-$10K, then 7% for $10K-$80K, then 5% for $80K-$250K, then 3% for $250K+ (whichever is greater)

**Additional Features**:
- ✅ **24/7 phone and chat support**
- ✅ **Full Trusted Advisor** (all checks)
- ✅ **API support** for Trusted Advisor and Health
- ✅ **Infrastructure Event Management** (additional fee)
- ✅ **Third-party software support**

**Response Times**:
- **General guidance**: < 24 hours
- **System impaired**: < 12 hours
- **Production system impaired**: < 4 hours
- **Production system down**: < 1 hour

**Support Scope**:
- ✅ **Unlimited contacts** can open cases
- ✅ **Production environment** support
- ✅ **Contextual architectural guidance**

**Best For**:
- Production workloads
- Business-critical applications
- Teams needing 24/7 support

**Analogy**: Like comprehensive car insurance with 24/7 roadside assistance and priority service.

### 4. Enterprise On-Ramp Support Plan

**Cost**: **$5,500/month** or 10% of monthly AWS usage (whichever is greater)

**Additional Features**:
- ✅ **Designated Technical Account Manager (TAM)** (shared)
- ✅ **Consultative review and guidance**
- ✅ **Infrastructure Event Management** (included)
- ✅ **Well-Architected reviews**
- ✅ **Operations reviews**

**Response Times**:
- **General guidance**: < 24 hours
- ✅ **System impaired**: < 12 hours
- ✅ **Production system impaired**: < 4 hours
- ✅ **Production system down**: < 1 hour
- ✅ **Business-critical system down**: < 30 minutes

**Support Scope**:
- ✅ Everything from Business plan
- ✅ **Proactive guidance** from TAM
- ✅ **Pool of Technical Account Managers**

**Best For**:
- Growing enterprises
- Organizations scaling AWS usage
- Companies needing proactive guidance

### 5. Enterprise Support Plan

**Cost**: **$15,000/month** or 10% of monthly AWS usage for first $0-$150K, then 7% for $150K-$500K, then 5% for $500K-$1M, then 3% for $1M+ (whichever is greater)

**Additional Features**:
- ✅ **Dedicated Technical Account Manager (TAM)**
- ✅ **Support API** access
- ✅ **White-glove case routing**
- ✅ **Management business reviews**
- ✅ **Training and workshops**

**Response Times**:
- **General guidance**: < 24 hours
- **System impaired**: < 12 hours
- **Production system impaired**: < 4 hours
- **Production system down**: < 1 hour
- **Business-critical system down**: < 15 minutes

**Support Scope**:
- ✅ Everything from Enterprise On-Ramp
- ✅ **Dedicated TAM** for your account
- ✅ **Proactive monitoring** and guidance
- ✅ **Executive-level relationships**

**Best For**:
- Large enterprises
- Mission-critical workloads
- Organizations with complex AWS environments

**Analogy**: Like having a personal mechanic on speed dial who knows your car inside and out.

---

## 🛠️ AWS Support Services and Tools

### 1. AWS Trusted Advisor

**Basic/Developer Plans** (7 Core Checks):
- ✅ Security Groups - Specific Ports Unrestricted
- ✅ Amazon S3 Bucket Permissions
- ✅ Amazon EBS Public Snapshots
- ✅ Amazon RDS Public Snapshots
- ✅ IAM Use
- ✅ MFA on Root Account
- ✅ Service Limits

**Business/Enterprise Plans** (Full Suite):
- ✅ **Cost Optimization**: 50+ checks
- ✅ **Performance**: 40+ checks
- ✅ **Security**: 60+ checks
- ✅ **Fault Tolerance**: 10+ checks
- ✅ **Service Limits**: 100+ checks

### 2. AWS Personal Health Dashboard

**Available to**: All support plans

**Features**:
- ✅ **Personalized view** of AWS service health
- ✅ **Proactive notifications** of planned activities
- ✅ **Real-time status** of your resources
- ✅ **Guided remediation** steps

### 3. AWS Support API

**Available to**: Business, Enterprise On-Ramp, Enterprise

**Capabilities**:
- ✅ **Create and manage** support cases programmatically
- ✅ **Retrieve Trusted Advisor** results
- ✅ **Access support case history**
- ✅ **Integrate with third-party tools**

### 4. Technical Account Manager (TAM)

**Available to**: Enterprise On-Ramp (shared), Enterprise (dedicated)

**Services Provided**:
- ✅ **Proactive guidance** and best practices
- ✅ **Architecture reviews** and recommendations
- ✅ **Operational support** and optimization
- ✅ **Advocacy within AWS** for your needs
- ✅ **Training and workshops**

---

## 📋 Real-World Scenarios

### Scenario 1: Startup Learning AWS
**Situation**: Small team exploring AWS for first application
**Recommended Plan**: **Basic Support**
**Reasoning**: 
- Cost-sensitive environment
- Learning and experimentation phase
- Non-critical applications
- Documentation and forums sufficient

### Scenario 2: Development Team
**Situation**: Development team building applications
**Recommended Plan**: **Developer Support**
**Reasoning**:
- Need email support for technical questions
- Architectural guidance during development
- Business hours support sufficient
- 1 primary contact adequate

### Scenario 3: Production E-commerce Site
**Situation**: Online store with business-critical operations
**Recommended Plan**: **Business Support**
**Reasoning**:
- 24/7 operations require round-the-clock support
- Production system downtime costs money
- Need < 1 hour response for critical issues
- Multiple team members need support access

### Scenario 4: Large Enterprise Migration
**Situation**: Fortune 500 company migrating to AWS
**Recommended Plan**: **Enterprise Support**
**Reasoning**:
- Mission-critical workloads
- Complex multi-account environment
- Need dedicated TAM for strategic guidance
- 15-minute response time for critical issues
- Proactive support and optimization

---

## 🎯 Decision Framework: Choosing Support Plans

### Step 1: Assess Your Needs

**Business Impact Questions**:
```
□ What's the cost of downtime per hour?
□ How critical are your AWS workloads?
□ Do you have internal AWS expertise?
□ What are your operating hours?
□ How many people need support access?
```

**Technical Complexity Questions**:
```
□ How complex is your AWS architecture?
□ Are you migrating existing workloads?
□ Do you need architectural guidance?
□ Are you using advanced AWS services?
□ Do you need compliance assistance?
```

### Step 2: Calculate Value

**Cost-Benefit Analysis**:
```
Downtime Cost = (Revenue per hour) × (Hours of downtime)
Support Cost = (Monthly support plan cost) × 12
Value = (Prevented downtime cost) - (Support cost)
```

**Example Calculation**:
- E-commerce site generates $10,000/hour
- Expected downtime without support: 8 hours/year
- Business Support cost: $3,000/year
- Value: ($10,000 × 8) - $3,000 = $77,000 net benefit

### Step 3: Match Plan to Needs

```
Basic: Learning/Development only
Developer: Single developer, development environment
Business: Production workloads, 24/7 operations
Enterprise On-Ramp: Growing enterprise, scaling usage
Enterprise: Mission-critical, complex environments
```

---

## 🧠 Memory Aids

### Support Plan Mnemonics

**BDBE Progression**:
- **B**asic: **B**eginners and learners
- **D**eveloper: **D**evelopment environments
- **B**usiness: **B**usiness-critical production
- **E**nterprise: **E**verything you need

**Response Time Ladder**:
```
Basic: No response (just docs)
Developer: 12-24 hours
Business: 1-24 hours (1 hour for critical)
Enterprise On-Ramp: 30 minutes for critical
Enterprise: 15 minutes for critical
```

### Quick Reference: What's Included

| Feature | Basic | Dev | Biz | Ent |
|---------|-------|-----|-----|-----|
| Documentation | ✅ | ✅ | ✅ | ✅ |
| Email Support | ❌ | ✅ | ✅ | ✅ |
| Phone/Chat | ❌ | ❌ | ✅ | ✅ |
| Full Trusted Advisor | ❌ | ❌ | ✅ | ✅ |
| TAM | ❌ | ❌ | ❌ | ✅ |

---

## 🔍 Best Practices for Support

### Maximizing Support Value

1. **Use the right channel**:
   - Documentation first for common questions
   - Support cases for specific technical issues
   - TAM for strategic guidance (if available)

2. **Provide complete information**:
   - Account ID and region
   - Detailed problem description
   - Steps already taken
   - Business impact

3. **Leverage all included services**:
   - Regularly review Trusted Advisor
   - Monitor Personal Health Dashboard
   - Use support case history for trends

4. **Build relationships**:
   - Regular communication with TAM
   - Participate in AWS events
   - Provide feedback to AWS

### Common Support Mistakes

❌ **Don't do this**:
- Choose plan based only on price
- Ignore Trusted Advisor recommendations
- Wait until crisis to engage support
- Provide incomplete problem descriptions

✅ **Do this instead**:
- Evaluate based on business impact
- Proactively address recommendations
- Build relationship before you need help
- Provide detailed, actionable information

---

## 📊 Support Plan Comparison Chart

```
Cost →        Free     $29+      $100+     $5,500+   $15,000+
             Basic   Developer  Business  Ent O-R   Enterprise
              │         │         │         │         │
Learning ─────┤         │         │         │         │
Development ──┼─────────┤         │         │         │
Production ───┼─────────┼─────────┤         │         │
Enterprise ───┼─────────┼─────────┼─────────┤         │
Mission Critical ──────┼─────────┼─────────┼─────────┤

Response Time:
Basic: No tech support
Developer: 12-24 hours
Business: 1-24 hours (1 hour critical)
Enterprise O-R: 30 min - 24 hours
Enterprise: 15 min - 24 hours
```

---

## 🎓 Practice Questions

### Question 1
**A company has a development environment where they're learning AWS. They occasionally need basic architectural guidance. Which support plan is most appropriate?**

A) Basic Support
B) Developer Support
C) Business Support
D) Enterprise Support

<details>
<summary>Click to reveal answer</summary>

**Answer: B**

**Explanation**: Developer Support is designed for development environments and provides email support with architectural guidance during business hours. Basic Support doesn't include technical support, while Business and Enterprise are overkill and expensive for a development environment.
</details>

### Question 2
**Which AWS Support plan provides access to ALL Trusted Advisor checks?**

A) Basic and above
B) Developer and above
C) Business and above
D) Enterprise only

<details>
<summary>Click to reveal answer</summary>

**Answer: C**

**Explanation**: Business Support and above (Business, Enterprise On-Ramp, Enterprise) provide access to the full suite of Trusted Advisor checks. Basic and Developer Support only include the 7 core security-focused checks.
</details>

### Question 3
**A company needs 24/7 support for their production environment with a maximum response time of 1 hour for critical issues. What is the minimum support plan they need?**

A) Developer Support
B) Business Support
C) Enterprise On-Ramp Support
D) Enterprise Support

<details>
<summary>Click to reveal answer</summary>

**Answer: B**

**Explanation**: Business Support provides 24/7 phone and chat support with < 1 hour response time for production system down scenarios. Developer Support only offers email support during business hours, while Enterprise plans offer faster response times but aren't required for this scenario.
</details>

### Question 4
**What is included with a dedicated Technical Account Manager (TAM)?**

A) Available with Business Support and above
B) Available with Enterprise On-Ramp (shared) and Enterprise (dedicated)
C) Available only with Enterprise Support
D) Available as an add-on to any support plan

<details>
<summary>Click to reveal answer</summary>

**Answer: B**

**Explanation**: Technical Account Managers are available with Enterprise On-Ramp Support (shared TAM) and Enterprise Support (dedicated TAM). Business Support and below do not include TAM services.
</details>

### Question 5
**Which support plan is most cost-effective for a startup running non-critical applications while learning AWS?**

A) Basic Support
B) Developer Support
C) Business Support
D) Enterprise Support

<details>
<summary>Click to reveal answer</summary>

**Answer: A**

**Explanation**: Basic Support is free and includes documentation, forums, and basic Trusted Advisor checks, which is sufficient for non-critical applications and learning scenarios. Developer Support and above include paid technical support that isn't necessary for non-critical learning environments.
</details>

---

## 🎯 Key Takeaways

1. **Support plans scale with business needs** - From free learning resources to dedicated enterprise support
2. **Response times matter** - Consider your tolerance for downtime when choosing plans
3. **Cost vs. value analysis** - Calculate the cost of downtime vs. support plan costs
4. **Trusted Advisor value increases** - Full suite only available with Business+ plans
5. **TAM provides strategic value** - Proactive guidance and relationship management
6. **24/7 support starts at Business** - Developer plan only offers business hours email support
7. **Multiple contacts need Business+** - Developer plan limited to one primary contact
8. **Support APIs enable automation** - Available with Business+ plans

### When to Upgrade Support Plans

**From Basic to Developer**:
- When you need technical guidance during development
- When documentation isn't sufficient
- When you have specific architectural questions

**From Developer to Business**:
- When you have production workloads
- When you need 24/7 support
- When downtime has business impact
- When multiple team members need support access

**From Business to Enterprise**:
- When you have mission-critical workloads
- When you need proactive guidance
- When you have complex, large-scale environments
- When 15-minute response time is required

---

## 📚 Next Steps
- Assess your current AWS environment and support needs
- Calculate the business impact of potential downtime
- Review your current support plan utilization
- Consider upgrading based on business growth and criticality

---

*🏠 [Back to Domain 4 Overview](README.md) | ⬅️ [Previous: Cost Optimization](cost-optimization.md) | 🎓 [Main Resource Hub](../README.md)*
