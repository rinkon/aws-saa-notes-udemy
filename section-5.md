##### Budget Alerts
- Spending threshold alert
- Monthly cost alert
- others

##### EC2 (Virtual Machines)
Mainly the combination of:
- EC2 - Elastic Computing Cloud
- EBS - Elastic Block Storwage
- ELB - Elastic Load Balancing
- ASG - Auto Scaling Group

##### EC2 onfig options:
1. OS
2. CPU
3. RAM
4. Storage
5. Network Card, IP
6. Security Group (Inbound, Outbound Rules)
7. Bootstrap Script (Startup Script): EC2 User Data

- User Data runs with root user
- Need Key pair for SSH login
- On restart, public IP may change, but private IP remains the same
- One user already setup in Amazon Linux named ec2-user

##### Naming
m5.2xlarge
m = Instance Class
5 = Generation (AWS improves them over time)
2xlarge = Size within the instance class

##### Instance Types
General Purpose 
Compute Optimized
Memory Optimized
Storage Optmized

reference: https://instances.vantage.sh/

##### Security group
- Defines the inbound and outbound rules for EC2 instance
- Many-to-Many relation between EC2 and Security group  
- Locked down to region / VPC
- Timeout is mostly security group issue
- connection refused mostly not security group issue
- By default all inbound blocked, all outbound authorised
- There are no explicit deny rules, only allow rules


##### SSH connection
change permission: ```chmod 0400 name.pem```
connect: ```ssh -i name.pem ec2-user@ip```

##### SSH Alternative: EC2 Instance Connect

Always use IAM Roles for EC2 instances. Never assign IAM Access Key ID or Secret Key in ec2.

##### EC2 Purchasing options
1. On demand: Highest Price
2. Reserved Instance: 1-3 years plan with around 70% discount. Commitment to specific instance type
3. EC2 Savings plan: 1-3 years plan with around 70% discount. Commitment to specific dollar amount
4. Spot Instances: upto 91% discount. for interruptible workloads. instance can be termintaed
5. Reserved Convertible: Reserved but with customisable intance. upto 66% discount
6. Dedicated Instance: dedicated hardware
7. Dedicated Host: dedicated hardware but full machine rent
8. Capacity Reservations: 