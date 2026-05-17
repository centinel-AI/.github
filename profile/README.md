<div align="center">

<br/>

```
 ██████╗███████╗███╗   ██╗████████╗██╗███╗   ██╗███████╗██╗      █████╗ ██╗
██╔════╝██╔════╝████╗  ██║╚══██╔══╝██║████╗  ██║██╔════╝██║     ██╔══██╗██║
██║     █████╗  ██╔██╗ ██║   ██║   ██║██╔██╗ ██║█████╗  ██║     ███████║██║
██║     ██╔══╝  ██║╚██╗██║   ██║   ██║██║╚██╗██║██╔══╝  ██║     ██╔══██║██║
╚██████╗███████╗██║ ╚████║   ██║   ██║██║ ╚████║███████╗███████╗██║  ██║██║
 ╚═════╝╚══════╝╚═╝  ╚═══╝   ╚═╝   ╚═╝╚═╝  ╚═══╝╚══════╝╚══════╝╚═╝  ╚═╝╚═╝
```

### *Your infrastructure never sleeps. Now you can.*

<br/>

[![Open Beta](https://img.shields.io/badge/🚀_Beta-Join_free-6C63FF?style=for-the-badge)](https://centinelai.io)
[![Status](https://img.shields.io/badge/Status-Actively_building-F59E0B?style=for-the-badge)](#roadmap)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Follow_us-0A66C2?style=for-the-badge&logo=linkedin)](https://linkedin.com/company/centinelai)

<br/>

> **How many alerts did your team receive yesterday?**
> How many actually mattered?

<br/>

</div>

---

## 🔥 The problem nobody has solved (yet)

<table>
<tr>
<td width="50%">

### Without centinelAI

```
🔴 ALERT: CPU > 80% on prod-api-01
🔴 ALERT: CPU > 80% on prod-api-01
🔴 ALERT: CPU > 80% on prod-api-01
🟡 WARN:  Elevated p99 latency
🔴 ALERT: CPU > 80% on prod-api-02
📧 EMAIL: Pipeline failed on staging
🔴 ALERT: CPU > 80% on prod-api-01
💬 SLACK: "hey, is anyone looking at this?"
🔴 ALERT: Memory usage > 90%
📟 PAGER: On-call woken up at 3am
🔴 ALERT: CPU > 80% on prod-api-03
💬 SLACK: "I see it, was a false positive"
🔴 ALERT: CPU > 80% on prod-api-01
...847 more tonight
```

❌ The team learns to ignore them  
❌ The real alert gets lost in the noise  
❌ The customer notices the outage before you do

</td>
<td width="50%">

### With centinelAI

```
🟣 [centinelAI] REAL INCIDENT — 03:47

   Service: prod-api (3 replicas)
   Root cause: OOMKilled after deploy
   at 03:30 (branch: feat/image-resize)
   Author: @carlos

   Impact: p99 latency +340ms
   Affected: ~120 active users

   ▶ Suggested action: rollback to v2.4.1
   ▶ kubectl rollout undo deployment/api

   Postmortem generated automatically.
```

✅ 1 notification, not 847  
✅ Root cause identified instantly  
✅ Your team sleeps. Your users too.

</td>
</tr>
</table>

---

## ⚡ What centinelAI does

<div align="center">

```
                  EVERYTHING GENERATING NOISE IN YOUR STACK
                                │
         ┌────────────────────┬─┴──────────────────┐
         ▼                    ▼                    ▼
   [Kubernetes]         [Datadog / NR]        [GitHub / GitLab]
   [Prometheus]         [Grafana]             [PagerDuty]
   [UptimeRobot]        [Alertmanager]        [Incoming Slack]
         │                    │                    │
         └────────────────────┼────────────────────┘
                              │
                              ▼
              ┌───────────────────────────────┐
              │       4-AGENT AI PIPELINE      │
              │                               │
              │  ➊ DEDUPLICATOR               │
              │     Removes repeated noise     │
              │     847 alerts → 23 unique     │
              │              │                │
              │  ➋ SCORER (Claude Haiku)      │
              │     Scores each alert 0-100    │
              │     23 unique → 8 relevant     │
              │              │                │
              │  ➌ CORRELATOR (Claude Haiku)  │
              │     Connects signals together  │
              │     8 relevant → 2 root causes │
              │              │                │
              │  ➍ NOTIFIER (Claude Sonnet)   │
              │     Generates actionable ctx   │
              │     2 causes → 1 that matters  │
              └───────────────────────────────┘
                              │
                              ▼  only if score > 70
              ┌───────────────────────────────┐
              │   YOUR TEAM — when it matters  │
              │   Slack · Email · Dashboard    │
              └───────────────────────────────┘
```

</div>

---

## 🔌 Connectors — Speaks your stack's language

> centinelAI doesn't ask you to change your tools. It connects to what you already have.

### ✅ Available from day one

| | Tool | What it adds | How it connects |
|---|---|---|---|
| ☸️ | **Kubernetes** | CrashLoops, OOMKills, Evictions, NodeNotReady, failed deploys | Python agent in your cluster |
| 🦊 | **GitLab CI/CD** | Broken pipelines, prod deploys, automatic rollbacks | Native webhook |
| 🐙 | **GitHub Actions** | Failed workflows, deploys, commit↔incident correlation | Native webhook |
| 📊 | **Prometheus + Grafana** | CPU, memory, latency, SLOs, Alertmanager | Native webhook |
| 🐕 | **Datadog** | APM, logs, synthetics, monitors | Native webhook |
| 🤖 | **Slack** | Enriched output + action button input | Bot API |
| 🟢 | **UptimeRobot** | Downed endpoints, degraded response times | Native webhook |

### 🔜 Phase 2 — On the roadmap

| | Tool | Status |
|---|---|---|
| 🔔 | **PagerDuty** | On-call history + incident correlation | Coming soon |
| 🔵 | **New Relic** | Alternative for teams migrating from Datadog | Coming soon |
| ☁️ | **AWS CloudWatch** | AWS infra, Lambda, RDS, ECS | Coming soon |
| 🔷 | **Azure Monitor** | Action Groups, App Insights | Coming soon |
| 🟠 | **Google Cloud Monitoring** | GKE, Cloud Run, BigQuery | Coming soon |
| 🪲 | **Sentry** | Code errors correlated with infra spikes | Coming soon |

> **Using something not listed?** [Open an Issue →](https://github.com/centinelai/docs/issues/new)

---

## 🏗️ Architecture

```
centinelai/
├── 🌐 app/          [PRIVATE]   Next.js 14 + Supabase — dashboard, API, billing
├── 🤖 agent/        [PUBLIC]    Python agent for Kubernetes — deploy in your cluster
├── ⚙️  infra/        [PRIVATE]   IaC, environment config, deploy scripts
└── 📚 docs/         [PUBLIC]    Documentation, integration guides, changelog
```

**Technology stack:**

```
Frontend    →  Next.js 14 (App Router + Server Components + Streaming)
Database    →  Supabase (PostgreSQL + pgvector + Realtime + multi-tenant RLS)
AI          →  Claude Haiku (bulk scoring/correlation) + Sonnet (synthesis)
Memory      →  pgvector — RAG over YOUR team's postmortem history
Workflows   →  Inngest — serverless event queue
Notif.      →  Slack Bot API + Resend (email)
Payments    →  Stripe
Deploy      →  Vercel (automatic CD)
```

---

## 📅 Roadmap

```
  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  PHASE 1 ████████░░░░░░░░░░░░░░  Weeks 1-2
  Technical foundation + K8s agent + GitLab + GitHub + dashboard

  PHASE 2 ░░░░░░░░████████░░░░░░  Weeks 3-4
  AI correlation + enriched Slack + Prometheus + Datadog
  Automatic postmortem + intelligent silencing

  PHASE 3 ░░░░░░░░░░░░░░░░██████  Weeks 5-6
  Onboarding < 10 min + Stripe + first paying customer
  UptimeRobot + New Relic + usage metrics

  PHASE 4 ░░░░░░░░░░░░░░░░░░░░░░  Month 2+
  Historical RAG + per-team custom scoring
  PagerDuty + AWS/Azure/GCP + public API + SSO
  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## 💶 Plans

<div align="center">

| | **Free** | **Team** ⭐ | **Pro** |
|---|:---:|:---:|:---:|
| **Price** | €0/month | €99/month | Custom pricing |
| Clusters / sources | 1 | 25 | Unlimited |
| Alerts/day | 500 | Unlimited | Unlimited |
| Connectors | 3 | All | All |
| AI correlation | ✓ | ✓ | ✓ |
| Auto postmortems | ✗ | ✓ | ✓ |
| RAG history | ✗ | 30 days | Unlimited |
| SSO / SAML | ✗ | ✗ | ✓ |
| SLA | ✗ | ✗ | 99.9% |
| Support | Community | Email | Dedicated |

*Gross margin > 85% from the first paying customer. Infra cost in beta: €0/month.*

</div>

---

## 🚀 Agent installation (2 minutes)

```bash
# 1. Apply the manifest (creates namespace, RBAC and agent)
kubectl apply -f https://centinelai.io/api/install/k8s/manifest.yaml

# 2. Create the secret with your token
kubectl create secret generic centinela-token \
  --from-literal=SENTINEL_TOKEN=<your-token-from-centinelai.io> \
  --from-literal=SENTINEL_API_URL=https://centinelai.io \
  -n centinela-system

# 3. Restart to pick up the secret
kubectl rollout restart deployment/centinela-agent -n centinela-system

# 4. Verify
kubectl get pods -n centinela-system
# centinela-agent-xxxx   1/1   Running   0   45s  ✓
```

For all other connectors (Datadog, GitLab, GitHub, Prometheus...) you just need to paste a webhook URL. No extra installations, no additional agents.

---

## 🎯 Who is centinelAI for

✅ **A great fit if...**
- Your team receives more than 100 alerts a day and has learned to ignore them
- You use Kubernetes, GitLab/GitHub or Datadog/Prometheus in production
- You have between 5 and 200 people on the technical team
- You pay > €500/month for enterprise observability tools but don't get full value
- Your on-call gets woken up by false alarms more than twice a week

❌ **Not for you if...**
- You have 0 alerts (you don't have enough monitoring — that's a different problem!)
- Your infra is purely on-premise with no webhook support
- You need very specific compliance before sending data outside the cluster

---

## 📊 The market

```
Spain + LATAM, 2026:

~4,800 companies with DevOps teams of 10+ people
~82% use Kubernetes in some production environment
~71% have active alert fatigue problems

Enterprise competitors (Datadog AIOps, New Relic AI):
→ Entry price: €500-800/month
→ Require adopting their entire stack
→ Out of reach for teams < 100 people

Opportunity window: 12-18 months
```

---

## 🤝 Open beta — 10 teams

We're looking for **10 DevOps teams** to test centinelAI in real production before launch.

**What we offer:**
- ✅ Free access for 3 months (Team plan)
- ✅ Direct influence on the roadmap
- ✅ Personalised onboarding with the founding team
- ✅ Published case study (if you want the visibility)

**Interested?** → [centinelai.io](https://centinelai.io) or reach out directly on LinkedIn

---

## 🛠️ Contributing

```bash
# Clone the relevant repo
git clone https://github.com/centinelai/<app|agent|infra|docs>

# Create your branch
git checkout -b feat/your-task-name

# Develop and open a PR against main
# Every task has its Issue in the GitHub Project
```

> `main` has branch protection active on all repos. No direct pushes.

---

<div align="center">

---

**centinelAI** · 2026

[🌐 Website](https://centinelai.io) · [💼 LinkedIn](https://linkedin.com/company/centinelai) · [📧 Contact](mailto:info@centinelai.io)

---

</div>
