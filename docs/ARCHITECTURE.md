# NiMa Connect — Architecture Overview

[← Project overview](../README.md) · [Case study →](CASE_STUDY.md)

This is a **simplified conceptual view** of the NiMa Connect integration approach, written for portfolio visitors. It is not an infrastructure diagram, deployment guide, network inventory, or complete description of the private implementation.

## User-facing workflow

~~~mermaid
flowchart TB
    U["Customer messages"] --> W["Messaging channel / integration"]
    W --> A["NiMa Connect application"]
    T["Business team"] <--> I["Shared Inbox / CRM interface"]
    I <--> A
    A <--> D[("Customer & conversation data")]
    A --> Q["Events / background processing"]
    Q --> X["Automation & configurable AI"]
    X --> A
~~~

## Major concerns

| Concern | Architectural approach |
| :--- | :--- |
| **Customer context** | Associate messaging activity with relevant CRM conversations and contacts. |
| **Asynchronous events** | Use event-based processing for work that should not block the user interface. |
| **Reliability** | Consider repeat delivery, message bursts, retries, and idempotent effects. |
| **Organization boundaries** | Respect organization-aware data and permission controls. |
| **Extensibility** | Keep external messaging and automation tools integrated through explicit interfaces. |
| **Observability** | Validate important application and integration paths in controlled environments. |

## Public technical stack

- **App and UI:** TypeScript, Next.js, React.
- **Data:** PostgreSQL and Supabase.
- **Messaging:** WhatsApp integration service, WAHA, webhooks.
- **Asynchronous components:** worker processes and Redis.
- **Environment:** Linux, Docker and reverse proxy.
- **Testing:** unit, integration and targeted end-to-end tests.

## Design boundaries

This diagram deliberately does **not** publish internal network names, service endpoints, infrastructure topology, credentials, customer data, access policies, or any details needed to operate the private deployment. It is intended to show problem-solving and engineering reasoning rather than reproduce sensitive configuration.

## Project provenance

NiMa Connect is adapted from the open-source [DeskcommCRM](https://github.com/melgarafael/DeskcommCRM) project. The architecture above represents the general solution approach, not an assertion that all components originated at NiMa.

---

[Contact NiMa](mailto:contato@nimaautomacao.com.br)
