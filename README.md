# Hi, I'm Zaheer Beg 👋

**DevOps Engineer** · Mumbai, India · [LinkedIn](https://www.linkedin.com/in/zaheer-beg-a21770ab/) · [Email](mailto:zaheerbeg21@gmail.com)

Software Engineer with 7+ years of experience building, deploying, and operating production applications across AWS, Azure, and self-hosted environments. Experienced in Docker, Nginx, PostgreSQL, Redis, FastAPI, Odoo, and cloud infrastructure, with a focus on platform operations, deployment automation, and production reliability. Proven experience supporting enterprise workloads and multi-service architectures in real-world deployments.

---

## 🚀 Production Deployments

| # | Repository | Industry | Stack | Scale |
|---|-----------|----------|-------|-------|
| 1 | [nginx-docker-multiservice-deploy](https://github.com/zaheerbeg21/nginx-docker-multiservice-deploy) | Manufacturing (Fortune 500) | Nginx · Docker · Odoo · Next.js · FastAPI · Azure AD SSO | 200+ field technicians · 24/7 · Middle East |
| 2 | [aws-rds-multitenant-erp](https://github.com/zaheerbeg21/aws-rds-multitenant-erp) | Manufacturing | AWS EC2 · RDS · S3 · ALB · Coolify · Traefik | Multi-tenant · 2 isolated clients |
| 3 | [azure-fastapi-redis-stack](https://github.com/zaheerbeg21/azure-fastapi-redis-stack) | Social Impact Platform | Azure VM · FastAPI · Next.js · PostgreSQL 15 · Redis 7 · Coolify | Full-stack · async API |
| 4 | [coolify-odoo-azure-deploy](https://github.com/zaheerbeg21/coolify-odoo-azure-deploy) | Facility Management | Azure VM · Odoo 18 · PostgreSQL 16 · Coolify · Traefik | 99% uptime SLA |
| 5 | [traefik-microservices-selfhosted](https://github.com/zaheerbeg21/traefik-microservices-selfhosted) | Field Services (Europe) | Coolify · Traefik · 4-service microstack · PostgreSQL | Self-hosted · Auto-SSL |
| 6 | [aws-rds-multitenant-erp-iac](https://github.com/zaheerbeg21/aws-rds-multitenant-erp-iac) | Manufacturing (IaC practice) | Terraform · AWS EC2 · RDS · S3 | Infra-as-code re-implementation of #2 |

**6 production systems · 3 cloud providers (AWS, Azure, Self-hosted) · 4 enterprise clients**

---

## 🏗️ Architecture at a Glance

```
On-Premise (#1)          AWS (#2)                  Azure (#3, #4)
─────────────────        ──────────────────────    ──────────────────────
Client VPN               ALB (SSL Termination)     Coolify + Traefik
     │                        │                          │
  Nginx :443              EC2 + Coolify             FastAPI / Odoo 18
  ├── Odoo 16             ├── Odoo A :8069          PostgreSQL 15/16
  ├── Next.js 15          └── Odoo B :8079          Redis 7 (AOF)
  ├── FastAPI WS          AWS RDS PostgreSQL
  └── Node.js             S3 (IAM Role, per-client)
  PostgreSQL (ext)
```

---

## 🛠️ DevOps Skills

**Cloud & Infrastructure**
`AWS (EC2, RDS, S3, ALB, IAM)` `Azure (VM, Entra ID / Azure AD)` `Self-hosted VPS`

**Containers & Orchestration**
`Docker` `Docker Compose v3.8/3.9` `Multi-stage builds` `Non-root execution` `Coolify`

**Reverse Proxy & SSL**
`Nginx 1.26` `Traefik` `Let's Encrypt auto-renewal` `Manual SSL/TLS cert management`

**CI/CD**
`Coolify git-push deployments` `Branch-based environments` `Health checks` `Auto-repair entrypoints`

**Databases**
`PostgreSQL 15/16` `AWS RDS` `Redis 7 (AOF)` `pg_dump/restore` `Migration scripts`

**Security**
`Microsoft Entra ID (Azure AD) SSO` `PBKDF2-SHA512` `IAM Role-based S3 access` `dbfilter multi-tenant isolation`

**Scripting**
`Bash` `PowerShell` `Python` `Node.js` `SQL`

**Monitoring**
`Docker health checks` `logrotate` `Cron logging` `Grafana`

---

## 📌 Highlighted Work

### Intelligent Entrypoint Script (aws-rds-multitenant-erp)
Auto-repairs database schema on every container start: `pg_isready` wait → `envsubst` config generation → monkey-patching → missing table detection/repair → stale asset cleanup → launch. Zero manual intervention needed after deploy.

### Multi-Tenant Isolation (aws-rds-multitenant-erp)
Single codebase, two isolated client instances. Branch-based deployments (`deploy/client-a`, `deploy/client-b`), separate RDS databases, per-client S3 buckets, strict `dbfilter` matching — no data leakage possible.

### 4-Service On-Premise Stack (nginx-docker-multiservice-deploy)
Odoo 16 ERP + Next.js 15 SSR + FastAPI WebSocket GPS + Node.js offline attendance — all behind Nginx with full SSL/TLS, WebSocket upgrade support, 512MB upload limit, Microsoft Entra ID SSO, and timezone-aware cron jobs. Deployed on a client's RDP machine with 24/7 uptime.

### Reusable Architecture Pattern
Same core pattern (`[Proxy] → [ERP + Frontend + GPS + Offline Sync] → PostgreSQL`) deployed across 3+ enterprise clients on different clouds — proving infrastructure portability through real use.

---

## 📊 GitHub Stats

![Snake animation](https://github.com/zaheerbeg21/zaheerbeg21/blob/output/github-contribution-grid-snake.svg)
---

## 🌐 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/zaheer-beg-a21770ab/)
[![Stack Overflow](https://img.shields.io/badge/-Stackoverflow-FE7A16?logo=stack-overflow&logoColor=white)](https://stackoverflow.com/users/13188708/zaheer-beg)
[![Email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:zaheerbeg21@gmail.com)

---

> *"Passionate about building self-hosted, production-ready systems that actually run in the real world."*
