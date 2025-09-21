# Day 2: AWS Global Infrastructure - Think Like a Global Architect! 🌍

## 🎯 Today's Mission
Master AWS's global infrastructure and understand how to design resilient, high-performance applications across multiple regions and availability zones.

## ⏰ Time Allocation (2 hours total)
- **Theory & Videos**: 75 minutes
- **Hands-on Practice**: 30 minutes  
- **Quiz & Review**: 15 minutes

---

## 📘 LEARNING RESOURCES

### 🎥 Primary Video Content (60 minutes)
1. **AWS Skill Builder - AWS Cloud Practitioner Essentials**
   - [Module 3: Global Infrastructure and Reliability](https://explore.skillbuilder.aws/learn/course/134) (FREE)
   - Duration: 45 minutes

2. **AWS Global Infrastructure Deep Dive**
   - [AWS Global Infrastructure Overview](https://aws.amazon.com/about-aws/global-infrastructure/) (READ - 15 min)
   - [AWS Regions and Availability Zones](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html) (READ)

### 📚 Essential Reading (15 minutes)
- [AWS Well-Architected Framework - Reliability Pillar](https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/welcome.html)
- [Disaster Recovery Strategies](https://aws.amazon.com/disaster-recovery/)

---

## 💻 HANDS-ON EXERCISES

### Exercise 1: Region and AZ Exploration (10 minutes)
1. Log into AWS Educate console
2. **Region Switching Exercise**:
   - Start in US East (N. Virginia) - us-east-1
   - Switch to Europe (Ireland) - eu-west-1
   - Switch to Asia Pacific (Tokyo) - ap-northeast-1
   - Switch to South America (São Paulo) - sa-east-1
3. **Document**: Note the services available in each region
4. **Observe**: How the console URL changes with regions

### Exercise 2: EC2 Multi-AZ Deployment (15 minutes)
1. **Launch EC2 instances in different AZs**:
   - Instance 1: us-east-1a (t2.micro)
   - Instance 2: us-east-1b (t2.micro)
   - Instance 3: us-east-1c (t2.micro)
2. **Compare**:
   - Instance IDs
   - Private IP addresses
   - Subnet assignments
3. **Terminate all instances** (avoid charges)

### Exercise 3: Global Latency Test (5 minutes)
1. Use [AWS Regional Services List](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/)
2. **Identify**: Which services are global vs regional
3. **Plan**: If serving users in Japan, Europe, and USA - which regions would you choose?

---

## 🧠 KNOWLEDGE CHECK EXERCISES

### Exercise 4: Disaster Recovery Planning
**Scenario**: You're designing a critical e-commerce application for a global retailer.

**Your Analysis**:
```
Primary Region: _______________
Secondary Region: _______________
Justification: _______________

Multi-AZ Strategy:
- Database: _______________
- Web servers: _______________
- Load balancers: _______________

RTO (Recovery Time Objective): _______________
RPO (Recovery Point Objective): _______________
```

### Exercise 5: Global Architecture Design
**Scenario**: Netflix-style video streaming service for global audience.

**Your Design**:
```
Content Delivery Strategy:
- Primary regions: _______________
- Edge locations role: _______________
- Content caching strategy: _______________

User Experience Optimization:
- Latency reduction: _______________
- Failover strategy: _______________
- Data replication: _______________
```

---

## 🌐 REAL-WORLD APPLICATION SCENARIOS

### Scenario 1: Financial Services Company
**Requirements**: 
- Serve customers in US, Europe, Asia
- 99.99% uptime requirement
- Data sovereignty compliance
- Sub-100ms latency

**Your Architecture**:
```
Regional Strategy: _______________
Compliance Considerations: _______________
High Availability Design: _______________
Latency Optimization: _______________
```

### Scenario 2: Gaming Company
**Requirements**:
- Real-time multiplayer gaming
- Global player base
- Seasonal traffic spikes (holidays)
- Low latency critical

**Your Architecture**:
```
Region Selection: _______________
Auto-scaling Strategy: _______________
Edge Computing: _______________
Traffic Management: _______________
```

---

## ❓ MASTERY QUIZ - Answer ALL Before Proceeding to Day 3

### Section A: Infrastructure Fundamentals (Must get 4/5 correct)

1. **What's the minimum number of Availability Zones in an AWS Region?** Explain why this number matters for high availability.

2. **Difference between Region, AZ, and Edge Location**: Define each and give an example of when you'd use the concept in architecture decisions.

3. **Data Sovereignty**: A European company must keep customer data in Europe. How does AWS global infrastructure support this requirement?

4. **Latency vs Availability**: You can choose between a single region with 3 AZs or 2 regions with 2 AZs each. For a real-time trading application, which would you choose and why?

5. **Edge Locations**: How do CloudFront edge locations improve performance? Give a specific example with a global e-commerce site.

### Section B: Architectural Thinking (Must get 3/4 correct)

6. **Multi-AZ vs Multi-Region**: When would you use each strategy? Give specific use cases for both.

7. **Disaster Recovery**: Explain the difference between backup/restore, pilot light, warm standby, and multi-site DR strategies.

8. **Global Load Balancing**: How would you route traffic for users in Tokyo, London, and New York to provide the best experience?

9. **Compliance and Regions**: A healthcare company needs HIPAA compliance. How does region selection impact their compliance strategy?

### Section C: Practical Application (Must get 2/2 correct)

10. **Cost vs Performance**: Deploying in multiple regions increases costs but improves performance. How would you make this trade-off decision?

11. **Service Availability**: Not all AWS services are available in all regions. How would this impact your architecture decisions for a global application?

---

## 🎯 MASTERY CHECKPOINTS

### ✅ Infrastructure Knowledge
- [ ] Understand the hierarchy: Region → AZ → Data Center
- [ ] Can explain the purpose of each infrastructure component
- [ ] Know how to check service availability by region
- [ ] Understand latency implications of geographic distance

### ✅ Architectural Thinking
- [ ] Can design multi-AZ deployments for high availability
- [ ] Understand when to use multi-region architectures
- [ ] Can plan disaster recovery strategies
- [ ] Consider compliance and data sovereignty requirements

### ✅ Practical Skills
- [ ] Can navigate between AWS regions in console
- [ ] Understand how to deploy resources across AZs
- [ ] Can evaluate trade-offs between cost, performance, and availability
- [ ] Know how to use AWS global infrastructure for optimization

---

## 🚨 COMPLETION REQUIREMENTS

**To unlock Day 3, you must:**

1. ✅ Complete ALL hands-on exercises with AWS Educate
2. ✅ Answer ALL 11 quiz questions correctly (minimum scores listed)
3. ✅ Submit screenshots of multi-AZ EC2 deployment
4. ✅ Design architecture for at least one real-world scenario
5. ✅ Pass mentor's spot-check questions on global infrastructure

---

## 🔥 BONUS CHALLENGES (Optional but Recommended)

1. **Research**: Look up the AWS regions closest to your location. What services are available there?

2. **Architecture Exercise**: Design a disaster recovery plan for a critical business application with specific RTO/RPO requirements.

3. **Cost Analysis**: Compare the costs of single-region vs multi-region deployment for a sample application.

---

## 📞 NEED HELP?

**Infrastructure concepts unclear?** Review the AWS Global Infrastructure whitepaper
**Can't access certain regions?** Some regions require special approval - focus on commonly available ones
**Confused about AZ naming?** Remember AZ names are account-specific (your 1a might be different from someone else's 1a)

---

**Master global thinking today. Tomorrow we dive into compute services! 🚀**
