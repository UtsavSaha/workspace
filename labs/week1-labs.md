# Week 1 Hands-On Labs

## Lab 1: Create AWS Account & Set Up Billing Alerts

### Objective
Set up a secure AWS account with proper billing alerts to avoid unexpected charges.

### Steps

1. **Create AWS Account**
   - Visit aws.amazon.com
   - Click "Create AWS Account"
   - Provide email, password, account name
   - Add payment method
   - Verify phone number

2. **Enable MFA on Root Account**
   - Go to IAM console
   - Click "Users" → Click username (root)
   - Scroll to "Security credentials"
   - Enable MFA device
   - Use authenticator app (Google Authenticator, Authy)

3. **Set Up Billing Alerts**
   - Go to AWS Billing Console
   - Settings → Preferences
   - Check "Receive Free Tier Usage Alerts"
   - Save preferences
   - Go to CloudWatch
   - Alarms → Create alarm
   - Select "Estimated Charges"
   - Set threshold to $10
   - Create SNS notification

4. **Create IAM User for Daily Work**
   - IAM Console → Users → Create user
   - Username: `aws-learning`
   - Attach policy: `AdministratorAccess` (for learning only)
   - Create access key (if needed)
   - Download credentials CSV

### Verification
- [ ] Root account has MFA enabled
- [ ] Billing alert configured
- [ ] IAM user created and accessible
- [ ] Can access AWS console with IAM user

### Time: ~20 minutes

---

## Lab 2: Launch Your First EC2 Instance

### Objective
Launch an EC2 instance, connect to it (or understand how to), then terminate it properly.

### Prerequisites
- AWS account with IAM user created
- Understanding of security groups
- Familiar with EC2 dashboard

### Steps

1. **Navigate to EC2 Dashboard**
   - AWS Console → EC2
   - Ensure you're in correct region (e.g., us-east-1)

2. **Launch Instance**
   - Click "Launch Instances"
   - **Name:** `aws-learning-test`
   - **AMI:** Amazon Linux 2 (free tier eligible)
   - **Instance Type:** t2.micro (free tier)
   - **Key Pair:** Create new
     - Name: `aws-learning-keypair`
     - Type: RSA
     - Format: .pem (for Linux/Mac) or .ppk (for Windows PuTTY)
     - Save securely!
   - **Network:** Default VPC
   - **Subnet:** Default subnet
   - **Storage:** 30 GB gp2 (default)
   - **Security Group:** Create new
     - Name: `aws-learning-sg`
     - SSH access from your IP (0.0.0.0/0 only for learning!)
   - Click "Launch Instances"

3. **Monitor Instance Launch**
   - Instances page shows your instance
   - Wait for State = "Running"
   - Wait for Status checks = "2/2 passed"
   - Note the Public IP address

4. **Connect to Instance (Option A: Browser)**
   - Select instance → Connect tab
   - Choose EC2 Instance Connect
   - Click "Connect"
   - You'll get a browser terminal

5. **Connect to Instance (Option B: SSH - for practice)**
   - Windows: Use PuTTY with .ppk key
   - Mac/Linux: 
     ```bash
     chmod 400 aws-learning-keypair.pem
     ssh -i aws-learning-keypair.pem ec2-user@<PUBLIC_IP>
     ```
   - Command: `sudo yum update -y`

6. **Terminate Instance**
   - Back to EC2 Dashboard
   - Select your instance
   - Instance State → Terminate
   - Confirm termination
   - Wait for State = "Terminated"

### Key Concepts Observed
- [ ] Public IP address assignment
- [ ] Security groups control access
- [ ] Key pairs for authentication
- [ ] Instance state lifecycle
- [ ] Free tier eligibility (t2.micro, gp2 storage)

### Verification Checklist
- [ ] Instance launched successfully
- [ ] Could see it in running state
- [ ] Attempted connection (browser or SSH)
- [ ] Successfully terminated instance
- [ ] No instances left running

### Cleanup
- [ ] Terminate instance if still running
- [ ] Review Key Pairs (keep your key safe!)
- [ ] Delete security group if not needed
- [ ] Save key pair location for future reference

### Time: ~30-40 minutes

---

## Lab 3: Create IAM User and Security Group

### Objective
Practice creating IAM users with specific permissions and understand security groups.

### Steps

1. **Create IAM User**
   - IAM Console → Users → Create user
   - User name: `developer-user`
   - Uncheck "Provide user access to AWS Management Console" (for now)
   - Click Next
   - **Attach Permissions:** Search for `EC2FullAccess`
   - Select `AmazonEC2FullAccess`
   - Click Next and Create

2. **Create IAM User with Console Access**
   - Create user: `learning-admin`
   - CHECK "Provide user access to AWS Management Console"
   - Custom password: Create one
   - UNCHECK "Users must create new password on sign-in"
   - Attach policy: `AdministratorAccess`
   - Create and download credentials

3. **Create Security Group**
   - EC2 → Security Groups → Create Security Group
   - Name: `web-access-sg`
   - Description: "Allow web traffic and SSH"
   - **Inbound Rules:**
     - Rule 1: SSH | TCP | 22 | Your IP
     - Rule 2: HTTP | TCP | 80 | 0.0.0.0/0
     - Rule 3: HTTPS | TCP | 443 | 0.0.0.0/0
   - **Outbound Rules:** Allow all (default)

4. **Review IAM Policies**
   - Go to IAM → Policies
   - Search: `EC2FullAccess`
   - View the JSON document
   - Note: Which permissions are granted?

### Concepts Verified
- [ ] Understand IAM user creation
- [ ] Know difference between permissions
- [ ] Security groups control traffic
- [ ] Understand inbound/outbound rules
- [ ] CIDR notation: 0.0.0.0/0, your-ip/32

### Verification
- [ ] Created 2 IAM users
- [ ] Can see their policies
- [ ] Created security group with rules
- [ ] Understand what each rule does

### Time: ~25-30 minutes

---

## Lab 4: Explore AWS Regions

### Objective
Understand AWS regions and practice changing regions in the console.

### Steps

1. **View All Regions**
   - Top right of AWS Console → Region dropdown
   - Explore list of 30+ regions
   - Note the naming convention: continent-direction-number

2. **Change Region**
   - Select a different region (e.g., `eu-west-1`)
   - Notice: EC2 instances, S3 buckets, other services are region-specific
   - Go back to original region

3. **Research Region Availability**
   - Visit: https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/
   - Check which regions have which services
   - Note: Not all services are in all regions

4. **Calculate Latency**
   - Find your physical location
   - Identify the closest AWS region
   - Note: Latency is usually 5-30ms from nearest region

### Concepts Learned
- [ ] AWS has 30+ regions worldwide
- [ ] Each region is independent
- [ ] Services vary by region
- [ ] Regions named: continent-direction-number
- [ ] Latency impacts performance

### Time: ~15 minutes

---

## Lab Summary

**Total Hands-On Lab Time:** ~2 hours (spread across week)

**What You've Accomplished:**
- ✅ Set up secure AWS account with billing alerts
- ✅ Launched and terminated EC2 instance
- ✅ Created IAM users and security groups
- ✅ Explored AWS regions and services
- ✅ Hands-on experience with AWS console

**Key Takeaways:**
1. Always use IAM users, not root account
2. Security groups control instance access
3. Key pairs are essential for EC2 access
4. AWS is global - choose regions strategically
5. Always terminate unused resources to save costs

---

## Troubleshooting Guide

### Issue: Can't connect to EC2 instance
**Solutions:**
- Check security group allows SSH (port 22)
- Verify key pair matches the instance
- Check instance has public IP
- Check your network allows outbound SSH

### Issue: Instance won't launch
**Solutions:**
- Check free tier eligibility (t2.micro)
- Verify account has payment method on file
- Check region has capacity
- Try a different region

### Issue: Can't find EC2 service
**Solutions:**
- Make sure you're logged in with correct account
- Check you're viewing correct region
- Service might not be available in your region

### Issue: IAM user can't do something
**Solutions:**
- Verify permissions are attached
- Check there are no Deny policies
- Verify resource-level permissions

---

**Great job completing Week 1 labs! You now have hands-on AWS experience. 🎉**
