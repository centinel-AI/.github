<div align="center">

<br/>

# ◢ GRAUSS

### **Despliega infraestructura con agentes de IA**

*Describe lo que quieres. Los agentes lo aprovisionan, lo vigilan y lo mantienen.*

<br/>

[![Beta](https://img.shields.io/badge/%E2%97%8F_Beta-Acceso_anticipado-059669?style=for-the-badge)](https://grauss.io)
[![Estado](https://img.shields.io/badge/En_construcci%C3%B3n-activa-10B981?style=for-the-badge)](#)

<br/>

> **Provisionar infra hoy es escribir Terraform, abrir PRs y rezar.**
> Grauss lo cambia: tú declaras la intención, **los agentes ejecutan el despliegue**
> y corrigen la deriva sin que toques un manifiesto.

<br/>

</div>

---

## Qué resuelve

| | Antes | Con Grauss |
|---|---|---|
| 🚀 **Desplegar** | Terraform a mano, PRs, revisión manual | Declaras la intención, el agente aplica |
| 🔁 **Mantener** | La infra deriva del IaC con el tiempo | Reconciliación continua hacia tu intención |
| 🩺 **Vigilar** | 847 alertas → ruido que se ignora | Correlación a 1 incidente con causa raíz |
| 💶 **Coste** | La factura sorprende a fin de mes | Coste atribuido y desvíos detectados al vuelo |

---

## Arquitectura

```
grauss/
├── 🧠 engine     orquestación — los agentes que planifican y aplican
├── ☸️  agent      se despliega en tu clúster Kubernetes y reporta estado
├── 🌐 portal     plataforma de cliente — defines intención, ves el estado
└── 🛰️  monitor    vigilancia con IA — deriva, incidentes y coste
```

```
Next.js 16  ·  Azure Postgres + pgvector  ·  Claude (planificación + síntesis) ·  Slack / email  ·  Stripe
```

Aislamiento por **proyecto**: cada proyecto tiene su cloud, sus conectores y su clave de IA (BYOK).

---

## Conectores

**Hoy** ☸️ Kubernetes · 🦊 GitLab CI/CD · 🐙 GitHub Actions · 📊 Prometheus/Grafana 

**Pronto** 🔔 PagerDuty · 🔵 New Relic · ☁️ CloudWatch · 🔷 Azure Monitor · 🟠 GCP · 🪲 Sentry · 🐕 Datadog · 🤖 Slack · 🟢 UptimeRobot

> Se conecta a lo que ya tienes. K8s con un agente; el resto, una URL de webhook.

---

## Beta · equipos piloto

Buscamos equipos de DevOps/SRE para pilotar Grauss en producción real.

Acceso anticipado · roadmap influenciable · onboarding con el equipo fundador.

**→ [grauss.io](https://grauss.io)**

---

<div align="center">

**Grauss** · 2026 · León, España 🇪🇸

[🌐 Web](https://grauss.io) · [💼 LinkedIn](https://linkedin.com/company/grauss) · [📧 Contacto](mailto:info@grauss.io)

*Tu infraestructura no duerme. Ahora tú sí.*

</div>
