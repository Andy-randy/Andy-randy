# Daria Lesnikova ·

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
- парсинг и нормализация данных;
- workflow-документация, чтобы проект можно было передать другому человеку.

Основной репозиторий с проектами: [`n8n-portfolio`](https://github.com/Andy-randy/n8n-portfolio)

**Сейчас:** открыта к freelance-задачам и junior / junior+ позициям в automation / workflow engineering.  
**В фокусе роста:** RAG, Supabase / vector DB, Docker, production deployment, прикладной Python.  
**Языки:** русский, английский.

---

## Избранные проекты

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
**AI / LLM:** `Groq` · AI Agent · Simple Memory · structured JSON output · prompt engineering  
**Integrations:** `Telegram Bot API` · `Gmail` · `Google Sheets` · `Bitrix24 REST API` · `Notion API` · `HH.ru API`  
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

My focus is not “a bot for the sake of a bot”, but practical business automation:

- incoming lead processing;
- AI lead qualification;
- Telegram and email notifications;
- CRM, Google Sheets, Notion, and external API integrations;
- data parsing and normalization;
- workflow documentation so the project can be maintained or handed over.

Main project repository: [`n8n-portfolio`](https://github.com/Andy-randy/n8n-portfolio)

**Currently:** open to freelance tasks and junior / junior+ automation or workflow engineering roles.  
**Growing into:** RAG, Supabase / vector DBs, Docker, production deployment, practical Python.  
**Languages:** Russian, English.

---

## Selected Projects

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

**Key points:**

- The AI Agent analyzes the meaning of the request, not just keywords.
- The Code node cleans and parses the model’s JSON output.
- The budget is extracted from the request text.
- Hot leads are sent to Bitrix24 CRM through REST API.
- Invalid AI output is handled through a fallback branch.

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

**Key points:**

- Deterministic logic checks objective conditions: salary and work format.
- The LLM evaluates semantic relevance.
- Matching vacancies are collected into a Telegram digest.
- Non-matching vacancies are logged separately so nothing gets lost.

**Stack:** `n8n` · `Groq` · `HH.ru API` · `Telegram Bot API` · `JavaScript`

---

## Additional Projects

The portfolio also includes:

- RSS / news digest automation;
- e-commerce order processing;
- HR onboarding workflow;
- financial monitoring;
- AI content repurposing;
- customer support routing;
- Notion API automations.

---

## Technical Stack

**Automation:** `n8n` · Webhook · Schedule Trigger · Switch · IF · Loop · Aggregate · Error handling  
**AI / LLM:** `Groq` · AI Agent · Simple Memory · structured JSON output · prompt engineering  
**Integrations:** `Telegram Bot API` · `Gmail` · `Google Sheets` · `Bitrix24 REST API` · `Notion API` · `HH.ru API`  
**Code:** `JavaScript` for Code node · basic `Python` · REST API · JSON  
**Tools:** `Git` · `GitHub` · `Docker` · `VS Code`

---

## How I Approach Automation Projects

1. I start with the business process: where time is lost, where manual work happens, where errors appear.
2. I sketch the workflow: input data, branches, integrations, fallback logic.
3. I build an MVP and test it on sample data.
4. I add error handling, logging, and clear node names.
5. I document the project: README, sample input, workflow export, and architecture screenshot.

---

## Contacts

- Telegram: [@Andyyy_Randyyy](https://t.me/Andyyy_Randyyy)
- GitHub: [Andy-randy](https://github.com/Andy-randy)
- Workflow portfolio: [n8n-portfolio](https://github.com/Andy-randy/n8n-portfolio)
