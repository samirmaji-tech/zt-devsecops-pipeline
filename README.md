# Zero-Trust DevSecOps Pipeline

A CI/CD pipeline built around Zero-Trust security principles — combining policy-as-code enforcement, container security scanning, and automated vulnerability checks into the software delivery process.

> 📌 This was built as a 2-person group project. See [Contributions](#contributions) below for what each of us worked on.

## Overview

This project implements a DevSecOps pipeline that enforces security controls at every stage of the CI/CD process rather than treating security as an afterthought. Key components include:

- **Policy-as-code** — OPA (Open Policy Agent) rules that gate deployments based on defined security policies
- **Container security scanning** — automated vulnerability checks on container images before deployment
- **Infrastructure as Code** — Terraform-managed infrastructure with security guardrails baked in
- **CI automation** — GitHub Actions workflows that run security checks, tests, and audits on every change

## Tech Stack

- **CI/CD:** GitHub Actions
- **Policy Enforcement:** Open Policy Agent (OPA)
- **IaC:** Terraform (HCL)
- **Languages:** Go, Python
- **Security:** Semgrep (SAST), container/dependency scanning

## Repository Structure

```
.github/workflows/   → CI pipeline definitions
app/                 → Application code
build/               → Build scripts and configuration
docs/architecture/   → Architecture documentation
infra/               → Infrastructure as Code (Terraform)
policy/              → OPA policy-as-code rules
scripts/             → Automation/utility scripts
security/            → Security scanning configuration
tests/audit/         → Audit and compliance tests
```

## Getting Started

```bash
# Clone the repo
git clone https://github.com/samirmaji-tech/zt-devsecops-pipeline.git
cd zt-devsecops-pipeline

# [Add your actual setup/run instructions here, e.g.:]
# make build
# make test
```

## Contributions

This was a collaborative group project. Breakdown of individual contributions:

**Samir Maji ([@samirmaji-tech](https://github.com/samirmaji-tech))**
- Terraform & AWS infrastructure setup (`infra/`) — provisioning and infrastructure-as-code for the pipeline's cloud resources
- CI/CD pipeline design and implementation (`.github/workflows/`) — automating build, test, and security-check stages
- Co-developed the OPA policy-as-code rules (`policy/`)

**G. Ananthapadmanabhan ([@Ananthapad77](https://github.com/Ananthapad77))**
- Application and container development (`app/`, `build/`) — building and containerizing the application layer
- Co-developed the OPA policy-as-code rules (`policy/`)

## Notes

- `devopslabcloud-AI` appears in the commit history as a shared lab/automation account used during development.
- This repo is a full-history mirror of the original project repository, preserved for portfolio purposes.
