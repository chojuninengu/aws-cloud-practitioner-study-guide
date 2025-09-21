U# Day 2 Quick Reference Sheet 📋

## 🔗 Essential Links (Bookmark These!)

### Primary Learning Resources
- [AWS Global Infrastructure Overview](https://aws.amazon.com/about-aws/global-infrastructure/)
- [AWS Skill Builder Module 3](https://explore.skillbuilder.aws/learn/course/134) - Global Infrastructure
- [AWS Regions and AZs Documentation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html)
- [AWS Well-Architected Reliability Pillar](https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/welcome.html)

### Day 2 Specific Resources
- [AWS Regional Services List](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/)
- [AWS Disaster Recovery Strategies](https://aws.amazon.com/disaster-recovery/)
- [CloudFront Edge Locations](https://aws.amazon.com/cloudfront/features/)
- [AWS Compliance Programs](https://aws.amazon.com/compliance/programs/)

### Tools You'll Use Today
- [AWS Console Region Selector](https://console.aws.amazon.com/)
- [AWS Service Health Dashboard](https://status.aws.amazon.com/)
- [AWS Personal Health Dashboard](https://phd.aws.amazon.com/)

---

## 📝 Key Concepts Cheat Sheet

### AWS Global Infrastructure Hierarchy
1. **Regions** (24+ worldwide)
   - Geographic locations with multiple AZs
   - Minimum 3 AZs per region
   - Isolated from other regions
   
2. **Availability Zones (AZs)** (80+ worldwide)
   - One or more data centers
   - Redundant power, networking, connectivity
   - Low-latency links between AZs in same region
   
3. **Edge Locations** (400+ worldwide)
   - Content delivery network (CDN) endpoints
   - Cache content closer to users
   - Used by CloudFront and Route 53

### Region Selection Criteria
- **Latency**: Proximity to users
- **Compliance**: Data sovereignty requirements
- **Service Availability**: Not all services in all regions
- **Cost**: Pricing varies by region

### Availability Zone Facts
- **Naming**: AZ names are account-specific (your 1a ≠ my 1a)
- **Minimum**: 3 AZs per region (some have 6+)
- **Distance**: 100km apart within region
- **Connectivity**: High bandwidth, low latency between AZs

---

## 🏗️ Architecture Patterns

### High Availability Patterns
1. **Multi-AZ Deployment**
   - Distribute resources across multiple AZs
   - Automatic failover capability
   - Example: RDS Multi-AZ, ELB across AZs

2. **Multi-Region Deployment**
   - Active-passive or active-active
   - Cross-region replication
   - Example: S3 Cross-Region Replication

### Disaster Recovery Strategies
1. **Backup and Restore** (RPO: hours, RTO: 24hrs)
2. **Pilot Light** (RPO: minutes, RTO: hours)
3. **Warm Standby** (RPO: minutes, RTO: minutes)
4. **Multi-Site Active-Active** (RPO: real-time, RTO: automatic)

---

## 🌍 Global Services vs Regional Services

### Global Services (Same everywhere)
- **IAM** - Identity and Access Management
- **Route 53** - DNS service
- **CloudFront** - Content Delivery Network
- **WAF** - Web Application Firewall

### Regional Services (Region-specific)
- **EC2** - Virtual servers
- **RDS** - Managed databases
- **VPC** - Virtual networks
- **S3** - Object storage (regional but globally accessible)

### AZ-Specific Services
- **EBS** - Block storage (tied to specific AZ)
- **Subnets** - Network segments within AZ

---

## ⚡ Quick Commands & Navigation

### Region Switching in Console
1. Click region dropdown (top-right)
2. Select desired region
3. Note: URL changes to include region
4. Bookmark frequently used regions

### Multi-AZ EC2 Launch
1. EC2 Console → Launch Instance
2. Choose AMI and instance type
3. **Configure Instance Details**
4. **Subnet**: Select specific AZ
5. Repeat for additional AZs

### Checking Service Availability
1. Go to [AWS Regional Services](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/)
2. Filter by region
3. Verify service availability before architecture decisions

---

## 🎯 Today's Success Metrics
- [ ] Can navigate between AWS regions confidently
- [ ] Understand the difference between Region, AZ, and Edge Location
- [ ] Can deploy resources across multiple AZs
- [ ] Know when to use multi-region vs multi-AZ strategies
- [ ] Understand disaster recovery trade-offs (RTO/RPO)
- [ ] Can design global architectures for different use cases
- [ ] Consider compliance and data sovereignty in designs

---

## 🚨 Common Beginner Mistakes to Avoid
1. **Confusing AZ names** - Remember they're account-specific
2. **Ignoring compliance** - Some data must stay in specific regions
3. **Over-engineering** - Not every app needs multi-region
4. **Under-engineering** - Critical apps need proper DR planning
5. **Ignoring costs** - Multi-region significantly increases expenses
6. **Forgetting edge locations** - CloudFront can dramatically improve performance

---

## 💡 Pro Tips for Day 2
- **Latency rule**: Every 1000 miles ≈ 10ms additional latency
- **AZ strategy**: Odd numbers (3, 5) prevent split-brain scenarios
- **Region pairs**: Some regions are paired for disaster recovery
- **Service launches**: New services typically launch in us-east-1 first
- **Cost optimization**: us-east-1 often has lowest pricing

---

## 🔍 Troubleshooting Guide

### "Service not available in this region"
- Check [Regional Services List](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/)
- Switch to supported region
- Consider alternative services

### "Cannot launch in this AZ"
- AZ might be at capacity
- Try different AZ in same region
- Check service limits

### "Cross-region access denied"
- Verify IAM permissions include target region
- Check resource-based policies
- Ensure compliance requirements are met
