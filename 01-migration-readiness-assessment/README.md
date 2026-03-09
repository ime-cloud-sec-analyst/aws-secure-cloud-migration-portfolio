# Lab 1 — Secure Cloud Migration Readiness Assessment

## Objective
The goal of this lab is to simulate how a Lead Technical Architect evaluates an organisation before migrating workloads from on-premise infrastructure to AWS.

## Scenario
A government organisation currently operates multiple systems on-premise. The objective is to assess migration readiness and identify the most appropriate migration strategies.

## Current Environment
- 15 Virtual Machines (VMware)
- 2 SQL Databases
- 1 File Storage Server
- Internal Active Directory
- Web Application hosted internally

## Assessment Tasks
1. Identify workloads
2. Determine dependencies
3. Assess security risks
4. Choose migration strategies
5. Define AWS target services

## Tools Referenced
- AWS Migration Hub
- AWS Application Migration Service
- AWS Database Migration Service
- AWS DataSync

## Expected Outcome
A migration readiness report identifying migration strategy for each workload.

## System Inventory

| System | Type | Function | Criticality |
|------|------|------|------|
| Web Server | VM | Hosts public website | High |
| Application Server | VM | Runs backend services | High |
| Database Server | SQL Server | Stores customer data | Critical |
| File Storage | NAS | Stores documents | Medium |
| Active Directory | Windows Server | Identity management | Critical |

## System Dependencies

Web Server → connects to Application Server

Application Server → connects to Database Server

Users → authenticate through Active Directory

Documents → stored in File Storage Server

## Current Architecture (On-Premise)

Users
  ↓
Web Server
  ↓
Application Server
  ↓
Database Server

Application Server → File Storage

Employees → Authenticate via Active Directory

## Security Risk Assessment


Potential security risks identified in the current on-premise environment include:

- Unencrypted data transfer between systems
- Weak access control policies and privilege management
- Legacy operating systems that may contain vulnerabilities
- Lack of centralised logging and monitoring
- Limited disaster recovery capability

## Migration Strategy

| System | Strategy |
|------|------|
| Web Server | Rehost (Lift and Shift) |
| Application Server | Replatform |
| Database Server | Refactor to Amazon RDS |
| File Storage | Migrate to Amazon S3 |
| Active Directory | Extend to AWS Directory Service |

## Target AWS Architecture

| On-Prem System | AWS Service |
|------|------|
| Web Server | Amazon EC2 |
| Application Server | Amazon EC2 |
| Database Server | Amazon RDS |
| File Storage | Amazon S3 |
| Active Directory | AWS Directory Service |

## AWS Migration Tools

| Tool | Purpose |
|------|------|
| AWS Migration Hub | Track migration progress |
| AWS Application Migration Service | Migrate servers |
| AWS Database Migration Service | Migrate databases |
| AWS DataSync | Transfer file storage |

## Architect Summary

Before migrating workloads to AWS, the organisation must conduct a structured migration readiness assessment. This includes system discovery, dependency mapping, risk analysis, and migration strategy selection.

Using AWS migration services and secure architecture principles aligned with the AWS Well-Architected Security Pillar ensures the migration process remains secure, auditable, and reliable.

