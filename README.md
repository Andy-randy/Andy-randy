# Daria · `Andy-randy`

**Automation engineer · n8n + LLM**

Собираю системы, которые заменяют ручные операционные процессы — не одноразовые скрипты, а воркфлоу с AI-агентами, обработкой ошибок и документацией, готовые к эксплуатации.

I build automation systems that replace manual ops work — not one-off scripts, but workflows with AI agents, error handling, and documentation ready for production.

[🇷🇺 По-русски](#-по-русски) · [🇬🇧 In English](#-in-english)

---

## 🇷🇺 По-русски

### О чём это портфолио

Специализируюсь на n8n с интеграцией LLM: AI-агенты для продаж и обработки заказов, маршрутизация лидов, парсинг данных с LLM-скорингом. В репозитории [`n8n-portfolio`](https://github.com/Andy-randy/n8n-portfolio) — готовые воркфлоу с описанием и экспортированным JSON.

**Сейчас:** open to freelance · ищу позиции automation / workflow engineer  
**В фокусе роста:** RAG и vector DBs, LangChain / CrewAI, продакшен-деплой в Docker  
**Языки:** русский, английский

### Избранные кейсы

#### 🤖 AI-ассистент, который сам закрывает заказы
**Контекст.** Владельцу бизнеса нужен бот, который ведёт клиента от первого сообщения до подтверждения заказа — и сам понимает, когда собрано достаточно данных, чтобы оформить сделку, а не мучает клиента лишними вопросами.  
**Система.** Telegram-триггер → AI-агент на Groq c Simple Memory → разветвление: если агент считает, что пора подтверждать — бот отправляет клиенту подтверждение, структурирует данные, пишет заказ в Google Sheets и уведомляет менеджера; если нет — задаёт уточняющий вопрос.  
**Что интересно.** Переход между стадиями «разговор → подтверждение» принимает LLM, а не жёсткий if-else по ключевым словам. За счёт этого сценарий не ломается на «нестандартных» клиентах. Уведомление менеджера — отдельный узел, чтобы не тормозить ответ клиенту.  
**Стек.** `n8n` · `Groq` · `Telegram Bot API` · `Google Sheets`

#### 🎯 Воронка лидов с LLM-классификатором
**Контекст.** Входящие лиды надо делить по температуре и распределять по каналам: холодных — в nurture-рассылку, тёплых — в CRM менеджеру с уведомлением, горячих — на прямой контакт.  
**Система.** Webhook принимает данные лида → AI-агент на Groq классифицирует его как холодный / тёплый / горячий → Switch маршрутизирует: холодные → email через Gmail + лог в Google Sheets; тёплые → уведомление менеджеру в Telegram + карточка в Bitrix24 через REST API; горячие → прямой email.  
**Что интересно.** Классификатор — не regex и не набор правил, а LLM, которая корректно разбирает расплывчатые формулировки в заявках («подумаю», «нужно срочно», «сколько примерно стоит»). Webhook как универсальная точка входа — подключается любая форма, лендинг или чат.  
**Стек.** `n8n` · `Groq` · Webhook · `Gmail` · `Telegram` · `Google Sheets` · `Bitrix24 REST API`

#### 🔍 Умный парсер вакансий с LLM-скорингом
**Контекст.** Поиск работы через ленту HH.ru быстро превращается в ручную фильтрацию десятков постов в день: открыть, пробежать глазами, закрыть, повторить. Нужен инструмент, который оставляет только релевантные вакансии — и по содержанию, и по формальным требованиям.  
**Система.** HTTP GET к HH.ru API → JavaScript нормализует поля (зарплата, формат работы, описание) → Loop по вакансиям → AI-агент на Groq с фиксированным промптом под мои навыки оценивает каждую → IF проверяет жёсткие условия (зарплата ≥ 100k AND удалёнка). Подходящие собираются в Telegram-дайджест через Aggregate + Code; остальные уходят отдельным сообщением — чтобы ничего не потерялось.  
**Что интересно.** Чистое разделение ответственности между LLM и детерминированной логикой: Groq судит о содержании (соответствуют ли навыки описанию), IF обрабатывает объективные критерии (зарплата, формат). LLM не считает числа — где она ошибается чаще всего. Плюс реальное использование: этим парсером я сама отсмотрела ~10 вакансий при поиске работы и определила лучший fit для себя.  
**Стек.** `n8n` · `Groq` · `HH.ru API` · `Telegram Bot API` · JavaScript

> **Ещё проекты в репозитории:** новостной дайджест из RSS, обработка заказов для e-commerce, HR-онбординг, финансовый мониторинг, AI-репурпозинг контента, клиентский букинг-бот, автоматизации для Notion через API.

### Чему учусь на чужих воркфлоу

Помимо своих проектов — разбираю готовые шаблоны сложных n8n-систем, чтобы понять архитектурные решения. Например, финансовый трекер с мультиформатным вводом (photo / PDF / text), OCR-пайплайнами через Google Gemini и Structured Output Parser для нормализации данных. Читать чужой код — отдельный навык, и мне кажется правильным прокачивать его параллельно с построением собственных систем.

### Стек

**Automation** `n8n` · webhooks · subworkflows · error handling · cron  
**AI / LLM** `Groq` · `OpenAI` · prompt engineering · AI-агенты с памятью  
**Backend** `Python` · REST API · `Docker` · `Git`  
**Data & tools** `Google Sheets` · `Notion API` · `Bitrix24` · `Telegram Bot API`

### Как я работаю с задачей

1. Разбираем в бизнес-терминах: какой процесс, где теряется время, где риски ошибок.
2. Рисую схему: точки интеграции, точки отказа, что логируется.
3. MVP → демо → итерируем. Не пытаюсь «сразу идеально».
4. Документация: README, комментарии в узлах, отдельный лог ошибок и решений — чтобы следующий человек (или я через месяц) разобрался без моих объяснений.

### Контакты

- Telegram: [@Andyyy_Randyyy](https://t.me/Andyyy_Randyyy)
- GitHub: [Andy-randy](https://github.com/Andy-randy)
- Портфолио воркфлоу: [n8n-portfolio](https://github.com/Andy-randy/n8n-portfolio)

---

## 🇬🇧 In English

### About this profile

I specialise in n8n workflows with LLM integrations: AI agents for sales and order processing, lead routing, data parsing with LLM-based scoring. The [`n8n-portfolio`](https://github.com/Andy-randy/n8n-portfolio) repository has the workflows with descriptions and exported JSON.

**Currently:** open to freelance · looking for automation / workflow engineer roles  
**Growing into:** RAG and vector DBs, LangChain / CrewAI, production deployment with Docker  
**Languages:** Russian, English

### Selected case studies

#### 🤖 AI assistant that closes orders on its own
**Context.** A business owner needs a bot that guides the customer from first message to order confirmation — and figures out by itself when it has enough data to close, instead of drowning the client in clarifying questions.  
**System.** Telegram trigger → an AI agent on Groq with Simple Memory → branching: if the agent decides it's time to confirm, the bot sends a confirmation to the customer, structures the data, writes the order to Google Sheets and notifies the manager; if not, it asks a follow-up question.  
**What's interesting.** The decision to move from "conversation" to "confirmation" is made by the LLM, not by a hard-coded if-else on keywords — so the flow doesn't break on non-standard customers. The manager notification is a separate node so it never slows down the customer-facing reply.  
**Stack.** `n8n` · `Groq` · `Telegram Bot API` · `Google Sheets`

#### 🎯 Lead funnel with an LLM classifier
**Context.** Incoming leads need to be split by temperature and routed to the right channel: cold into a nurture email flow, warm to a sales manager with a CRM card, hot to direct contact.  
**System.** A webhook receives the lead → an AI agent on Groq classifies it as cold / warm / hot → a Switch node routes it: cold → Gmail + log in Google Sheets; warm → Telegram alert to the manager + a Bitrix24 card via REST API; hot → direct email.  
**What's interesting.** The classifier isn't a regex or a set of rules — it's an LLM that correctly handles vague wording in real lead forms ("just thinking", "need it urgently", "roughly how much"). The webhook acts as a universal entry point — any form, landing page or chat can plug in.  
**Stack.** `n8n` · `Groq` · Webhook · `Gmail` · `Telegram` · `Google Sheets` · `Bitrix24 REST API`

#### 🔍 Smart vacancy parser with LLM-based scoring
**Context.** Job hunting on HH.ru quickly turns into manually filtering dozens of postings a day: open, skim, close, repeat. You need a tool that leaves only the relevant ones — both by content and by hard requirements.  
**System.** HTTP GET to the HH.ru API → JavaScript normalises the fields (salary, work format, description) → Loop over items → an AI agent on Groq with a fixed prompt tuned to my skills evaluates each posting → an IF node applies hard conditions (salary ≥ 100k AND remote). Matching vacancies go into a Telegram digest via Aggregate + Code; the rest go into a separate message — so nothing gets lost.  
**What's interesting.** A clean split of responsibilities between the LLM and deterministic logic: Groq judges content (do the skills match the description), the IF handles objective criteria (salary, work format). The LLM doesn't do the maths — which is where it's weakest. Plus real usage: I used this parser myself to review ~10 postings during my own job search and identify my best-fit role.  
**Stack.** `n8n` · `Groq` · `HH.ru API` · `Telegram Bot API` · JavaScript

> **More projects in the repository:** RSS news digest, e-commerce order processing, HR onboarding, financial monitoring, AI content repurposing, customer booking bot, Notion API automations.

### What I've been studying from others' workflows

Alongside my own projects, I dig into ready-made templates of complex n8n systems to understand the architectural choices behind them. For example, a finance tracker with multi-format input (photo / PDF / text), OCR pipelines through Google Gemini, and a Structured Output Parser for data normalisation. Reading someone else's code is a separate skill, and I think it's worth training alongside building my own systems.

### Stack

**Automation** `n8n` · webhooks · subworkflows · error handling · cron  
**AI / LLM** `Groq` · `OpenAI` · prompt engineering · AI agents with memory  
**Backend** `Python` · REST APIs · `Docker` · `Git`  
**Data & tools** `Google Sheets` · `Notion API` · `Bitrix24` · `Telegram Bot API`

### How I approach a project

1. Frame the task in business terms — which process, where time is lost, where the risk of errors sits.
2. Sketch the system: integration points, failure points, what gets logged.
3. MVP → demo → iterate. No pretending to ship it perfect on the first try.
4. Document: a README, comments in the nodes, and a separate log of mistakes and fixes — so that the next person (or me in a month) can figure it out without my explanations.

### Contacts

- Telegram: [@Andyyy_Randyyy](https://t.me/Andyyy_Randyyy)
- GitHub: [Andy-randy](https://github.com/Andy-randy)
- Workflow portfolio: [n8n-portfolio](https://github.com/Andy-randy/n8n-portfolio)
