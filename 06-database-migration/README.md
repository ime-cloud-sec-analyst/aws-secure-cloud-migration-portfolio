```text
Corporate Data Center
(On-Premise Database)
    │
    │ Secure Connection
    ▼
AWS Database Migration Service

    │
    │ Continuous Replication
    ▼

Amazon RDS Database
(AWS Cloud)
```


---

## Migration Workflow

1. The on-premise database acts as the migration source.
2. AWS Database Migration Service connects securely to the source database.
3. Data is replicated continuously to the AWS environment.
4. Amazon RDS becomes the target database infrastructure.
5. Applications are redirected to the AWS database after migration completion.

---

## Security Benefits

• encrypted data transfer  
• minimal service downtime  
• high availability  
• managed database infrastructure  
• improved scalability

---

## Conclusion

Database migration is a critical part of enterprise cloud transformation. Using AWS Database Migration Service and Amazon RDS enables organisations to migrate databases securely while maintaining reliability and application availability.