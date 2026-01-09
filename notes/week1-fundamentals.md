# Week 1: AWS Fundamentals & Core Services Introduction

## Overview
This week focuses on building a strong foundation in AWS basics. You'll learn about the AWS ecosystem, how to navigate the console, set up your first EC2 instance, and understand IAM fundamentals.

## Learning Objectives
By the end of this week, you should understand:
- ✅ AWS Global Infrastructure (Regions, AZs, Edge Locations)
- ✅ AWS Account Structure and IAM basics
- ✅ EC2 fundamentals and instance types
- ✅ How to navigate the AWS Management Console
- ✅ Basic AWS service categories

## Daily Breakdown

### Monday: AWS Account Setup & Console Navigation
**Duration:** 45 minutes
**Topics:** 
- Create AWS account and set up free tier
- Navigate the AWS Management Console
- Understand the AWS Console layout
- Learn about AWS service categories

**Key Resources:**
- Udemy: "Intro + Account Setup" section
- AWS Free Tier documentation

**Hands-On:**
- [ ] Create AWS account
- [ ] Set up billing alerts
- [ ] Explore the console dashboard
- [ ] Find and bookmark key services

**Notes:**
```
[Add your notes here]
```

---

### Tuesday: EC2 Basics - Instances & Types
**Duration:** 45 minutes
**Topics:**
- What is EC2 (Elastic Compute Cloud)
- Instance types and families
- T2, T3, M5 families overview
- Use cases for different instance types

**Key Resources:**
- Udemy: EC2 Section 1
- AWS EC2 Instance Types documentation

**Hands-On:**
- [ ] Review EC2 pricing calculator
- [ ] Understand instance naming convention
- [ ] Review instance type comparison

**Notes:**
```
[Add your notes here]
```

---

### Wednesday: Regions, Availability Zones & Edge Locations
**Duration:** 45 minutes
**Topics:**
- AWS Global Infrastructure components
- Regions and Availability Zones
- Edge Locations and CloudFront
- Disaster Recovery basics

**Key Resources:**
- Udemy: "Global Infra" section
- AWS Global Infrastructure map

**Hands-On:**
- [ ] Explore AWS regions on console
- [ ] Identify nearest region to you
- [ ] Research typical region selection criteria

**Notes:**
```
[Add your notes here]
```

---

### Thursday: IAM Fundamentals - Users, Groups, Roles
**Duration:** 45 minutes
**Topics:**
- Identity and Access Management (IAM)
- Users, Groups, and Roles
- IAM Policies and Permissions
- Root account vs. IAM users
- Security best practices

**Key Resources:**
- Udemy: IAM Section 1
- AWS IAM Best Practices

**Hands-On:**
- [ ] Create IAM user in your account
- [ ] Create IAM group
- [ ] Assign basic permissions
- [ ] Generate access keys (understand security implications)

**Notes:**
```
[Add your notes here]
```

---

### Friday: Hands-On Practice - Create EC2 Instance & IAM User
**Duration:** 45 minutes
**Topics:**
- Hands-on lab combining week's learning
- Practical application of EC2 and IAM
- Practice questions

**Hands-On Labs:**
- [ ] **Lab 1: Create IAM User**
  - Create a new IAM user with EC2 full access
  - Generate access keys
  - Document steps taken
  
- [ ] **Lab 2: Launch EC2 Instance**
  - Launch a t2.micro instance (free tier eligible)
  - Use the IAM user you created
  - Connect to the instance (or practice SSH commands)
  - Terminate the instance after

**Documentation:**
- [ ] Screenshot the IAM console showing your new user
- [ ] Document the EC2 launch process
- [ ] Note any errors encountered and how you resolved them

---

### Saturday: Deep Dive - EC2 Instance Types & Use Cases
**Duration:** 2 hours
**Topics:**
- Detailed EC2 instance family breakdown
- T2 vs T3 vs M5 vs C5 instances
- Use cases and pricing considerations
- Reserved instances vs. On-Demand

**Study Plan:**
1. **60 mins:** Watch Udemy EC2 Deep Dive section
2. **45 mins:** Create comparison chart of instance types
3. **15 mins:** Review practice questions

**Hands-On:**
- [ ] Compare pricing of different instance types
- [ ] Create a spreadsheet: Instance Type | vCPU | Memory | Use Case | Price

**Practice Questions:**
- Complete practice questions from course
- Target: 70%+ accuracy

**Notes:**
```
[Add your notes here]
```

---

### Sunday: Review Week 1 + Quiz
**Duration:** 2 hours
**Topics:**
- Comprehensive review of all week 1 concepts
- Practice quiz
- Identify weak areas

**Study Plan:**
1. **45 mins:** Review all notes from the week
2. **60 mins:** Complete practice quiz (Udemy or custom)
3. **15 mins:** Review incorrect answers

**Review Checklist:**
- [ ] AWS Global Infrastructure - can you name 3 regions?
- [ ] IAM - understand user vs. role differences
- [ ] EC2 - identify appropriate instance types for scenarios
- [ ] Console navigation - comfortable finding services

**Quiz Target:** 60%+ accuracy

**Weak Areas to Focus Next Week:**
```
List any topics you struggled with:
1. 
2. 
3. 
```

---

## Week 1 Objectives Checklist

**Understanding:**
- [ ] Understand AWS account structure
- [ ] Know the global infrastructure (regions, AZs, edges)
- [ ] Understand IAM basic concepts
- [ ] Know EC2 fundamentals
- [ ] Comfortable navigating AWS Console

**Hands-On Skills:**
- [ ] Can create IAM user
- [ ] Can launch EC2 instance
- [ ] Can select appropriate region
- [ ] Can set up basic security groups (basic)

**Knowledge:**
- [ ] Can differentiate instance types
- [ ] Understand EC2 pricing models
- [ ] Know when to use different regions
- [ ] Understand IAM security best practices

---

## Key Concepts Summary

### AWS Regions
- **What:** Geographic areas with multiple AZs
- **When to Use:** Disaster recovery, compliance, latency
- **Current Regions:** 30+ globally

### Availability Zones
- **What:** Physical data centers within a region
- **When to Use:** High availability architecture
- **Typical:** 2-4 AZs per region

### EC2 Instance Types
| Type | Use Case | Example |
|------|----------|---------|
| T2/T3 | General, burstable | Web servers, small apps |
| M5 | General purpose | Medium apps, balanced |
| C5 | Compute optimized | High traffic, batch |
| R5 | Memory optimized | Databases, caching |

### IAM Key Points
- **Always use IAM users** (never root for daily work)
- **Principle of least privilege**
- **Use roles for EC2** (not access keys stored on instance)
- **Enable MFA** for important accounts

---

## Resources for Week 1

**Course Sections:**
- [ ] Udemy: Course Introduction
- [ ] Udemy: AWS Account Setup
- [ ] Udemy: EC2 Introduction
- [ ] Udemy: IAM Basics
- [ ] Udemy: Global Infrastructure

**AWS Documentation:**
- [AWS Global Infrastructure](https://aws.amazon.com/about-aws/global-infrastructure/)
- [EC2 Documentation](https://docs.aws.amazon.com/ec2/)
- [IAM Documentation](https://docs.aws.amazon.com/iam/)

**Reference Materials:**
- [AWS Services by Region](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/)
- [EC2 Instance Types](https://aws.amazon.com/ec2/instance-types/)

---

## Common Mistakes to Avoid

❌ Using root account for daily work  
✅ Always use IAM users

❌ Storing access keys on EC2 instances  
✅ Use IAM roles for instances

❌ Choosing region randomly  
✅ Choose based on latency, compliance, costs

❌ Forgetting to terminate test instances  
✅ Always clean up after labs (costs!)

---

## Week 1 Progress Tracker

| Item | Status | Notes |
|------|--------|-------|
| Monday lesson | ⏳ | - |
| Tuesday lesson | ⏳ | - |
| Wednesday lesson | ⏳ | - |
| Thursday lesson | ⏳ | - |
| Friday lab | ⏳ | - |
| Saturday deep dive | ⏳ | - |
| Sunday review + quiz | ⏳ | - |
| Quiz Score | - | Target: 60%+ |

---

## Next Week Preview

Week 2 will cover **Storage & Databases**, including:
- S3 (Simple Storage Service) - object storage
- EBS (Elastic Block Store) - block storage
- RDS (Relational Database Service)
- DynamoDB (NoSQL database)

**Start thinking about:** What's the difference between object and block storage?

---

**Good luck with Week 1! This foundation is crucial for everything ahead. 💪**
