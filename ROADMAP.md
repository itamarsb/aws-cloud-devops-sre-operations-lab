
---

# 5. ROADMAP.md

```markdown
# Project Roadmap

This roadmap defines the progressive evolution of the AWS Cloud, DevOps & SRE Operations Lab.

---

## Stage 00 — Workstation & Repository

### Objective

Prepare the engineering workstation and repository foundation.

### Topics

- Git
- GitHub
- GitHub CLI
- AWS CLI
- Terraform
- Docker
- kubectl
- Python
- Bash
- VS Code
- Repository structure
- AWS connectivity

---

## Stage 01 — AWS Foundation

### Topics

- AWS CLI
- IAM
- IAM Roles
- IAM Policies
- VPC
- Public and Private Subnets
- Route Tables
- Internet Gateway
- NAT concepts
- Security Groups
- Network ACLs
- EC2
- Systems Manager
- CloudWatch

---

## Stage 02 — Terraform Foundation

### Topics

- Terraform CLI
- Providers
- Resources
- Variables
- Outputs
- State
- Remote state
- Modules
- Environments
- AWS infrastructure provisioning

---

## Stage 03 — Linux Operations

### Topics

- Users and groups
- Permissions
- Processes
- Services
- systemd
- Networking
- Logs
- CPU
- Memory
- Disk
- Bash
- Troubleshooting

---

## Stage 04 — Python Workload

### Topics

- Python
- REST API
- Health checks
- Logging
- Metrics endpoints
- Environment variables
- Tests

---

## Stage 05 — Docker

### Topics

- Images
- Containers
- Dockerfiles
- Networking
- Volumes
- Registries
- ECR
- Container troubleshooting

---

## Stage 06 — Kubernetes

### Topics

- Pods
- Deployments
- Services
- ConfigMaps
- Secrets
- Health probes
- Resource limits
- Scaling
- Troubleshooting
- Amazon EKS

---

## Stage 07 — CI/CD with GitHub Actions

### Topics

- Workflows
- Triggers
- Tests
- Docker builds
- Security checks
- ECR publishing
- AWS authentication
- Deployment automation

---

## Stage 08 — Monitoring

### Tools

- Amazon CloudWatch
- Zabbix

### Topics

- Infrastructure monitoring
- Metrics
- Thresholds
- Alerts
- Dashboards
- Availability monitoring

---

## Stage 09 — Observability

### Tool

- Datadog

### Topics

- Metrics
- Logs
- Traces
- Dashboards
- Alerts
- Application performance monitoring
- Infrastructure observability

---

## Stage 10 — SRE Operations

### Topics

- SLI
- SLO
- SLA
- Error budgets
- Alerting
- Incident response
- MTTR
- Reliability
- Root Cause Analysis
- Postmortems
- Runbooks

---

## Stage 11 — FinOps & Security

### Topics

- IAM review
- Least privilege
- Security Groups
- Cost monitoring
- Rightsizing
- Idle resources
- Cost allocation
- AWS cost analysis
- FinOps recommendations

---

## Stage 12 — Production Incident Labs

Planned incident scenarios:

1. Application unavailable
2. High CPU utilization
3. Memory pressure
4. Disk exhaustion
5. Kubernetes CrashLoopBackOff
6. Network connectivity failure
7. IAM AccessDenied
8. CI/CD deployment failure
9. Application latency degradation
10. Unexpected AWS cost

Each incident will produce:

- Incident report
- Timeline
- Root Cause Analysis
- Resolution
- Corrective actions
- Postmortem
