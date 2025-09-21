# Day 2 Exercises Workbook 📝

## 🎯 Complete ALL exercises before moving to Day 3

---

## EXERCISE 1: AWS Region Exploration ⚡
**Time: 15 minutes**

### Step-by-Step Regional Discovery:
**Part A: Region Switching**
- [ ] Log into AWS Educate console
- [ ] Start in US East (N. Virginia) - us-east-1
- [ ] Switch to Europe (Ireland) - eu-west-1
- [ ] Switch to Asia Pacific (Tokyo) - ap-northeast-1
- [ ] Switch to South America (São Paulo) - sa-east-1

**Document your findings:**
```
US East (N. Virginia):
- Services available: _______________
- Console URL: _______________
- Notable features: _______________

Europe (Ireland):
- Services available: _______________
- Console URL: _______________
- Notable features: _______________

Asia Pacific (Tokyo):
- Services available: _______________
- Console URL: _______________
- Notable features: _______________

South America (São Paulo):
- Services available: _______________
- Console URL: _______________
- Notable features: _______________
```

**Part B: Service Availability Analysis**
```
Services available in ALL regions tested:
1. _______________
2. _______________
3. _______________

Services NOT available in some regions:
1. _______________
2. _______________
3. _______________
```

---

## EXERCISE 2: Multi-AZ EC2 Deployment 💻
**Time: 20 minutes**

### Step-by-Step Multi-AZ Setup:
1. **Choose US East (N. Virginia) region**
2. **Launch 3 EC2 instances (t2.micro)**:
   - Instance 1: us-east-1a
   - Instance 2: us-east-1b  
   - Instance 3: us-east-1c

**Document each instance:**
```
Instance 1 (us-east-1a):
- Instance ID: _______________
- Private IP: _______________
- Subnet ID: _______________
- Launch time: _______________

Instance 2 (us-east-1b):
- Instance ID: _______________
- Private IP: _______________
- Subnet ID: _______________
- Launch time: _______________

Instance 3 (us-east-1c):
- Instance ID: _______________
- Private IP: _______________
- Subnet ID: _______________
- Launch time: _______________
```

**Analysis Questions:**
```
1. Are the private IP addresses in the same subnet range? _______________
2. Which AZ has the lowest alphabetical designation? _______________
3. If us-east-1a fails, which instances remain available? _______________
4. What's the benefit of this multi-AZ deployment? _______________
```

**⚠️ CRITICAL: Terminate all instances after documentation to avoid charges**

---

## EXERCISE 3: Global Latency Analysis 🌍
**Time: 10 minutes**

### Latency Planning Exercise:
**Scenario**: You're serving users in these locations:
- Tokyo, Japan
- London, UK  
- New York, USA
- Sydney, Australia

**Your Analysis:**
```
Optimal AWS Regions for each location:
Tokyo users: _______________
London users: _______________
New York users: _______________
Sydney users: _______________

Justification for each choice:
Tokyo: _______________
London: _______________
New York: _______________
Sydney: _______________

If you could only choose 2 regions total:
Primary: _______________
Secondary: _______________
Reasoning: _______________
```

---

## EXERCISE 4: Disaster Recovery Planning 🚨
**Time: 15 minutes**

### Scenario 1: E-commerce Platform
**Background**: Critical online store, 99.99% uptime requirement, global customers

**Your DR Strategy:**
```
Primary Region: _______________
Secondary Region: _______________
Distance between regions: _______________

RTO (Recovery Time Objective): _______________
RPO (Recovery Point Objective): _______________

Multi-AZ Components:
- Database strategy: _______________
- Web server strategy: _______________
- Load balancer strategy: _______________

Failover trigger conditions:
1. _______________
2. _______________
3. _______________
```

### Scenario 2: Financial Trading System
**Background**: Real-time trading, sub-second latency critical, regulatory compliance

**Your DR Strategy:**
```
Primary Region: _______________
Secondary Region: _______________
Compliance considerations: _______________

High Availability Design:
- Database: _______________
- Application servers: _______________
- Network: _______________

Latency optimization:
1. _______________
2. _______________
3. _______________
```

---

## EXERCISE 5: Global Architecture Design 🏗️
**Time: 20 minutes**

### Netflix-Style Streaming Service
**Requirements**:
- Global user base (North America, Europe, Asia)
- Video content delivery
- User authentication and profiles
- Recommendation engine
- 4K video streaming capability

**Your Global Architecture:**
```
Content Delivery Strategy:
Primary regions for content storage:
1. _______________
2. _______________
3. _______________

Edge locations strategy:
- Purpose: _______________
- Content caching: _______________
- Geographic distribution: _______________

User Experience Optimization:
- Authentication region strategy: _______________
- Profile data storage: _______________
- Recommendation engine placement: _______________

Bandwidth and Performance:
- 4K video delivery strategy: _______________
- Peak traffic handling: _______________
- Failover for video streams: _______________
```

**Cost vs Performance Trade-offs:**
```
High-cost, high-performance approach:
_______________

Medium-cost, balanced approach:
_______________

Low-cost, acceptable performance approach:
_______________

Your recommended approach and why:
_______________
```

---

## EXERCISE 6: Compliance and Data Sovereignty 📋
**Time: 10 minutes**

### Scenario Analysis:
**Company**: European healthcare provider
**Requirements**: GDPR compliance, patient data protection

**Your Compliance Strategy:**
```
Allowed regions for patient data:
1. _______________
2. _______________
3. _______________

Prohibited regions and why:
_______________

Data residency requirements:
- Patient records: _______________
- Backup data: _______________
- Analytics data: _______________

Cross-border data transfer considerations:
_______________

Audit and monitoring strategy:
_______________
```

---

## EXERCISE 7: Cost Optimization Analysis 💰
**Time: 15 minutes**

### Multi-Region Cost Comparison:
**Scenario**: Web application with database

**Single Region Deployment (us-east-1):**
```
Monthly costs estimate:
- EC2 instances (2x t3.medium): $_______________
- RDS database (db.t3.medium): $_______________
- Data transfer: $_______________
- Total monthly: $_______________
```

**Multi-Region Deployment (us-east-1 + eu-west-1):**
```
Monthly costs estimate:
- EC2 instances (4x t3.medium): $_______________
- RDS databases (2x db.t3.medium): $_______________
- Cross-region data transfer: $_______________
- Total monthly: $_______________

Additional cost for multi-region: $_______________
Percentage increase: _______________%
```

**Cost-Benefit Analysis:**
```
Benefits of multi-region:
1. _______________
2. _______________
3. _______________

When multi-region cost is justified:
_______________

When single region is sufficient:
_______________
```

---

## EXERCISE 8: Real-World Application 🌟
**Time: 10 minutes**

### Your Business Scenario:
**Choose ONE business type and design its global infrastructure:**

**Option A: Global Gaming Company**
```
Business requirements:
- Real-time multiplayer gaming
- Global tournaments
- Seasonal traffic spikes
- Anti-cheat systems

Your infrastructure design:
_______________
```

**Option B: International Banking**
```
Business requirements:
- 24/7 availability
- Regulatory compliance per country
- High security
- Real-time transactions

Your infrastructure design:
_______________
```

**Option C: Social Media Platform**
```
Business requirements:
- Billions of users
- Content moderation
- Real-time messaging
- Media storage and delivery

Your infrastructure design:
_______________
```

---

## 🎯 COMPLETION CHECKLIST

Before submitting to your mentor, ensure you have:

- [ ] Completed ALL 8 exercises
- [ ] Documented findings for region exploration
- [ ] Successfully deployed and terminated multi-AZ EC2 instances
- [ ] Designed disaster recovery strategies for 2 scenarios
- [ ] Created global architecture for streaming service
- [ ] Analyzed compliance requirements
- [ ] Calculated cost comparisons
- [ ] Applied concepts to real-world business scenario
- [ ] Taken screenshots of AWS console showing different regions

**Time to complete all exercises:** _____ minutes

**Ready for the Day 2 quiz? Only proceed if you completed EVERYTHING above!**
