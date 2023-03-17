# Week 4 — Postgres and RDS

### Watched Security Considerations - Securing Your Amazon RDS Postgres Database

Data stored in RDS needs to be secure as it can contain sensitive information.
Create an Amazon RDS Postgres for Developers to use for their Web Application in AWS

Spun up a Postgres RDS instance on AWS, reviewed it settings in Connectivity & Security & Configuration such as public accessibility, firewall inbound rules, outbound rules etc.

Added a rule under inbound rule to allow us to connect to the instance using a client called DBeaver. Added Custom TCP traffic type, port, source

Some Security Best Practices:

- Use VPCs: Use Amazon Virtual Private Cloud (VPC) to create a private network for your RDS instance. This helps prevent unauthorized access to your instance from the public internet.
- Compliance standard is what your business requires
- RDS Instances should only be in the AWS region that you are legally allowed to be holding user data in.
- Amazon Organizations SCP --> to manage RDS deletion, RDS creation, region lock, RDS Encryption enforced etc
- AWS CloudTrail is enabled & monitored to trigger alerts on malicious RDS behaviour by an identity in AWS.
- Amazon Guardduty is enabled in the account and region of RDS

- RDS Instance to use appropriate Authentication -Use IAM authentication, kerberos etc (not the default)
- Database User Lifecycle Management - Create, Modify, Delete Users
- AWS User Access Lifecycle Management - Change of Roles/ Revoke Roles etc
- Security Group to be restricted only to known IPs
- Not have RDS be internet accessible
- Encryption in Transit for comms between App & RDS
- Secret Management: Master User passwords can be used with AWS Secrets Manager to automatically rotate the secrets for Amazon RDS.
