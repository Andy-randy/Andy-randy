# Daria Lesnikova — AI Automation & Integration Engineer

I design reliable business workflows with n8n, AI/LLMs, APIs, CRM systems, and data tools.

My projects focus on the parts that make automation maintainable: data contracts, deterministic routing, controlled AI outputs, failure paths, operational visibility, testing, and handover-ready documentation.

**Flagship project: [AI Booking System](https://github.com/Andy-randy/ai-booking-system)** — nine connected n8n workflows for booking, rescheduling, cancellation, RAG FAQ, persistent conversations, and authorized administrator handoff.

[AI Booking System](https://github.com/Andy-randy/ai-booking-system) · [Portfolio](https://github.com/Andy-randy/n8n-portfolio) · [По-русски](#по-русски) · [Telegram](https://t.me/Andyyy_Randyyy)

## What I build

- Stateful booking and customer support workflows with persistent memory and administrator handoff
- AI-assisted lead qualification and request triage with validated model outputs
- API and webhook workflows with authentication, idempotency, and explicit responses
- RAG systems with separate ingestion and query boundaries
- CRM, Telegram, Gmail, Google Sheets, Notion, and external REST API integrations
- Scheduled monitoring, data normalization, operator alerts, and reporting
- Documentation and test scenarios that make workflow behavior reviewable

## Featured case studies

| Case study | Business use case | Engineering signal | Stack |
| --- | --- | --- | --- |
| [AI Booking System](https://github.com/Andy-randy/ai-booking-system) | Manage booking, rescheduling, cancellation, FAQ and administrator support | Nine workflows, persistent state, shared scheduling checks, authorized handoff and conditional rollback | n8n, Supabase / PostgreSQL, Groq, Gemini, Telegram |
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

**AI & data:** LLM agents, structured outputs, RAG, Groq, Gemini embeddings, Supabase / PostgreSQL / pgvector, Google Sheets

**Integrations:** REST APIs, CRM systems, Telegram Bot API, Gmail, Google Drive, Notion

**Code & tools:** JavaScript, SQL, JSON, Git, GitHub, Docker, VS Code

## Current focus / availability

Current focus: workflow orchestration, persistent state, failure recovery, and deployment.

Open to freelance automation projects and AI automation / integration roles.

Working languages: Russian and English.

## Contact

- Telegram: [@Andyyy_Randyyy](https://t.me/Andyyy_Randyyy)
- GitHub: [Andy-randy](https://github.com/Andy-randy)
- Portfolio: [n8n-portfolio](https://github.com/Andy-randy/n8n-portfolio)

---

## По-русски

Я проектирую бизнес-процессы на базе n8n, AI/LLM, API, CRM и систем хранения данных. Основной фокус — явные контракты, детерминированная маршрутизация, постоянное состояние, обработка отказов и документация для передачи проекта.

**Основной проект — [AI Booking System](https://github.com/Andy-randy/ai-booking-system)**: девять связанных workflow для записи, переноса, отмены, RAG FAQ и передачи диалога администратору. В проекте реализованы постоянное состояние, общий сервис расписания, проверка прав администратора и условный rollback при ошибке уведомления. [Русская документация](https://github.com/Andy-randy/ai-booking-system/blob/main/README.ru.md).

Другие кейсы: Barbershop Booking API, RAG Telegram FAQ Bot, AI Lead Processing Pipeline и Competitor Price Monitoring. Каталог [n8n-portfolio](https://github.com/Andy-randy/n8n-portfolio) объединяет ссылки на проекты; в их README есть схемы, экспорты, тестовые сценарии и известные ограничения.

Открыта к freelance-проектам по автоматизации и ролям в AI automation / integration. Связаться можно через [Telegram](https://t.me/Andyyy_Randyyy).
