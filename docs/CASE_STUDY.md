# Case Study — NiMa Connect

**Category:** CRM customization, business automation, customer communications  
**Role:** NiMa Automação e Tecnologia — application adaptation, integration, quality assurance, and environment engineering  
**Stage:** Active development and validation (October 2026)

[← Project overview](../README.md) · [Architecture →](ARCHITECTURE.md)

## Business problem

Many teams work with customer conversations, contacts, lead stages, follow-ups, and messaging automation across multiple tools. Context becomes fragmented, and a single customer interaction may require several manual steps to understand and continue.

The objective behind NiMa Connect is to bring those workflows closer together in a cohesive CRM environment while keeping the flexibility to integrate third-party services.

## Solution approach

Rather than claiming a CRM built entirely from scratch, NiMa Connect extends and adapts the open-source [DeskcommCRM](https://github.com/melgarafael/DeskcommCRM) foundation.

NiMa's work centers on:

1. **Making workflows usable:** tailoring CRM navigation, contacts, conversation views, and customer support flows to day-to-day requirements.
2. **Connecting channels:** integrating WhatsApp messaging and event/webhook processing with CRM context.
3. **Adapting organization controls:** supporting organization-aware settings, permissions, and configurable modules.
4. **Strengthening reliability:** validating background processing, messaging behavior, and regression cases.
5. **Operating environments:** running the platform and integrations in containerized development and homologation environments.

## Functional areas

| Area | What the project addresses | Status context |
| :--- | :--- | :--- |
| **Inbox and conversations** | Centralized interaction and conversation workflows. | Core interaction flows exercised in homologation. |
| **Contacts and customer activity** | Contact views, creation flows, and event timelines. | Core flows exercised; further UX validation continues. |
| **Sales pipeline** | Lead stages and follow-up visibility. | Pipeline views reviewed during validation. |
| **WhatsApp connection** | Messaging channel integration and webhook flow. | Connected channel and basic connectivity validated in homologation. |
| **Automation and AI** | Automated processing and AI-assisted CRM operations. | Implemented capabilities subject to configuration and ongoing tests. |
| **Multi-organization controls** | Per-organization module configuration and security-oriented access patterns. | Relevant changes integrated into the private main branch. |
| **Listening channel** | Optional employee-feedback / reporting module with privacy-oriented workflow. | Code integrated and locally tested; not claimed as publicly deployed. |

The status descriptions are intentionally specific: **local testing, integration into main, homologation, and production release are different milestones**.

## Engineering decisions

### Messaging must be dependable

A messaging-based CRM needs predictable processing when customers send multiple messages close together. The project includes work to keep turn context bounded, handle bursts of incoming events, and avoid resending replies after a downstream checkpoint failure.

**Engineering emphasis:** idempotency, event ordering, failure recovery, and regression testing.

### Configuration varies by organization

Different businesses may require different modules and workflow rules. Organization-aware design supports selective availability of modules, access controls, and administrative boundaries without creating a separate product for every customer.

**Engineering emphasis:** consistent organization identity, permission checks, and controlled settings changes.

### Integrations are part of the product

The CRM integrates with external messaging services and related processing components. That requires coordinating application routes, webhooks, workers, databases, and operations.

**Engineering emphasis:** connection diagnosis, environment configuration, and end-to-end validation.

## Technology overview

| Layer | Stack |
| :--- | :--- |
| Frontend and application | TypeScript, React, Next.js |
| Data | PostgreSQL, Supabase |
| Messaging integration | WhatsApp integration service (WAHA), webhooks |
| Asynchronous services | Background workers, Redis |
| Delivery environment | Linux, Docker, reverse proxy |
| Quality | Type checking, targeted regression tests, E2E tests |

See the [architecture overview](ARCHITECTURE.md) for a simplified conceptual diagram.

## Scope of my work

My contribution through NiMa includes product configuration and customization, integration work, technical diagnosis, regression validation, infrastructure setup, and the evolution of application-specific modules.

This is a real engineering and integration project, but it would be inaccurate to claim original authorship of every existing feature inherited from the upstream CRM. The original project's contributors retain credit for the open-source foundation.

## Outcomes and evidence

- CRM interface and customer-communication workflows have been reviewed in a real homologation environment.
- A WhatsApp integration was connected and tested.
- Organization-level module management and specific messaging-reliability changes were integrated into the private source's main branch.
- The listening-channel development phase was integrated following local automated and browser-based tests.
- Application and supporting services were validated in a containerized environment.

**No numerical increase in revenue, reduction in support time, customer adoption metric, or production deployment claim is made here without verifiable evidence.**

## What this public case study does not include

- Source code from the private commercial adaptation.
- Client conversations, personal data, customer records, or credentials.
- Server addresses, account details, deployment secrets, or internal security configurations.
- A publicly accessible test account.
- Unverified sales figures or performance metrics.

A portfolio can demonstrate technical competence without publishing a customer's private information.

## Next showcase improvements

A small set of **real, sanitized** screenshots may be published in a future revision: a redacted CRM overview, an anonymized Inbox view, and a sample sales pipeline or module settings screen. Screenshots must be approved before publication.

See [screenshot guidelines](SCREENSHOTS.md).

---

### Let's discuss your project

**[NiMa Automação e Tecnologia](https://www.nimaautomacao.com.br)** · [contato@nimaautomacao.com.br](mailto:contato@nimaautomacao.com.br) · [@nivcam](https://github.com/nivcam)
