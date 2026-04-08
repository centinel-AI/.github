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

### *Tu infraestructura nunca duerme. Ahora tú sí puedes.*

<br/>

[![Beta Abierta](https://img.shields.io/badge/🚀_Beta-Únete_gratis-6C63FF?style=for-the-badge)](https://centinelai.io)
[![Estado](https://img.shields.io/badge/Estado-En_construcción_activa-F59E0B?style=for-the-badge)](#roadmap)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Síguenos-0A66C2?style=for-the-badge&logo=linkedin)](https://linkedin.com/company/centinelai)

<br/>

> **¿Cuántas alertas recibió tu equipo ayer?**
> ¿Cuántas importaban de verdad?

<br/>

</div>

---

## 🔥 El problema que nadie resuelve (todavía)

<table>
<tr>
<td width="50%">

### Sin centinelAI

```
🔴 ALERT: CPU > 80% en prod-api-01
🔴 ALERT: CPU > 80% en prod-api-01
🔴 ALERT: CPU > 80% en prod-api-01
🟡 WARN:  Latencia p99 elevada
🔴 ALERT: CPU > 80% en prod-api-02
📧 EMAIL: Pipeline fallido en staging
🔴 ALERT: CPU > 80% en prod-api-01
💬 SLACK: "oye alguien mira esto?"
🔴 ALERT: Memory usage > 90%
📟 PAGER: On-call despertado a las 3am
🔴 ALERT: CPU > 80% en prod-api-03
💬 SLACK: "lo veo, era un falso positivo"
🔴 ALERT: CPU > 80% en prod-api-01
...x847 más esta noche
```

❌ El equipo aprende a ignorarlas  
❌ La alerta real se pierde entre el ruido  
❌ El cliente detecta el fallo antes que tú

</td>
<td width="50%">

### Con centinelAI

```
🟣 [centinelAI] INCIDENTE REAL — 03:47

   Servicio: prod-api (3 réplicas)
   Causa raíz: OOMKilled tras deploy
   de las 03:30 (rama: feat/image-resize)
   Autor: @carlos

   Impacto: latencia p99 +340ms
   Afectados: ~120 usuarios activos

   ▶ Sugerencia: rollback a v2.4.1
   ▶ kubectl rollout undo deployment/api

   Postmortem generado automáticamente.
```

✅ 1 notificación, no 847  
✅ Causa raíz identificada al instante  
✅ Tu equipo duerme. Los usuarios también.

</td>
</tr>
</table>

---

## ⚡ Qué hace centinelAI

<div align="center">

```
                    TODO LO QUE GENERA RUIDO EN TU STACK
                              │
         ┌────────────────────┼────────────────────┐
         ▼                    ▼                    ▼
   [Kubernetes]         [Datadog / NR]        [GitHub / GitLab]
   [Prometheus]         [Grafana]             [PagerDuty]
   [UptimeRobot]        [Alertmanager]        [Slack entrante]
         │                    │                    │
         └────────────────────┼────────────────────┘
                              │
                              ▼
              ┌───────────────────────────────┐
              │      PIPELINE DE 4 AGENTES IA  │
              │                               │
              │  ➊ DEDUPLICADOR               │
              │     Elimina el ruido repetido  │
              │     847 alertas → 23 únicas    │
              │              │                │
              │  ➋ SCORER (Claude Haiku)      │
              │     Puntúa cada alerta 0-100   │
              │     23 únicas → 8 relevantes   │
              │              │                │
              │  ➌ CORRELADOR (Claude Haiku)  │
              │     Conecta señales entre sí   │
              │     8 relevantes → 2 causas    │
              │              │                │
              │  ➍ NOTIFICADOR (Claude Sonnet) │
              │     Genera contexto accionable │
              │     2 causas → 1 que importa   │
              └───────────────────────────────┘
                              │
                              ▼  solo si score > 70
              ┌───────────────────────────────┐
              │   TU EQUIPO — cuando importa  │
              │   Slack · Email · Dashboard   │
              └───────────────────────────────┘
```

</div>

---

## 🔌 Conectores — Habla el idioma de tu stack

> centinelAI no te pide que cambies tus herramientas. Se conecta a lo que ya tienes.

### ✅ MVP — Disponibles desde el día 1

| | Herramienta | Qué aporta | Cómo se conecta |
|---|---|---|---|
| ☸️ | **Kubernetes** | CrashLoops, OOMKills, Evictions, NodeNotReady, deploys fallidos | Agente Python en tu cluster |
| 🦊 | **GitLab CI/CD** | Pipelines rotos, deploys a prod, rollbacks automáticos | Webhook nativo |
| 🐙 | **GitHub Actions** | Workflows fallidos, deploys, correlación commit↔incidente | Webhook nativo |
| 📊 | **Prometheus + Grafana** | CPU, memoria, latencia, SLOs, Alertmanager | Webhook nativo |
| 🐕 | **Datadog** | APM, logs, synthetics, monitors | Webhook nativo |
| 🤖 | **Slack** | Salida enriquecida + entrada con botones de acción | Bot API |
| 🟢 | **UptimeRobot** | Endpoints caídos, tiempo de respuesta degradado | Webhook nativo |

### 🔜 Fase 2 — En el roadmap

| | Herramienta | Estado |
|---|---|---|
| 🔔 | **PagerDuty** | Historial de on-call + correlación de incidentes | Próximamente |
| 🔵 | **New Relic** | Alternativa a Datadog para equipos que migran | Próximamente |
| ☁️ | **AWS CloudWatch** | Infra en AWS, Lambda, RDS, ECS | Próximamente |
| 🔷 | **Azure Monitor** | Action Groups, App Insights | Próximamente |
| 🟠 | **Google Cloud Monitoring** | GKE, Cloud Run, BigQuery | Próximamente |
| 🪲 | **Sentry** | Errores de código que se correlacionan con picos de infra | Próximamente |

> **¿Usas algo que no está aquí?** [Abre un Issue →](https://github.com/centinelai/docs/issues/new)

---

## 🏗️ Arquitectura

```
centinelai/
├── 🌐 app/          [PRIVADO]  Next.js 14 + Supabase — dashboard, API, billing
├── 🤖 agent/        [PÚBLICO]  Agente Python para Kubernetes — instálalo en tu cluster
├── ⚙️  infra/        [PRIVADO]  IaC, configuración de entornos, scripts de deploy
└── 📚 docs/         [PÚBLICO]  Documentación, guías de integración, changelog
```

**Stack tecnológico:**

```
Frontend    →  Next.js 14 (App Router + Server Components + Streaming)
Base datos  →  Supabase (PostgreSQL + pgvector + Realtime + RLS multi-tenant)
IA          →  Claude Haiku (scoring/correlación masiva) + Sonnet (síntesis)
Memoria     →  pgvector — RAG sobre historial de postmortems de TU equipo
Workflows   →  Inngest — cola de eventos serverless
Notif.      →  Slack Bot API + Resend (email)
Pagos       →  Stripe
Deploy      →  Vercel (CD automático)
```

---

## 📅 Roadmap

```
  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  FASE 1 ████████░░░░░░░░░░░░░░  Semanas 1-2
  Base técnica + agente K8s + GitLab + GitHub + dashboard

  FASE 2 ░░░░░░░░████████░░░░░░  Semanas 3-4
  Correlación IA + Slack enriquecido + Prometheus + Datadog
  Postmortem automático + silenciamiento inteligente

  FASE 3 ░░░░░░░░░░░░░░░░██████  Semanas 5-6
  Onboarding < 10 min + Stripe + primer cliente de pago
  UptimeRobot + New Relic + métricas de uso

  FASE 4 ░░░░░░░░░░░░░░░░░░░░░░  Mes 2+
  RAG histórico + scoring personalizado por equipo
  PagerDuty + AWS/Azure/GCP + API pública + SSO
  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## 💶 Planes

<div align="center">

| | **Free** | **Team** ⭐ | **Pro** |
|---|:---:|:---:|:---:|
| **Precio** | 0 €/mes | 149 €/mes | 349 €/mes |
| Clusters / fuentes | 1 | 5 | Ilimitadas |
| Alertas/día | 500 | 10.000 | Ilimitadas |
| Conectores | 3 | Todos | Todos |
| Correlación IA | ✓ | ✓ | ✓ |
| Postmortems auto | ✗ | ✓ | ✓ |
| Historial RAG | ✗ | 30 días | Ilimitado |
| SSO / SAML | ✗ | ✗ | ✓ |
| SLA | ✗ | ✗ | 99,9% |
| Soporte | Community | Email | Dedicado |

*Margen bruto > 85% desde el primer cliente de pago. Coste de infra en beta: 0 €/mes.*

</div>

---

## 🚀 Instalación del agente (en 2 minutos)

```bash
# 1. Crear el secreto con tu token
kubectl create secret generic centinela-token \
  --from-literal=SENTINEL_TOKEN=<tu-token-de-centinelai.io> \
  --from-literal=SENTINEL_API_URL=https://centinelai.io/api \
  -n centinela-system --create-namespace

# 2. Instalar el agente en tu cluster
kubectl apply -f https://centinelai.io/install/k8s/manifest.yaml

# 3. Verificar
kubectl get pods -n centinela-system
# centinela-agent-xxxx   1/1   Running   0   45s  ✓
```

**Para el resto de conectores** (Datadog, GitLab, GitHub, Prometheus...) solo necesitas pegar una URL de webhook. Sin instalaciones, sin agentes adicionales.

---

## 🎯 Para quién es centinelAI

✅ **Encaja perfectamente si...**
- Tu equipo recibe más de 100 alertas al día y ha aprendido a ignorarlas
- Usas Kubernetes, GitLab/GitHub o Datadog/Prometheus en producción
- Tienes entre 5 y 200 personas en el equipo técnico
- Pagas > 500 €/mes en herramientas de observabilidad enterprise pero no las aprovechas al máximo
- Tu on-call se despierta por falsas alarmas más de 2 veces por semana

❌ **No es para ti si...**
- Tienes 0 alertas (¡no tienes monitorización suficiente, ese es otro problema!)
- Tu infra es puramente on-premise sin webhooks
- Necesitas compliance muy específico antes de enviar datos fuera del cluster

---

## 📊 El mercado

```
España, 2026:

~4.800 empresas con equipos DevOps de +10 personas
~82% usan Kubernetes en algún entorno de producción
~71% tienen problemas activos de fatiga de alertas

Competidores enterprise (Datadog AIOps, New Relic AI):
→ Precio de entrada: 500-800 €/mes
→ Requieren adoptar todo su stack
→ Inaccesibles para equipos < 100 personas

Ventana de oportunidad: 12-18 meses
```

---

## 🤝 Beta cerrada — 10 equipos en España

Estamos buscando **10 equipos DevOps** para probar centinelAI en producción real antes del lanzamiento.

**A cambio ofrecemos:**
- ✅ Acceso gratuito durante 3 meses (plan Team)
- ✅ Influencia directa en el roadmap
- ✅ Onboarding personalizado con el equipo fundador
- ✅ Caso de éxito publicado (si quieres visibilidad)

**¿Te interesa?** → [centinelai.io](https://centinelai.io) o escríbenos directamente en LinkedIn

---

## 🛠️ Para el equipo — Contribuir

```bash
# Clona el repo correspondiente
git clone https://github.com/centinelai/<app|agent|infra|docs>

# Crea tu rama
git checkout -b feat/nombre-de-la-tarea

# Desarrolla y abre PR hacia main
# Toda tarea tiene su Issue en el GitHub Project
```

> `main` tiene protección activa en todos los repos. No se hace push directo.

---

<div align="center">

---

**centinelAI** · 2026

[🌐 Web](https://centinelai.io) · [💼 LinkedIn](https://linkedin.com/company/centinelai) · [📧 Beta](mailto:hola@centinelai.io)

---

</div>

