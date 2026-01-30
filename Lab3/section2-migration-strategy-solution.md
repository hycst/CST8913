
Migration Strategy Overview

I am planing to apply a progress migration approach is recommended to minimize risk and downtime:

Start with Lift-and-Shift (Rehosting) for critical workloads
Gradually rebuild application to service which runnong on cloud
Transfer data, file storeage, email service to cloud 


Component Migration:
Web Application → PaaS,  Use Rehost Strategy,  to Move monolithic application to VM on cloud
Database → PaaS, Use  Use Rehost Strategy,  migrate to Dababase (such as Oracle, or SQL Server on VM on CLoud)
File Storage → PaaS, Use Replace Strategy, migrate entire storege files to target storage on CLoud

Networking → Cloud-Native Networking
Router  → 	VPC / VNet
Firewall  → 	Security Groups / NSGs
Load Balancer →  Managed Load Balancer

Email Service → SaaS,Use Replace Strategy, migrate email server to server runnning on CLoud


Migration Plan

Step 1 – Assessment and Plan:
- Investige and clarify current applications and relationships among them (dependencies, and procedure)
- Investigge data sensitivity and compliance needs

Step 2 2 – Foundation
- Set up virtual network on cloud(VPC/VNet)
- Set up IAM ( in case of AWS), or RBAC( in case of Azure), resource grpup, user group, and security policies

Step 3: – Migration
- Backup all the data, and files
- Rehost web app to IaaS
- Migrate database to VM on cloud
- Transfer entire files storege to target storage server
- Set up email serveron SaaS, transfer email server to SaaS provider

Step 4: – Verification
- Re-Build  web app to PaaS
- Re-balance database to managed SQL
- Enable Service, monitoring performace and and set for autoscaling
