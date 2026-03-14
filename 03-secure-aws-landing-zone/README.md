# Lab 3 — Secure AWS Landing Zone Architecture

## Objective

The objective of this lab is to design a secure AWS Landing Zone architecture that provides a scalable, governed, and security-focused foundation for enterprise cloud workloads.

Before large organisations migrate workloads to AWS, they establish a **Landing Zone** that defines account structure, governance controls, identity management, and centralized logging.

This lab demonstrates how a Cloud Architect designs the foundational AWS environment required for secure cloud adoption.


## Scenario

Following the migration readiness assessment and migration strategy planning in previous labs, the organisation is preparing to migrate multiple workloads to AWS.

To support a secure and scalable cloud environment, the architecture team must first design a **Landing Zone architecture** that enforces security controls, governance, and operational standards across all AWS accounts.

The landing zone will support future migration of:

- VMware workloads
- SQL databases
- Internal web applications
- File storage systems
- Identity services


## What is an AWS Landing Zone?

An AWS Landing Zone is a **secure multi-account AWS environment** that provides:

- Centralized security monitoring
- Identity and access governance
- Logging and auditing
- Account isolation
- Network architecture standards

This ensures that all workloads deployed into AWS follow consistent **security and compliance standards**.


## Landing Zone Architecture Design

The landing zone uses **AWS Organizations** to structure multiple AWS accounts for different operational purposes.


AWS Organization
│
├── Security Account
│ ├── AWS GuardDuty
│ ├── AWS Security Hub
│ └── AWS Config
│
├── Log Archive Account
│ └── Centralized CloudTrail & S3 logging
│
├── Shared Services Account
│ ├── Active Directory Integration
│ └── Shared networking services
│
├── Workload Accounts
│ ├── Application workloads
│ ├── Databases
│ └── Web services
│
└── Management Account
└── Governance and billing management




## Core Security Services Used

The landing zone integrates several AWS security services to maintain visibility and control across all accounts.

### AWS GuardDuty
Provides threat detection by analyzing AWS logs and network activity.

### AWS Security Hub
Central dashboard for monitoring security findings across AWS services.

### AWS Config
Tracks configuration changes and enforces compliance policies.

### AWS CloudTrail
Captures API activity across AWS accounts for auditing and investigation.

### Amazon S3 (Centralized Logging)
Stores CloudTrail logs and security findings in a dedicated log archive account.


## Governance and Control

Governance across AWS accounts is enforced using **Service Control Policies (SCPs)** within AWS Organizations.

Examples of governance controls include:

- Preventing creation of resources in unapproved regions
- Enforcing encryption requirements
- Restricting privileged IAM actions
- Enforcing logging and monitoring standards


## Architecture Benefits

The secure landing zone architecture provides several benefits:

- Secure account isolation
- Centralized security monitoring
- Consistent governance controls
- Improved audit and compliance capability
- Scalable environment for enterprise workloads


## Architecture Tools Referenced

- AWS Organizations
- AWS Control Tower
- AWS GuardDuty
- AWS Security Hub
- AWS Config
- AWS CloudTrail
- Amazon S3
- AWS IAM


## Summary

This lab demonstrates how a Cloud Architect designs the foundational AWS environment required before enterprise workloads migrate to the cloud.

By implementing a secure landing zone, organisations ensure that future cloud workloads are deployed within a **well-governed, secure, and compliant cloud architecture**.



## Landing Zone Architecture Overview


AWS Organization
│
├── Management Account
│   └── Billing and governance
│
├── Security Account
│   ├── AWS GuardDuty
│   ├── AWS Security Hub
│   └── AWS Config
│
├── Log Archive Account
│   └── Centralized CloudTrail logs stored in Amazon S3
│
├── Shared Services Account
│   ├── Directory services
│   ├── CI/CD pipelines
│   └── Shared networking
│
└── Workload Accounts
    ├── Application workloads
    ├── Databases
    └── Web services




