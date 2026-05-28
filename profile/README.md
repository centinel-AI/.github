<div align="center">

# ◢ GRAUSS

### **Deploy infrastructure with AI agents**

*Describe what you want. The agents provision it, watch it, and keep it that way.*

<br/>

[![Beta](https://img.shields.io/badge/%E2%97%8F_Beta-Early_access-059669?style=for-the-badge)](https://grauss.io)
[![Status](https://img.shields.io/badge/Actively-building-10B981?style=for-the-badge)](#)

<br/>

> **Provisioning infra today means writing Terraform, opening PRs and praying.**
> Grauss changes that: you declare the intent, **the agents run the deploy**
> and fix drift without you touching a single manifest.

<br/>

</div>

---

## What it solves

| | Before | With Grauss |
|---|---|---|
| 🚀 **Deploy** | Hand-written Terraform, PRs, manual review | Declare the intent, the agent applies it |
| 🔁 **Maintain** | Infra drifts away from your IaC over time | Continuous reconciliation toward your intent |
| 🩺 **Watch** | 847 alerts → noise everyone ignores | Correlated down to 1 incident with root cause |
| 💶 **Cost** | The bill surprises you at month-end | Cost attributed and overruns caught on the fly |

---

## Architecture

```
grauss/
├── 🧠 engine     orchestration — the agents that plan and apply
├── ☸️  agent      runs in your Kubernetes cluster and reports state
├── 🌐 portal     customer platform — you declare intent, you see state
└── 🛰️  monitor    AI watch — drift, incidents and cost
```

```
Next.js 16  ·  Azure Postgres + pgvector  ·  Claude (planning + synthesis)
Deployed on Azure AKS  ·  Slack / email  ·  Stripe
```

Isolation per **project**: each project has its own cloud, connectors and AI key (BYOK).

---

## Connectors

**Today** ☸️ Kubernetes · 🦊 GitLab CI/CD · 🐙 GitHub Actions · 📊 Prometheus/Grafana
**Soon** 🔔 PagerDuty · 🔵 New Relic · ☁️ CloudWatch · 🔷 Azure Monitor · 🟠 GCP · 🪲 Sentry · 🐕 Datadog · 🤖 Slack · 🟢 UptimeRobot

> It connects to what you already run. K8s via an agent; everything else, a webhook URL.

---

## Beta · pilot teams

We're looking for DevOps/SRE teams to pilot Grauss in real production.

Early access · influence the roadmap · onboarding with the founding team.

**→ [grauss.io](https://grauss.io)**

---

<div align="center">

**Grauss** · 2026 
[🌐 Website](https://grauss.io) · [💼 LinkedIn](https://linkedin.com/company/grauss) · [📧 Contact](mailto:info@grauss.io)

*Your infrastructure never sleeps. Now you can.*

</div>
