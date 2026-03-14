# Lab 2 — Enterprise Cloud Migration Strategy Framework

## Objective

The objective of this lab is to design an enterprise migration strategy that moves workloads from on-premise infrastructure to AWS using structured migration waves and the AWS 6R migration model.

The lab simulates how a cloud architect plans and coordinates large-scale enterprise migrations while minimizing downtime, operational risk, and security exposure.


## Scenario

Following the readiness assessment completed in Lab 1, the organisation has approved migration to AWS.

The on-premise environment contains:

• 15 VMware virtual machines  
• 2 SQL databases  
• 1 file storage server  
• Internal Active Directory identity services  
• A web application hosted internally

The enterprise architecture team must now determine the best migration strategy for each workload and plan the migration phases.


## AWS 6R Migration Framework

This migration plan follows the AWS 6R model used by enterprise cloud architects:

1. Rehost – Lift and shift workloads to EC2
2. Replatform – Optimize applications during migration
3. Refactor – Redesign applications for cloud-native services
4. Repurchase – Replace with SaaS solutions
5. Retire – Decommission unused systems
6. Retain – Keep certain workloads on-premise temporarily


## Migration Planning Tasks

During this stage the architecture team performs:

• Application dependency mapping  
• Workload prioritisation  
• Migration wave planning  
• Strategy assignment using the 6R model  
• Risk assessment for each system  
• Identification of target AWS services


## Enterprise Migration Strategy Architecture


On-Premise Data Center
│
├── VMware Virtual Machines
├── SQL Databases
├── Active Directory
├── File Storage Server
└── Internal Web Application
        │
        │  (Migration Planning & Discovery)
        ▼
Migration Tools
│
├── AWS Application Discovery Service
├── AWS Migration Hub
├── AWS Migration Evaluator
└── AWS Database Migration Service
        │
        │  (Migration Execution)
        ▼
AWS Cloud Environment
│
├── Amazon EC2 (Lift & Shift workloads)
├── Amazon RDS (Database migration)
├── Amazon S3 (File storage)
├── AWS IAM (Identity management)
└── Elastic Load Balancer (Web application traffic)


## Migration Wave Planning

Enterprise migrations are typically executed in phases called **migration waves**.  
Each wave groups workloads that can be migrated together with minimal risk.

| Migration Wave | Workloads | Migration Strategy | Target AWS Service |
|----------------|----------|-------------------|-------------------|
| Wave 1 | File Storage Server | Rehost | Amazon S3 |
| Wave 2 | Internal Web Application | Replatform | EC2 + Elastic Load Balancer |
| Wave 3 | SQL Databases | Refactor | Amazon RDS |
| Wave 4 | Active Directory | Retain / Hybrid | AWS Directory Service |
| Wave 5 | VMware Virtual Machines | Rehost | Amazon EC2 |


## Architecture Tools Referenced

The migration strategy and architecture planning leverage the following AWS and enterprise architecture tools:

• AWS Migration Hub – Central dashboard for tracking migration progress  
• AWS Application Discovery Service – Discovery of on-premise workloads and dependencies  
• AWS Migration Evaluator – Cloud cost modelling and migration planning  
• AWS Database Migration Service (DMS) – Migration of database workloads  
• AWS Well-Architected Framework – Cloud architecture best practices  
• AWS Migration Acceleration Program (MAP) – Enterprise migration methodology






