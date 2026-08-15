
# AWS Cloud, DevOps & SRE Operations Lab

A hands-on engineering laboratory focused on Cloud, DevOps, Site Reliability Engineering, Monitoring, Observability, Infrastructure Automation, Incident Management and FinOps using AWS and modern infrastructure tooling.

This repository is designed as an end-to-end operational environment where infrastructure is built, deployed, monitored, intentionally broken, investigated and improved.

---

## Project Objectives

The main objective of this repository is to develop practical experience across the complete lifecycle of modern cloud infrastructure operations.

The project covers:

- AWS Cloud Infrastructure
- Linux Administration
- Terraform / Infrastructure as Code
- Docker
- Kubernetes
- Git and GitHub
- GitHub Actions
- CI/CD
- Python
- Bash
- AWS Networking
- IAM and Cloud Security
- Monitoring with Zabbix
- Monitoring with Amazon CloudWatch
- Observability with Datadog
- Troubleshooting
- Incident Management
- Root Cause Analysis
- Runbooks
- SLI, SLO and reliability concepts
- FinOps
- Production incident simulations

---

## Architecture Evolution

The platform will evolve incrementally throughout the laboratory.

```mermaid
flowchart TD

    DEV[Developer]

    DEV --> GIT[Git / GitHub]

    GIT --> CICD[GitHub Actions CI/CD]

    CICD --> TESTS[Tests]
    CICD --> BUILD[Docker Build]
    CICD --> DEPLOY[Deployment]

    DEPLOY --> AWS[AWS Cloud]

    AWS --> IAM[IAM / Security]
    AWS --> VPC[VPC Networking]

    VPC --> LB[Load Balancer]
    LB --> K8S[Kubernetes / EKS]

    K8S --> APP[Python Application]

    APP --> CW[CloudWatch]
    APP --> ZABBIX[Zabbix]
    APP --> DATADOG[Datadog]

    CW --> OPS[Operations]
    ZABBIX --> OPS
    DATADOG --> OPS

    OPS --> TROUBLE[Troubleshooting]
    OPS --> INCIDENT[Incident Management]
    OPS --> SRE[SRE Practices]
    OPS --> FINOPS[FinOps]

```
---


```markdown
aws-cloud-devops-sre-operations-lab/
│
├── README.md
├── LICENSE
├── .gitignore
├── ROADMAP.md
├── CHANGELOG.md
├── CONTRIBUTING.md
│
├── docs/
│   ├── architecture/
│   │
│   ├── getting-started/
│   │
│   ├── stages/
│   │   └── 00-workstation-repository/
│   │
│   ├── aws/
│   ├── linux/
│   ├── terraform/
│   ├── docker/
│   ├── kubernetes/
│   ├── ci-cd/
│   │
│   ├── monitoring/
│   │   ├── zabbix/
│   │   └── cloudwatch/
│   │
│   ├── observability/
│   │   └── datadog/
│   │
│   ├── troubleshooting/
│   ├── incidents/
│   ├── runbooks/
│   ├── finops/
│   └── security/
│
├── scripts/
│   ├── bash/
│   └── python/
│
├── terraform/
│   ├── modules/
│   └── envs/
│       ├── dev/
│       └── prod/
│
├── docker/
│
├── kubernetes/
│   ├── base/
│   ├── overlays/
│   │   ├── dev/
│   │   └── prod/
│   └── helm/
│
├── apps/
│   └── python-service/
│       ├── app/
│       ├── tests/
│       ├── requirements.txt
│       ├── Dockerfile
│       └── README.md
│
├── .github/
│   └── workflows/
│
├── images/
│
└── .vscode/
```

---

## 📈 Repository Metrics

<p align="center">
  <a href="http://s01.flagcounter.com/more/058">
    <img
      src="https://s01.flagcounter.com/count/058/bg_FFFFFF/txt_000000/border_CCCCCC/columns_8/maxflags_120/viewers_0/labels_1/pageviews_1/flags_0/percent_0/"
      alt="Flag Counter"
      width="900"
    />
  </a>
</p>

