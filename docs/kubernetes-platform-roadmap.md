# Kubernetes Platform Engineering Track — Local Kubernetes to Amazon EKS

**Status:** proposed specialization; existing Stage 00 and Stage 01 status remain unchanged.

## Purpose and boundaries

This repository owns **Kubernetes platform operations**, from local clusters to short-lived Amazon EKS validation: workloads, scheduling, deployment strategy, networking, storage, security, autoscaling, GitOps, incident response and reproducible cleanup.

- Prerequisite Linux, AWS and Terraform operations: [Cloud Infrastructure Operations Lab](https://github.com/itamarsb/cloud-infrastructure-operations-lab).
- Docker image engineering, Compose, Amazon ECR and ECS deployment: [AWS Cloud Engineering Lab](https://github.com/itamarsb/aws-cloud-engineering-lab).
- Grafana dashboards, TCC observability framework and the space systems repository remain independent.
- The original numbered Stage 00–12 roadmap stays as historical planning context. The **K** identifiers below are a focused sub-track, not a claim of completion.

## Deployment environments

1. **Local first:** Docker + kind (Kubernetes in Docker), kubectl and Helm. The local cluster must be reproducible and disposable.
2. **Platform operations:** deploy a versioned Python/FastAPI reference workload using Kubernetes manifests, Kustomize and Helm. Test health, rollouts, failures and access controls.
3. **Cloud validation:** use Terraform to provision EKS **only after** the local track is evidenced and a cost/cleanup plan has been reviewed. Keep the cluster short-lived.

## Progressive lab map

| Lab | Focus | Required demonstration |
|---|---|---|
| K00 | Local toolchain | Version checks, kind cluster create/delete |
| K01 | Kubernetes primitives | Namespaces, Pods, kubectl describe/events/logs |
| K02 | Deployments | Replicas, rolling updates, rollback |
| K03 | Networking | Services, CoreDNS and service reachability |
| K04 | Configuration | ConfigMaps and Secrets without committing secrets |
| K05 | Persistence | PV, PVC, reclaim behavior and restoration |
| K06 | Reliability | Startup/readiness/liveness probes; resource requests/limits |
| K07 | HTTP routing | Ingress or Gateway API controller, documented choice |
| K08 | Helm | Versioned chart with values and rollback |
| K09 | Kustomize | Base and dev/prod overlays; diff before apply |
| K10 | Capacity | Metrics Server, HPA and bounded load test |
| K11 | Security | ServiceAccounts, RBAC, Pod Security and NetworkPolicies with supported CNI |
| K12 | CI | GitHub Actions checks for image, YAML and chart |
| K13 | GitOps | Argo CD reconciliation and rollback test |
| K14 | Observability | Events, logs, metrics and incident triage; no dashboard duplication |
| K15 | Incidents | CrashLoopBackOff, OOMKilled, failed readiness, DNS and scheduling |
| K16 | Terraform AWS | Versioned EKS infrastructure plan, tags, IAM and cost review |
| K17 | Amazon EKS | Short-lived deployment, cluster/network verification |
| K18 | Production operations | Upgrade/rollback exercises, runbook, destroy and independent verification |

## Definition of done

Each lab must include: objective, dependencies, architecture, reproducible commands/configuration, positive/negative tests, evidence screenshots or logs, diagnosis, remediation, and teardown. Keep unexecuted work explicitly **Planned**.

Record the image digest and workload version when demonstrating Kubernetes rollouts. Do not assert a multi-AZ, production-grade or HA architecture unless actually tested.

## Repository organization proposal

Preserve existing directories. As labs are implemented, organize them under:

```text
apps/python-service/       # reference workload and tests
docker/                    # development-only local image tooling
kubernetes/base/           # workload manifests
kubernetes/overlays/dev/   # Kustomize environment
kubernetes/overlays/prod/  # illustrative configuration, not live prod
kubernetes/helm/           # versioned chart
terraform/modules/         # shared EKS-supporting modules, once implemented
terraform/envs/            # temporary lab environments
docs/runbooks/             # operational diagnostics and rollback
docs/evidence/             # execution evidence by K lab
.github/workflows/         # lint, build and controlled deployment
```

Do not create directories or copy manifests simply to make the tree look complete; add working files as the related lab is executed.

## Cost and safety guardrails

Most Kubernetes learning belongs on **kind** to avoid persistent cloud charges. EKS control plane, compute nodes, public IPv4, NAT gateways, load balancers, EBS and telemetry may incur costs. Set an AWS budget/alert before any EKS deployment, use short lab windows and perform a verified destroy. Do not use static long-lived AWS keys. Prefer least-privilege IAM and ephemeral credentials.

## Portfolio result

Show a versioned and secure application progressing from local Kubernetes to a documented EKS deployment, with Helm/Kustomize, GitOps, reproducible incident recovery, controlled IaC and proven cleanup.
