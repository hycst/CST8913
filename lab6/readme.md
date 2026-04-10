###  26W_CST8913_010 Cloud Migration

 

###  Lab 06: Cloud Resource Comparison Across AWS, Azure, and Google Cloud

###  Professor: Islam Gomaa

###  Student:  Hesheng Yang, 041094882

 

 

 

 

###  Contents

1) Cloud Resource Comparison Table (AWS vs Azure vs Google Cloud)

2) Big Similarities

3) Key Differences

4) Unique strengths

5) Naming convention patterns, for AWS, Azure and Google Cloud:

6) Reference

###  1) Cloud Resource Comparison Table (AWS vs Azure vs Google Cloud)

####  Core Compute & Storage
 
| #  | Description               | AWS        | Azure                  | Google Cloud    |
| -- | ------------------------- | ---------- | ---------------------- | --------------- |
| 1  | Scalable Virtual Machines | Amazon EC2 | Azure Virtual Machines | Compute Engine  |
| 2  | Object Storage            | Amazon S3  | Azure Blob Storage     | Cloud Storage   |
| 8  | Block Storage for VMs     | Amazon EBS | Azure Managed Disks    | Persistent Disk |
| 28 | Shared File Storage       | Amazon EFS | Azure Files            | Filestore       |


####  Databases

| #  | Description            | AWS             | Azure                          | Google Cloud    |
| -- | ---------------------- | --------------- | ------------------------------ | --------------- |
| 3  | Managed Relational DB  | Amazon RDS      | Azure SQL / MySQL / PostgreSQL | Cloud SQL       |
| 7  | NoSQL DB (Low latency) | Amazon DynamoDB | Azure Cosmos DB                | Cloud Firestore |
| 18 | Data Warehouse         | Amazon Redshift | Azure Synapse Analytics        | BigQuery        |

 
####  Compute & Serverless


| #  | Description          | AWS                   | Azure             | Google Cloud              |
| -- | -------------------- | --------------------- | ----------------- | ------------------------- |
| 4  | Serverless Functions | AWS Lambda            | Azure Functions   | Cloud Functions           |
| 11 | PaaS Deployment      | AWS Elastic Beanstalk | Azure App Service | App Engine                |
| 15 | Auto Scaling         | EC2 Auto Scaling      | VM Scale Sets     | Compute Engine Autoscaler |


####  Networking

| #  | Description     | AWS                   | Azure                  | Google Cloud         |
| -- | --------------- | --------------------- | ---------------------- | -------------------- |
| 5  | Private Network | Amazon VPC            | Azure VNet             | VPC                  |
| 6  | CDN             | Amazon CloudFront     | Azure Front Door / CDN | Cloud CDN            |
| 13 | DNS             | Amazon Route 53       | Azure DNS              | Cloud DNS            |
| 14 | Load Balancing  | Elastic Load Balancer | Azure Load Balancer    | Cloud Load Balancing |

####  Identity & Security

| #  | Description               | AWS       | Azure                | Google Cloud    |
| -- | ------------------------- | --------- | -------------------- | --------------- |
| 10 | Identity & Key Management | IAM + KMS | Entra ID + Key Vault | IAM + Cloud KMS |


####  Monitoring & DevOps

| #  | Description            | AWS            | Azure         | Google Cloud                   |
| -- | ---------------------- | -------------- | ------------- | ------------------------------ |
| 12 | Monitoring & Logging   | CloudWatch     | Azure Monitor | Cloud Monitoring + Logging     |
| 23 | Infrastructure as Code | CloudFormation | ARM / Bicep   | Deployment Manager / Terraform |
| 24 | CI/CD                  | CodePipeline   | Azure DevOps  | Cloud Build + Deploy           |

####  Integration & Messaging

| #  | Description            | AWS            | Azure              | Google Cloud      |
| -- | ---------------------- | -------------- | ------------------ | ----------------- |
| 16 | Message Queue          | Amazon SQS     | Azure Service Bus  | Pub/Sub           |
| 17 | Real-time Streaming    | Amazon Kinesis | Azure Event Hubs   | Pub/Sub           |
| 20 | Data Integration / ETL | AWS Glue       | Azure Data Factory | Cloud Data Fusion |
| 19 | Workflow Automation    | Step Functions | Logic Apps         | Cloud Workflows   |



####    Data Governance & AI


| #  | Description               | AWS                   | Azure             | Google Cloud |
| -- | ------------------------- | --------------------- | ----------------- | ------------ |
| 21 | Data Catalog & Governance | AWS Glue Data Catalog | Microsoft Purview | Dataplex     |
| 22 | AI / ML Services          | SageMaker             | Azure AI Services | Vertex AI    |


####  Containers & Big Data
| #  | Description        | AWS        | Azure                        | Google Cloud   |
| -- | ------------------ | ---------- | ---------------------------- | -------------- |
| 9  | Managed Kubernetes | Amazon EKS | Azure AKS                    | Google GKE     |
| 27 | Big Data Platform  | Amazon EMR | Azure Databricks / HDInsight | Cloud Dataproc |


Enterprise & Advanced Services

| #  | Description                | AWS               | Azure                        | Google Cloud             |
| -- | -------------------------- | ----------------- | ---------------------------- | ------------------------ |
| 25 | Desktop as a Service       | Amazon WorkSpaces | Azure Virtual Desktop        | Dizzion Frame            |
| 26 | Backup & Disaster Recovery | AWS Backup        | Azure Backup + Site Recovery | DR Service               |
| 29 | Media Processing           | AWS MediaConvert  | Azure Media Services         | Transcoder API           |
| 30 | Notifications              | Amazon SNS        | Azure Communication Services | Firebase Cloud Messaging |




#


 

### 2) Big Similarities
As my research, all thes three service providers offer the same "core building segments":

#### Compute (VMs), Storage (object + disks + files), and Networking (VPC/VNet, DNS, load balancing).
#### Serverless functions for event-driven code (Lambda / Functions / Cloud Functions).
#### Managed databases (relational + NoSQL) and analytics (warehouse + big data processing).
#### Security services for identity and encryption keys (IAM/Entra/IAM + KMS/Key Vault/KMS).
#### DevOps tools for CI/CD and Infrastructure as Code.
As we talking about the biggest difference is, is usually by service name, how components are grouped, and default integrations, rather than whether the capability exists.

### 3) Key Differences
#### 3.1) Naming + product packaging

For AWS, which products family often uses short product names (EC2, S3, RDS).
For Azure, wich  often uses "Azure + concept" names (Azure Virtual Machines, Azure Blob Storage).
For Google Cloud, which often uses direct functional names, for example, Compute Engine, Cloud Storage, without providers' name.

#### 3.2) "One service" vs "multiple services"
In some caes, descriptions of one AWS service, will map to multiple services in Azure/GCP:

####
Example: "Managed relational DB" → AWS RDS is one umbrella, while Azure commonly splits by engine (Azure SQL / Azure Database for MySQL/Postgres).
Example: "Notifications" → AWS SNS is broad, while GCP commonly uses FCM for push plus partners for SMS/email.
#### 3.3) Governance and data tooling

##### Azure is strong in "enterprise governance" branding (Purview).
##### Google Cloud often groups governance into "data platform" families (Dataplex).
##### AWS ties many governance/metadata pieces into analytics services (Glue catalog).

###  4) Unique strengths
As my research,

##### AWS:  Which service had already been running for longest time, very mature service catalog; lots of options per category.
##### Azure:  Which is alignment with Microsoft Software and Application family standard and system.
##### Google Cloud: Which is strong in data analytics (BigQuery),  and, provides developer-friendly managed services.


#### 5) Naming convention patterns, for AWS, Azure and Google Cloud
##### VMs: EC2 ↔ Azure Virtual Machines ↔ Compute Engine
##### Object storage: S3 ↔ Blob Storage ↔ Cloud Storage
##### Kubernetes: EKS ↔ AKS ↔ GKE
##### Functions: Lambda ↔ Functions ↔ Cloud Functions
##### Data warehouse: Redshift ↔ Synapse ↔ BigQuery
 

### Reference:
[1] Amazon Web Services, "AWS Documentation," Amazon Web Services. [Online]. Available: https://docs.aws.amazon.com/. [Accessed: Feb. 20, 2026].

[2] Microsoft, "Azure Documentation," Microsoft Learn. [Online]. Available: https://learn.microsoft.com/azure/. [Accessed: Feb. 20, 2026].

[3] Google Cloud, "Google Cloud Documentation," Google Cloud. [Online]. Available: https://cloud.google.com/docs. [Accessed: Feb. 20, 2026].

 
