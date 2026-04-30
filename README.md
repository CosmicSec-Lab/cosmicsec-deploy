<div align="center">
  <img src="https://via.placeholder.com/150x150.png?text=CosmicSec" alt="CosmicSec Logo" width="120" />
  <h1>🚢 CosmicSec Deploy (Manifest)</h1>
  <p><strong>The central orchestration and infrastructure-as-code repository.</strong></p>
  
  <p>
    <a href="https://github.com/CosmicSec-Lab/cosmicsec-deploy/actions"><img src="https://img.shields.io/github/actions/workflow/status/CosmicSec-Lab/cosmicsec-deploy/build.yml?logo=github&style=flat-square" alt="Build Status"></a>
    <a href="https://github.com/CosmicSec-Lab/cosmicsec-deploy/issues"><img src="https://img.shields.io/github/issues/CosmicSec-Lab/cosmicsec-deploy?style=flat-square" alt="Issues"></a>
    <a href="https://github.com/CosmicSec-Lab/cosmicsec-deploy/pulls"><img src="https://img.shields.io/github/issues-pr/CosmicSec-Lab/cosmicsec-deploy?style=flat-square" alt="Pull Requests"></a>
    <a href="https://github.com/CosmicSec-Lab/cosmicsec-deploy/blob/main/LICENSE"><img src="https://img.shields.io/github/license/CosmicSec-Lab/cosmicsec-deploy?style=flat-square" alt="License"></a>
  </p>
</div>

<hr />

## 📖 Table of Contents
- [Executive Summary](#-executive-summary)
- [Architecture & Domain](#-architecture--domain)
- [Technical Specifications](#-technical-specifications)
- [Getting Started](#-getting-started)
- [Contributing](#-contributing)
- [License & Security](#-license--security)

---

## 🎯 Executive Summary
**CosmicSec Deploy** is the umbrella repository (Master Manifest) for the entire organization. It unites `cosmicsec-core`, `cosmicsec-web`, `cosmicsec-ai`, and all specialized services into a unified, highly available platform. Its primary goal is to provide a deterministic, one-click deployment experience for local development, staging, and enterprise production environments.

## 🏗️ Architecture & Domain
- **Infrastructure as Code (IaC):** Immutable infrastructure scripts (Terraform, Pulumi) for provisioning multi-cloud AWS/GCP/Azure resources.
- **Container Orchestration:** 
  - **Local/Dev:** Master `docker-compose.yml` that seamlessly pulls together adjacent Git repositories.
  - **Production:** Production-grade Kubernetes manifests and Helm charts featuring auto-scaling, pod disruption budgets, and ingress routing.
- **CI/CD Pipelines:** Global GitHub Actions workflows that monitor and orchestrate dependent deployments across the entire multi-repo architecture.

## 🚀 Getting Started (Local Development)

To launch the entire CosmicSec platform locally, you must clone this repository alongside the others into a shared parent directory.

### Directory Structure
```text
/Miraz_Work
├── cosmicsec-core/
├── cosmicsec-web/
├── cosmicsec-services/
├── cosmicsec-ai/
└── cosmicsec-deploy/     <-- You are here
```

### Execution
```bash
# Navigate into the deploy manifest
cd cosmicsec-deploy

# Build and start the entire platform in detached mode
docker compose up --build -d

# View live aggregate logs
docker compose logs -f
```

## 🛡️ License & Security
All rights reserved by **CosmicSec-Lab**.
