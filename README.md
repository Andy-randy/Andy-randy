# Daria Lesnikova · n8n Automation Specialist

**n8n Automation Specialist · LLM Workflows · AI Agents**

I build practical automation workflows that reduce manual work: lead routing, AI-assisted customer communication, data parsing, CRM updates, notifications, and structured reporting.

[🇷🇺 По-русски](#-по-русски) · [🇬🇧 In English](#-in-english)

---

## 🇷🇺 По-русски

### Кто я

Я развиваюсь как специалист по автоматизации на базе **n8n, LLM и API-интеграций**.

Мой фокус — не «бот ради бота», а рабочие процессы для бизнеса:

- обработка входящих заявок;
- AI-квалификация лидов;
- Telegram- и email-уведомления;
- интеграции с CRM, Google Sheets, Notion и внешними API;
- парсинг, мониторинг цен и нормализация данных;
- workflow-документация, чтобы проект можно было передать другому человеку.

Основной репозиторий с проектами: [`n8n-portfolio`](https://github.com/Andy-randy/n8n-portfolio)

**Сейчас:** открыта к freelance-задачам и junior / junior+ позициям в automation / workflow engineering.  
**В фокусе роста:** RAG, Supabase / vector DB, Docker, production deployment, прикладной Python.  
**Языки:** русский, английский.

---

## Избранные проекты

### 🤖 RAG Telegram FAQ Bot

**Задача:** создать Telegram-бота, который отвечает на вопросы пользователей на основе собственной базы знаний.

**Как работает:**

```text
Telegram Trigger
→ Switch (/start)
├── Start → Welcome Message
└── Question
    → AI Agent
    → Supabase Vector Store
    → Groq LLM
    → Telegram Response
    → Google Sheets Logging
```

**Что важно:**

- Используется Retrieval-Augmented Generation (RAG).
- Документы загружаются из PDF в Supabase Vector Store.
- AI Agent отвечает только на основе найденных фрагментов.
- Все вопросы и ответы сохраняются в Google Sheets.
- Реализовано onboarding-сообщение по команде `/start`.

**Стек:** `n8n` · `Telegram Bot API` · `Supabase` · `pgvector` · `Hugging Face Embeddings` · `Groq` · `Google Drive` · `Google Sheets`

[📂 Открыть проект](https://github.com/Andy-randy/n8n-portfolio/tree/main/04-rag-telegram-faq-bot)

---

### 📉 Мониторинг цен конкурентов

**Задача:** автоматически отслеживать цены конкурентов и быстро получать уведомления об изменениях.

**Как работает:**

```text
Schedule Trigger
→ Competitors list
→ HTML parsing + custom price enrichment
→ Google Sheets history
→ Price comparison
→ Telegram daily report / AI price alert
```

**Что важно:**

- Workflow собирает товары с нескольких e-commerce сайтов.
- Для сайта со скрытыми ценами используется отдельный JSON-запрос.
- Цены нормализуются и сравниваются с историей в Google Sheets.
- Telegram получает ежедневный отчёт и отдельные alert-сообщения.
- AI Agent кратко объясняет изменение цены.

**Стек:** `n8n` · `JavaScript` · `Google Sheets` · `Telegram Bot API` · `Groq`

[📂 Открыть проект](https://github.com/Andy-randy/n8n-portfolio/tree/main/05-competitor-price-%26-offer-monitoring-system)

---

### 🤖 AI-ассистент, который сам закрывает заказы

**Задача:** автоматизировать общение с клиентом от первого сообщения до подтверждения заказа.

**Как работает:**

```text
Telegram Trigger
→ AI Agent + Simple Memory
→ проверка готовности к заказу
→ Google Sheets
→ Telegram-уведомление менеджеру
```

**Что важно:**

- AI Agent ведёт диалог и собирает данные клиента.
- Simple Memory хранит контекст разговора.
- LLM сама определяет, когда данных достаточно для оформления заказа.
- Менеджер получает уже структурированную заявку, а не сырую переписку.

**Стек:** `n8n` · `Groq` · `Telegram Bot API` · `Google Sheets`

---

### 🎯 Воронка лидов с LLM-классификатором

**Задача:** автоматически разделять входящие заявки на холодные, тёплые и горячие.

**Как работает:**

```text
Webhook
→ AI Agent
→ Code node
→ Switch
├── холодный лид → email + Google Sheets
├── тёплый лид → email + Google Sheets
├── горячий лид → Telegram manager ping + Bitrix24 CRM
└── fallback → Telegram error notification
```

**Что важно:**

- AI Agent анализирует заявку по смыслу, а не по ключевым словам.
- Code node чистит и парсит JSON-ответ модели.
- Из текста заявки извлекается бюджет.
- Для горячего лида создаётся сделка в Bitrix24 через REST API.
- Ошибки AI-формата уходят в fallback-ветку.

**Стек:** `n8n` · `Groq` · `Webhook` · `JavaScript` · `Gmail` · `Telegram` · `Google Sheets` · `Bitrix24 REST API`

---

### 🔍 Умный парсер вакансий с LLM-скорингом

**Задача:** сократить ручную фильтрацию вакансий и оставлять только релевантные варианты.

**Как работает:**

```text
Schedule / Manual Trigger
→ HH.ru API
→ JavaScript normalization
→ Loop Over Items
→ AI scoring
→ IF filter
→ Telegram digest
```

**Что важно:**

- Детерминированная логика проверяет объективные условия: зарплата, формат работы.
- LLM оценивает смысловую релевантность вакансии.
- Результаты собираются в Telegram-дайджест.
- Неподходящие вакансии тоже логируются отдельно, чтобы ничего не терялось.

**Стек:** `n8n` · `Groq` · `HH.ru API` · `Telegram Bot API` · `JavaScript`

---

## Дополнительные проекты

В портфолио также есть:

- RSS / news digest automation;
- e-commerce order processing;
- HR onboarding workflow;
- financial monitoring;
- AI content repurposing;
- customer support routing;
- Notion API automations.

---

## Технический стек

**Automation:** `n8n` · Webhook · Schedule Trigger · Switch · IF · Loop · Aggregate · Error handling  
**AI / LLM:** `Groq` · AI Agent · Simple Memory · RAG · structured JSON output · prompt engineering  
**Integrations:** `Telegram Bot API` · `Gmail` · `Google Sheets` · `Bitrix24 REST API` · `Notion API` · `HH.ru API` · `Supabase`  
**Code:** `JavaScript` для Code node · базовый `Python` · REST API · JSON  
**Tools:** `Git` · `GitHub` · `Docker` · `VS Code`

---

## Как я подхожу к автоматизации

1. Сначала разбираю бизнес-процесс: где теряется время, где ручной труд, где ошибки.
2. Рисую схему workflow: входные данные, ветки, интеграции, fallback.
3. Собираю MVP и проверяю на тестовых данных.
4. Добавляю обработку ошибок, логирование и понятные названия нод.
5. Документирую проект: README, пример входных данных, workflow export, скрин архитектуры.

---

## Контакты

- Telegram: [@Andyyy_Randyyy](https://t.me/Andyyy_Randyyy)
- GitHub: [Andy-randy](https://github.com/Andy-randy)
- Workflow portfolio: [n8n-portfolio](https://github.com/Andy-randy/n8n-portfolio)

---

## 🇬🇧 In English

### About me

I am developing as an automation specialist focused on **n8n, LLM workflows, and API integrations**.

My focus is not “a bot for the sake of a bot”, but practical business automation.

Main project repository: [`n8n-portfolio`](https://github.com/Andy-randy/n8n-portfolio)

**Currently:** open to freelance tasks and junior / junior+ automation or workflow engineering roles.  
**Growing into:** RAG, Supabase / vector DBs, Docker, production deployment, practical Python.  
**Languages:** Russian, English.

---

## Selected Projects

### 🤖 RAG Telegram FAQ Bot

**Goal:** build a Telegram bot that answers questions using a custom knowledge base.

**Workflow:**

```text
Telegram Trigger
→ Switch (/start)
├── Welcome Message
└── User Question
    → AI Agent
    → Supabase Vector Store
    → Groq LLM
    → Telegram Response
    → Google Sheets Logging
```

**Key points:**

- Uses Retrieval-Augmented Generation (RAG).
- PDF documents are embedded and stored in Supabase Vector Store.
- The AI Agent answers only using retrieved context.
- All questions and answers are logged to Google Sheets.
- Includes a `/start` onboarding flow.

**Stack:** `n8n` · `Telegram Bot API` · `Supabase` · `pgvector` · `Hugging Face Embeddings` · `Groq` · `Google Drive` · `Google Sheets`

[📂 Open Project](https://github.com/Andy-randy/n8n-portfolio/tree/main/04-rag-telegram-faq-bot)

---

### 📉 Competitor Price Monitoring

**Goal:** automatically monitor competitor prices and receive alerts when prices change.

**Workflow:**

```text
Schedule Trigger
→ Competitors list
→ HTML parsing + custom price enrichment
→ Google Sheets history
→ Price comparison
→ Telegram daily report / AI price alert
```

**Key points:**

- The workflow collects products from multiple e-commerce websites.
- A custom JSON request handles a website with hidden prices.
- Prices are normalized and compared with Google Sheets history.
- Telegram receives daily reports and separate price alerts.
- AI Agent briefly explains each price change.

**Stack:** `n8n` · `JavaScript` · `Google Sheets` · `Telegram Bot API` · `Groq`

[📂 Open Project](https://github.com/Andy-randy/n8n-portfolio/tree/main/05-competitor-price-%26-offer-monitoring-system)

---

### 🤖 AI Assistant That Closes Orders

**Goal:** automate customer communication from the first message to order confirmation.

**Workflow:**

```text
Telegram Trigger
→ AI Agent + Simple Memory
→ order readiness check
→ Google Sheets
→ Telegram manager notification
```

**Key points:**

- The AI Agent talks to the customer and collects order details.
- Simple Memory keeps the conversation context.
- The LLM decides when enough information has been collected.
- The manager receives structured order data instead of raw chat messages.

**Stack:** `n8n` · `Groq` · `Telegram Bot API` · `Google Sheets`

---

### 🎯 Lead Funnel With an LLM Classifier

**Goal:** automatically classify incoming leads as cold, warm, or hot.

**Workflow:**

```text
Webhook
→ AI Agent
→ Code node
→ Switch
├── cold lead → email + Google Sheets
├── warm lead → email + Google Sheets
├── hot lead → Telegram manager ping + Bitrix24 CRM
└── fallback → Telegram error notification
```

**Stack:** `n8n` · `Groq` · `Webhook` · `JavaScript` · `Gmail` · `Telegram` · `Google Sheets` · `Bitrix24 REST API`

---

### 🔍 Smart Vacancy Parser With LLM Scoring

**Goal:** reduce manual job-search filtering and keep only relevant vacancies.

**Workflow:**

```text
Schedule / Manual Trigger
→ HH.ru API
→ JavaScript normalization
→ Loop Over Items
→ AI scoring
→ IF filter
→ Telegram digest
```

**Stack:** `n8n` · `Groq` · `HH.ru API` · `Telegram Bot API` · `JavaScript`

---

## Additional Projects

The portfolio also includes:

- RSS / news digest automation
- E-commerce order processing
- HR onboarding workflow
- Financial monitoring
- AI content repurposing
- Customer support routing
- Notion API automations

---

## Technical Stack

**Automation:** `n8n`, Webhooks, Schedules, Switch, IF, Loops  
**AI / LLM:** `Groq`, AI Agent, RAG, Prompt Engineering  
**Integrations:** Telegram, Gmail, Google Sheets, Notion, Supabase, Bitrix24  
**Code:** JavaScript, Python basics, REST APIs, JSON  
**Tools:** Git, GitHub, Docker, VS Code

---

## Contacts

- Telegram: [@Andyyy_Randyyy](https://t.me/Andyyy_Randyyy)
- GitHub: [Andy-randy](https://github.com/Andy-randy)
- Workflow portfolio: [n8n-portfolio](https://github.com/Andy-randy/n8n-portfolio)
