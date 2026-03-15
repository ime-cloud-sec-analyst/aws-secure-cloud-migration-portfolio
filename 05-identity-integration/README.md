# Lab 5 — Identity Integration Architecture

## Identity Integration Architecture Diagram

```
Corporate User
      │
      │ Login
      ▼
Enterprise Identity Provider
(Azure AD / Active Directory)
      │
      │ SAML / Federation
      ▼
AWS IAM Identity Center
      │
      ▼
IAM Roles
      │
      ▼
AWS Resources
(EC2, S3, RDS, etc.)
```


## Overview

This lab demonstrates how enterprises integrate corporate identity systems with AWS during cloud migration. Identity integration ensures that employees can securely access cloud resources using their existing corporate credentials.

Most organisations rely on enterprise identity providers such as Active Directory or Azure AD. Integrating these systems with AWS allows centralised authentication and governance while maintaining strong security controls.

This architecture supports secure access to cloud workloads while maintaining enterprise identity management standards.

---

## Objective

The objective of this lab is to design a secure identity integration architecture that enables corporate users to authenticate into AWS environments using enterprise identity providers.

The architecture focuses on centralised authentication, role-based access control, and federated access management.

---

## Architecture Scenario

An enterprise organisation operates an on-premise Active Directory environment that manages all employee identities.

As part of a cloud migration initiative, workloads are being deployed into AWS accounts. To maintain governance and security, the organisation integrates its identity provider with AWS IAM Identity Center.

Corporate users authenticate using their enterprise credentials and are granted access to AWS resources through federated roles.

---

## Architecture Components

### Active Directory / Identity Provider
The enterprise identity provider manages employee authentication and identity lifecycle.

### AWS IAM Identity Center
Provides centralised identity management and enables single sign-on access to AWS accounts.

### IAM Roles
Define permissions and control access to AWS resources based on user responsibilities.

### Federation (SAML / Identity Federation)
Allows corporate identities to securely authenticate with AWS without creating separate IAM users.

---

## Security Benefits

• Centralised identity governance  
• Reduced credential sprawl  
• Strong authentication policies  
• Role-based access control  
• Secure federated authentication  

---

## Enterprise Architecture Flow

1. User signs in using corporate credentials.
2. Identity provider authenticates the user.
3. Authentication request is federated to AWS IAM Identity Center.
4. IAM roles grant appropriate access to AWS resources.
5. User securely accesses cloud services based on assigned permissions.

---

## Conclusion

Identity integration is a critical component of secure cloud migration. By integrating enterprise identity providers with AWS IAM Identity Center, organisations maintain strong governance while enabling secure access to cloud workloads.


