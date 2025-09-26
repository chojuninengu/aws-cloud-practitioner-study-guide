# Day 2 Theory-Based Exercises (No AWS Account Required) 📚

## 🎯 Complete ALL exercises using theoretical knowledge and research

**Since you can't access EC2 instances, we'll focus on deep conceptual understanding and research-based learning.**

---

## EXERCISE 1: AWS Region Research & Analysis 🌍
**Time: 20 minutes**

### Part A: Global Region Mapping
**Research and document the following AWS regions:**

```
North America:
- US East (N. Virginia): us-east-1
  - Number of AZs: _______________
  - Key services launched here first: _______________
  - Why it's considered the "primary" region: _______________

- US West (Oregon): us-west-2
  - Number of AZs: _______________
  - Climate advantages: _______________
  - Cost comparison to us-east-1: _______________

Europe:
- Europe (Ireland): eu-west-1
  - Number of AZs: _______________
  - GDPR compliance features: _______________
  - Services available vs us-east-1: _______________

Asia Pacific:
- Asia Pacific (Tokyo): ap-northeast-1
  - Number of AZs: _______________
  - Latency to major Asian cities: _______________
  - Disaster recovery considerations: _______________
```

### Part B: Service Availability Analysis
**Research which services are available in each region:**

```
Services available in ALL regions:
1. _______________
2. _______________
3. _______________
4. _______________
5. _______________

Services only in select regions:
1. _______________
2. _______________
3. _______________

Services that launch in us-east-1 first:
1. _______________
2. _______________
3. _______________
```

---

## EXERCISE 2: Multi-AZ Architecture Design 🏗️
**Time: 25 minutes**

### Scenario: E-commerce Platform
**Design a multi-AZ architecture without actually deploying:**

```
Application Components:
- Web servers (front-end)
- Application servers (business logic)
- Database servers (data storage)
- Load balancers
- File storage

Your Multi-AZ Design:

AZ-1a (Primary):
- Components: _______________
- Rationale: _______________

AZ-1b (Secondary):
- Components: _______________
- Rationale: _______________

AZ-1c (Tertiary):
- Components: _______________
- Rationale: _______________

Cross-AZ Communication:
- How components communicate: _______________
- Network latency considerations: _______________
- Data synchronization strategy: _______________
```

### Failure Scenarios Analysis:
```
If AZ-1a fails completely:
- What happens to users: _______________
- Automatic failover process: _______________
- Recovery time estimate: _______________

If AZ-1a and AZ-1b both fail:
- Remaining capacity: _______________
- Performance impact: _______________
- Business continuity plan: _______________
```

---

## EXERCISE 3: Global Latency Calculation 📊
**Time: 15 minutes**

### Theoretical Latency Analysis
**Calculate approximate latencies based on geographic distance:**

```
Distance-Based Latency Rule: ~10ms per 1000 miles

User Locations and Optimal Regions:

Tokyo User:
- Distance to ap-northeast-1 (Tokyo): _____ miles = _____ ms
- Distance to us-west-2 (Oregon): _____ miles = _____ ms  
- Distance to eu-west-1 (Ireland): _____ miles = _____ ms
- Optimal region: _______________

London User:
- Distance to eu-west-1 (Ireland): _____ miles = _____ ms
- Distance to us-east-1 (Virginia): _____ miles = _____ ms
- Distance to ap-northeast-1 (Tokyo): _____ miles = _____ ms
- Optimal region: _______________

New York User:
- Distance to us-east-1 (Virginia): _____ miles = _____ ms
- Distance to us-west-2 (Oregon): _____ miles = _____ ms
- Distance to eu-west-1 (Ireland): _____ miles = _____ ms
- Optimal region: _______________
```

### Multi-Region Strategy:
```
If you could only choose 2 regions for global coverage:
Primary: _______________
Secondary: _______________

Reasoning:
_______________

Trade-offs accepted:
_______________
```

---

## EXERCISE 4: Disaster Recovery Planning 🚨
**Time: 20 minutes**

### Scenario 1: Financial Trading Platform
**Requirements**: 99.99% uptime, <1 second RTO, regulatory compliance

```
Your DR Strategy:

Primary Region: _______________
DR Region: _______________
Distance between regions: _______________

RTO (Recovery Time Objective): _______________
RPO (Recovery Point Objective): _______________

DR Architecture Type (choose one):
□ Backup and Restore (cheapest, slowest)
□ Pilot Light (minimal resources always running)
□ Warm Standby (scaled-down version always running)
□ Multi-Site Active-Active (most expensive, fastest)

Justification for choice: _______________

Data Replication Strategy:
- Real-time replication: _______________
- Batch replication: _______________
- Manual backup: _______________

Failover Triggers:
1. _______________
2. _______________
3. _______________
```

### Scenario 2: Social Media Platform
**Requirements**: Global users, content delivery, moderate downtime acceptable

```
Your DR Strategy:

Primary Regions (choose 2-3): _______________
DR Regions: _______________

Content Distribution:
- User data storage: _______________
- Media files (photos/videos): _______________
- Real-time messaging: _______________

Acceptable Downtime: _______________
Cost vs Availability Trade-off: _______________
```

---

## EXERCISE 5: Compliance & Data Sovereignty 📋
**Time: 15 minutes**

### Scenario: European Healthcare Company
**Requirements**: GDPR compliance, patient data protection

```
Compliance Analysis:

Allowed Regions for Patient Data:
1. _______________
2. _______________
3. _______________

Prohibited Regions and Why:
_______________

Data Residency Requirements:
- Patient medical records: _______________
- Backup and archive data: _______________
- Analytics and reporting: _______________
- Application logs: _______________

Cross-Border Data Transfer:
- When is it allowed: _______________
- What approvals needed: _______________
- Technical safeguards required: _______________

Audit Requirements:
- Data access logging: _______________
- Regular compliance checks: _______________
- Incident reporting: _______________
```

---

## EXERCISE 6: Edge Locations & CloudFront Strategy 🌐
**Time: 15 minutes**

### Global Content Delivery Design
**Scenario**: Video streaming service like Netflix

```
Content Distribution Strategy:

Origin Servers (where content is stored):
- Primary: _______________
- Secondary: _______________
- Tertiary: _______________

Edge Location Strategy:
- High-priority regions: _______________
- Medium-priority regions: _______________
- Low-priority regions: _______________

Content Caching Rules:
- Popular content (top 10%): _______________
- Regular content (next 40%): _______________
- Long-tail content (remaining 50%): _______________

Performance Optimization:
- 4K video delivery: _______________
- Mobile optimization: _______________
- Peak traffic handling: _______________

Cost Optimization:
- Cache hit ratio target: _______________
- Origin data transfer minimization: _______________
- Regional pricing considerations: _______________
```

---

## EXERCISE 7: Business Case Analysis 💼
**Time: 20 minutes**

### Multi-Region Cost-Benefit Analysis
**Scenario**: SaaS application with 100,000 users globally

```
Single Region Approach (us-east-1 only):
Pros:
1. _______________
2. _______________
3. _______________

Cons:
1. _______________
2. _______________
3. _______________

Estimated Monthly Cost: $_______________

Multi-Region Approach (us-east-1 + eu-west-1 + ap-northeast-1):
Pros:
1. _______________
2. _______________
3. _______________

Cons:
1. _______________
2. _______________
3. _______________

Estimated Monthly Cost: $_______________

Business Justification:
- Revenue at risk from downtime: $_______________
- Customer satisfaction impact: _______________
- Competitive advantage: _______________
- Regulatory requirements: _______________

Recommendation: _______________
```

---

## EXERCISE 8: Real-World Architecture Challenge 🎯
**Time: 25 minutes**

### Choose ONE scenario and design complete global architecture:

**Option A: Global Gaming Platform**
```
Requirements:
- Real-time multiplayer gaming
- 50 million players worldwide
- Tournament hosting capability
- Anti-cheat systems
- Seasonal traffic spikes (3x normal)

Your Architecture:
- Regions selected: _______________
- Game server distribution: _______________
- Player data storage: _______________
- Real-time communication: _______________
- Anti-cheat processing: _______________
- Tournament infrastructure: _______________
- Auto-scaling strategy: _______________
```

**Option B: International Banking Platform**
```
Requirements:
- 24/7 availability (99.99%)
- Multi-country regulatory compliance
- Real-time transaction processing
- Fraud detection
- Customer data protection

Your Architecture:
- Regions selected: _______________
- Transaction processing: _______________
- Customer data storage: _______________
- Fraud detection systems: _______________
- Compliance monitoring: _______________
- Disaster recovery: _______________
- Security architecture: _______________
```

**Option C: Global E-learning Platform**
```
Requirements:
- Video content delivery
- Interactive learning tools
- Student progress tracking
- Multi-language support
- Peak usage during school hours

Your Architecture:
- Regions selected: _______________
- Video content delivery: _______________
- Interactive tools hosting: _______________
- Student data storage: _______________
- Multi-language content: _______________
- Peak traffic handling: _______________
- Progress synchronization: _______________
```

---

## 🎯 COMPLETION CHECKLIST

Before submitting to your mentor, ensure you have:

- [ ] Researched and documented AWS regions and AZ information
- [ ] Designed multi-AZ architecture for e-commerce platform
- [ ] Calculated theoretical latencies for global users
- [ ] Created disaster recovery plans for 2 different scenarios
- [ ] Analyzed compliance requirements for healthcare data
- [ ] Designed content delivery strategy for video streaming
- [ ] Completed cost-benefit analysis for multi-region deployment
- [ ] Architected complete solution for chosen real-world scenario
- [ ] Used research and AWS documentation to support all answers
- [ ] Demonstrated understanding of trade-offs and business considerations

**Time to complete all exercises:** _____ minutes

**This theory-based approach will give you the same deep understanding as hands-on practice!**
