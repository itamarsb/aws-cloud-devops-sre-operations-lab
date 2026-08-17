# Stage 01 — AWS Foundation
# Lab 01 — AWS Account Security, Identity & Cost Baseline

This lab establishes the account's operational baseline prior to the creation of VPCs, EC2 instances, or other resources.

## Scope

- Validate current AWS identity using STS;
- Inventory user, ARN, account, and operational region;
- Verify MFA protection for the root user;
- Confirm that the root user has no access keys;
- Review primary, billing, operations, and security contacts;
- Analyze the current authentication method used for AWS login;
- Identify existing users, groups, roles, and policies;
- Check the IAM credential report;
- Configure AWS Free Tier alerts;
- Create a monthly AWS Budget with alerts for actual and forecasted costs;
- Record evidence without revealing the account ID, full ARN, email, or credentials;
- Produce a checklist covering validation, troubleshooting, and operational conclusions.

AWS recommends using temporary credentials and roles for human access, avoiding permanent access keys whenever possible. It also recommends restricting the root user to tasks that strictly require it and avoiding the creation of access keys for the root account.

The budget will be configured with alerts for both actual and forecasted costs. AWS Budgets monitors and notifies but does not automatically prevent new charges.
