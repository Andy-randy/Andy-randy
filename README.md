# Daria Lesnikova — AI Automation & Integration Engineer

I design reliable business workflows with n8n, AI/LLMs, APIs, CRM systems, and data tools.

My projects focus on the parts that make automation maintainable: data contracts, deterministic routing, controlled AI outputs, failure paths, operational visibility, testing, and handover-ready documentation.

[Portfolio](https://github.com/Andy-randy/n8n-portfolio) · [Русское резюме](#по-русски) · [Telegram](https://t.me/Andyyy_Randyyy)

## What I build

- AI-assisted lead qualification and request triage with validated model outputs
- API and webhook workflows with authentication, idempotency, and explicit responses
- RAG systems with separate ingestion and query boundaries
- CRM, Telegram, Gmail, Google Sheets, Notion, and external REST API integrations
- Scheduled monitoring, data normalization, operator alerts, and reporting
- Documentation and test scenarios that make workflow behavior reviewable

## Featured case studies

| Case study | Business use case | Engineering signal | Stack |
| --- | --- | --- | --- |
| [Barbershop Booking API](https://github.com/Andy-randy/barbershop-booking-api) | Validate, store, deduplicate, and notify on bookings | Modular workflows, practical idempotency, async notifications, centralized errors | n8n, Webhooks, Google Sheets, Telegram, Gmail |
| [RAG Telegram FAQ Bot](https://github.com/Andy-randy/rag-telegram-faq-bot) | Answer support questions from a controlled knowledge base | Separate ingestion/query paths and explicit retrieval limitations | n8n, Supabase, pgvector, Hugging Face, Groq, Telegram |
| [AI Lead Processing Pipeline](https://github.com/Andy-randy/ai-lead-processing-pipeline) | Qualify and route inbound sales leads | Validation before AI, parsed model contract, deterministic routing | n8n, Groq, CRM API, Telegram, Gmail, Google Sheets |
| [Competitor Price Monitoring](https://github.com/Andy-randy/n8n-portfolio/tree/main/05-competitor-price-monitoring) | Detect changes on public product pages | Deterministic comparison, explicit extraction failures, AI-only enrichment | n8n, JavaScript, Groq, Google Sheets, Telegram |

The complete project index, exports, examples, screenshots, test scenarios, and limitations are in the [n8n Automation & Integration Portfolio](https://github.com/Andy-randy/n8n-portfolio).

## Engineering approach

```text
Business process
→ boundaries and data contracts
→ deterministic workflow + selective AI
→ validation and failure paths
→ observability and testing
→ handover-ready documentation
```

I use AI where semantic judgment adds value and keep validation, permissions, routing, and state transitions deterministic whenever possible.

I treat a successful demo as the beginning of review: retries, idempotency, partial failures, concurrency, personal-data handling, and deployment constraints still need explicit decisions.

## Core stack

**Automation:** n8n, webhooks, scheduled workflows, sub-workflows, Error Workflows

**AI & data:** LLM agents, structured outputs, RAG, embeddings, Supabase / pgvector, Google Sheets

**Integrations:** REST APIs, CRM systems, Telegram Bot API, Gmail, Google Drive, Notion

**Code & tools:** JavaScript, JSON, Git, GitHub, Docker, VS Code

## Current focus / availability

Current focus: orchestration, state, memory, reliable tool use, and production deployment.

Open to freelance automation projects and AI automation / integration roles.

Working languages: Russian and English.

## Contact

- Telegram: [@Andyyy_Randyyy](https://t.me/Andyyy_Randyyy)
- GitHub: [Andy-randy](https://github.com/Andy-randy)
- Portfolio: [n8n-portfolio](https://github.com/Andy-randy/n8n-portfolio)

---

## По-русски

Я проектирую надёжные бизнес-процессы на базе n8n, AI/LLM, API, CRM и систем хранения данных. Основной фокус — не отдельный «бот», а весь рабочий контур: входные данные, границы компонентов, маршрутизация, ошибки, наблюдаемость и передача проекта.

В портфолио лучше начать с Barbershop Booking API, RAG Telegram FAQ Bot, AI Lead Processing Pipeline и Competitor Price Monitoring. В README проектов есть схемы, workflow exports, примеры контрактов, тестовые сценарии, известные ограничения и план production hardening.

Открыта к freelance-проектам по автоматизации и ролям в AI automation / integration. Связаться можно через [Telegram](https://t.me/Andyyy_Randyyy).
