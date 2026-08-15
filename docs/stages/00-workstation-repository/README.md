# Stage 00 — Workstation & Repository

## Objective

Prepare and validate the engineering workstation required for the AWS Cloud, DevOps & SRE Operations Lab.

This stage establishes the local development environment, command-line tools, Git workflow and repository structure used throughout all subsequent stages.

---

## Tools

The following tools will be installed and validated:

- Git
- GitHub CLI
- AWS CLI
- Terraform
- Docker
- kubectl
- Python 3
- Bash
- Visual Studio Code

Optional Linux utilities:

- curl
- wget
- jq
- tree
- unzip

---

## Stage Goals

By the end of this stage, the workstation must be able to:

- Clone and update GitHub repositories
- Authenticate with GitHub
- Authenticate with AWS
- Execute AWS CLI commands
- Execute Terraform commands
- Build and run Docker containers
- Execute kubectl commands
- Run Python scripts
- Run Bash scripts
- Commit and push changes to GitHub

---

# Step 1 — Git Validation

Run:

```bash
git --version
