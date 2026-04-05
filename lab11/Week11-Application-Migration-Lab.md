### Week11 – Application Migration Lab  
### Tailwind Traders – Azure Migration Strategy

---

### 1. Overview

Tailwind Traders is migrating a **3-tier on-premises application** to Microsoft Azure.

### Architecture Includes:
- **Web Tier:** WEB01, WEB02 (VMware)  
- **Application Tier:** APP01 (VMware)  
- **Database Tier:** SQL01 (Physical SQL Server 2017)  
- **Supporting Components:** LB01, backups, firewall rules  

### Migration Goals
- Meet **≤ 1-hour downtime requirement**  
- Improve **scalability and resilience**  
- Optimize **cost and performance**  
- Maintain **security and compliance**  

---

#### 2. Current Architecture (On-Premises)

```mermaid
flowchart LR
    Users --> LB01[Internal Load Balancer]
    LB01 --> WEB01
    LB01 --> WEB02
    WEB01 --> APP01
    WEB02 --> APP01
    APP01 --> SQL01[(SQL Server 2017)]
    SQL01 --> Backup[(Nightly Backup)]
