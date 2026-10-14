<div align="center">

<img src="https://avatars.githubusercontent.com/u/28583638?v=4" alt="NiMa Automação e Tecnologia" width="108" />

# NiMa Connect

### Customer conversations. Sales workflows. Business automation.

**A customizable CRM experience built around messaging, team workflows, and practical integrations.**

[![Portfolio Showcase](https://img.shields.io/badge/Portfolio-Public_Showcase-00A4BA?style=flat-square)](https://github.com/nivcam)
![Source Code](https://img.shields.io/badge/Source_Code-Private-26344A?style=flat-square)
![Status](https://img.shields.io/badge/Status-Active_Development_%26_Validation-F59E0B?style=flat-square)

[**Explore the case study**](docs/CASE_STUDY.md) · [**Architecture overview**](docs/ARCHITECTURE.md) · [**Contact NiMa**](https://www.nimaautomacao.com.br)

</div>

---

## The idea

Business conversations don't happen in isolation. A customer messages the team, a lead needs follow-up, information needs to move between tools, and everyone needs to understand what happened next.

**NiMa Connect** brings these activities together through a CRM foundation adapted for business communications, sales processes, and automation. It is designed for teams that want more context and fewer disconnected manual steps.

> **Portfolio notice:** This is a public product and engineering showcase, **not a source-code distribution, live demo, or production availability announcement**. The application itself is maintained in a private repository.

## What it brings together

| Capability | Business value |
| :--- | :--- |
| 💬 **Shared Inbox** | Organize customer conversations and their history in a common workspace. |
| 👥 **Contacts and customer context** | Keep customer records and conversation activity connected. |
| 📊 **Sales pipeline** | Provide a structured view of leads, stages, and follow-up work. |
| 🔗 **WhatsApp integration** | Connect messaging flows with CRM operations through integrations and webhooks. |
| ⚙️ **Automation** | Use events, background workers, and integrations to reduce repetitive work. |
| 🤖 **AI-assisted workflows** | Explore configurable AI features alongside human customer service. |
| 🏢 **Organization-aware configuration** | Support organization-specific modules and access controls. |

**Availability note:** Capabilities are at different stages of development and validation; some require integration setup and some are not yet deployed for general use.

## At a glance

<div align="center">

**Messaging** → **CRM context** → **Team actions** → **Automation**

</div>

~~~mermaid
flowchart LR
    A["Customer / WhatsApp"] --> B["Messaging integration"]
    B --> C["NiMa Connect CRM"]
    C <--> D[("Customer & sales data")]
    C --> E["Events and automation"]
    E --> C
    C --> F["Team Inbox & sales workflows"]
~~~

*Conceptual overview only. Real infrastructure and customer environments are intentionally omitted.*

## Technology stack

| Area | Technologies |
| :--- | :--- |
| **Web application** | TypeScript, Next.js, React |
| **Data and access** | PostgreSQL, Supabase |
| **Messaging** | WhatsApp integrations, WAHA, webhooks |
| **Services** | REST APIs, background workers, Redis |
| **Hosting / deployment** | Linux, Docker, reverse proxy |
| **Engineering quality** | Git, GitHub, automated testing, E2E validation |

## Engineering work highlighted

**Business-focused CRM customization.** Adapting the product to organizational workflows, navigation, permissions, and module requirements.

**Event-driven integration.** Connecting inbound events and CRM processing while considering reliability, ordering, and duplicate-response prevention.

**Organization-aware design.** Working with tenant isolation, role-based access, and administrative governance patterns.

**Hands-on delivery.** Running and validating a containerized environment with application, worker, messaging, and supporting services.

Read the [**detailed case study**](docs/CASE_STUDY.md) for the problem, design choices, work performed, and validation boundaries.

## Gallery

Real, approved product screenshots can be added here after removing names, phone numbers, messages, tokens, customer data, and internal infrastructure details.

**No mock interface is presented as a real product screenshot.** See [screenshot publication guidelines](docs/SCREENSHOTS.md).

## Project background and attribution

NiMa Connect builds on the open-source **[DeskcommCRM](https://github.com/melgarafael/DeskcommCRM)** foundation. This showcase focuses on NiMa's customization, integration, engineering, testing, and deployment work; it **does not claim authorship of the entire original CRM**.

Product code, commercial adaptations, customer configurations, and internal infrastructure remain private. This showcase contains documentation only and does not grant a license to the private application.

## Have a similar project?

NiMa Automação e Tecnologia works with CRM customization, application integrations, workflow automation, data, and business systems.

**[Visit NiMa](https://www.nimaautomacao.com.br)** · **[Email us](mailto:contato@nimaautomacao.com.br)** · **[GitHub portfolio](https://github.com/nivcam)**

<sub>NiMa Automação e Tecnologia · Portfolio case study · October 2026</sub>
