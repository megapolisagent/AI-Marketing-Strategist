---
name: customer-journey-mapping
description: Map customer journeys from awareness to advocacy. Visualize touchpoints, identify drop-off points, analyze channel interactions, and optimize the end-to-end experience. Use when the user asks about customer journey, funnel mapping, touchpoint analysis, or experience optimization.
license: MIT
origin: custom
author: Rebecca Rae Barton
author_url: https://github.com/thatrebeccarae
metadata:
  version: 1.1.0
  category: strategy
  domain: customer-experience
  updated: 2026-03-18
  tested: 2026-03-18
  tested_with: "Claude Code v2.1"
---

> Адаптировано Engineer 2026-09-11: донор-версия (v1.0.0) была нетронутым B2B SaaS-шаблоном (NRR,
> setup wizard, GA4-воронки) — нулевая применимость к реальному делу владельца (premium-недвижимость,
> высокочековая сделка с человеком, не self-serve продукт), и три ссылки на несуществующие в этой
> установке скиллы (`google-analytics`, `retention-churn-prevention`, `icp-research`). Правки ниже:
> (1) стадии/метрики обобщены так, чтобы работать и для SaaS, и для высокочековой сделки через
> человека — роль сама заявлена универсальной (`CLAUDE.md`), не только под одно дело; (2) добавлен
> рабочий вариант для relationship-sales с реальными точками из уже собранного профиля аудитории
> этого дела (`knowledge/businesses/агентство-недвижимости-премиум.md`); (3) мёртвые ссылки убраны.

# Customer Journey Mapping

Map, analyze, and optimize the full customer journey from first touch to advocacy.

## Journey Stages

Шесть стадий — общий скелет для любой модели продаж. Столбцы «SaaS/self-serve» и «Высокочековая
сделка через человека» — два готовых варианта; для другой модели адаптируй по тому же принципу
(не выдумывай метрики, которых бизнес физически не может измерить).

| Stage | Customer Goal | SaaS/self-serve (Channels · Metrics) | Высокочековая сделка через человека, напр. недвижимость (Channels · Metrics) |
|-------|-------------|-------------|-------------|
| **Awareness** | Discover a solution/provider exists | SEO, social, ads, PR, referral · Impressions, reach, brand searches | Личный бренд/контент, доски объявлений (Avito/ЦИАН), сарафан, закрытые клубы · Просмотры карточки, обращения, брендовые запросы |
| **Consideration** | Evaluate options | Blog, reviews, comparison, webinar · Time on site, pages/session, downloads | Сравнение предложений/агентов, отзывы, закрытые показы · Число просмотренных объектов, повторные обращения |
| **Decision** | Choose and commit | Pricing page, demo, trial, sales · Conversion rate, CAC, time to close | Личная встреча/показ, переговоры по цене, эксклюзивный договор · Конверсия в договор, срок от первого контакта до сделки |
| **Fulfillment** (было «Onboarding» — переименовано, «настройка продукта» не универсальна) | Get what was promised, without friction | Welcome email, docs, setup wizard · Activation rate, time to value | Юридическое оформление, нотариус, передача ключей · Срыв сделки на этом этапе (%), срок закрытия после договора |
| **Retention** | Continue getting value / stay satisfied | Product, email, success team · NRR, usage frequency, NPS | Повторная сделка (апгрейд/второй объект), поддержание отношений · Доля повторных клиентов, срок до повторного обращения |
| **Advocacy** | Recommend to others | Referral, review, community · NPS, referral rate, review count | Рекомендация знакомым, отзыв, вход в закрытый клуб · Доля сделок по рекомендации |

**Как выбирать вариант:** self-serve модель (пользователь сам доходит до покупки без человека на той
стороне) → колонка SaaS. Сделка, где решение реально принимается в разговоре с человеком (агентом,
консультантом, продавцом) — недвижимость, консалтинг, B2B-контракты — → колонка справа, метрики
считаются по реальным точкам контакта (звонки, показы, встречи), не по вебу.

## Journey Map Template

For each stage, document:

```markdown
### [Stage Name]

**Customer goal:** What are they trying to accomplish?
**Emotional state:** How do they feel? (confident, anxious, frustrated, delighted)
**Touchpoints:**
- [Channel 1]: [Specific interaction]
- [Channel 2]: [Specific interaction]

**Pain points:**
- [What causes friction or frustration]

**Opportunities:**
- [How to improve the experience]

**Key metric:** [Primary measurement]
**Drop-off risk:** [What causes people to leave at this stage]
```

## Touchpoint Inventory

### Common B2B SaaS Touchpoints

| Stage | Touchpoint | Owner |
|-------|-----------|-------|
| Awareness | Google search result | SEO/Content |
| Awareness | LinkedIn ad | Paid Media |
| Awareness | Blog post | Content |
| Consideration | Product page | Marketing |
| Consideration | Case study | Marketing |
| Consideration | Demo request form | Marketing |
| Decision | Sales demo | Sales |
| Decision | Pricing page | Product/Marketing |
| Decision | Proposal/contract | Sales |
| Onboarding | Welcome email sequence | CRM/CS |
| Onboarding | Setup wizard | Product |
| Onboarding | First value moment | Product |
| Retention | Feature adoption email | Product/CRM |
| Retention | QBR/check-in | CS |
| Retention | Product updates | Product |
| Advocacy | NPS survey | CS |
| Advocacy | Referral program | Growth |
| Advocacy | Case study request | Marketing |

Adapt the owner column to the delegation model actually in place — for a non-SaaS business, "Owner" names the specialist agent or channel responsible for that touchpoint, not a department.

### Пример — высокочековая сделка через человека (premium-недвижимость)

Собрано по уже известному профилю аудитории этого дела
(`knowledge/businesses/агентство-недвижимости-премиум.md`), не выдумано заново.

| Stage | Touchpoint | Owner |
|-------|-----------|-------|
| Awareness | Личный бренд-контент (соцсети/каналы), карточка на Avito/ЦИАН | Личный бренд владельца, Авитолог |
| Awareness | Рекомендация знакомого / вход через закрытый клуб инвесторов | Сарафан, вне контроля агента |
| Consideration | Звонок/переписка с агентом, ответ на возражение | Агент, Авитолог (авто-ответ) |
| Consideration | Закрытый показ без публичного объявления | Агент лично |
| Decision | Личная встреча, обсуждение цены и условий | Агент лично |
| Decision | Эксклюзивный договор | Агент лично, юрист |
| Fulfillment | Юридическое оформление, нотариус | Юрист, агент |
| Fulfillment | Передача ключей | Агент лично |
| Retention | Контакт после сделки (не бросить клиента) | Агент лично |
| Advocacy | Рекомендация знакомым, отзыв | Сарафан, вне контроля агента |

## Drop-Off Analysis

### Identifying Drop-Offs

Метод зависит от модели — не универсален, не подставляй SaaS-инструменты бизнесу без веб-воронки:
1. **Self-serve/веб-воронка:** GA4 funnel reports, cohort analysis, conversion tracking.
2. **Продажа через человека:** нет автоматических цифр — считать вручную по CRM/журналу звонков
   (сколько дошло от звонка до показа, от показа до договора), спрашивать причину отказа напрямую.
3. **Qualitative (обе модели):** интервью с клиентами, темы жалоб/возражений.
4. **Survey:** опрос после каждого перехода — уместен для веб-воронки, для сделки через человека
   часто заменяется прямым вопросом агента при отказе.

### Common Drop-Off Points

| Transition | SaaS/self-serve — Drop-Off Cause | Продажа через человека — Drop-Off Cause | Fix (общий принцип) |
|-----------|---------------|---------------|-----|
| Awareness → Consideration | Irrelevant content, slow site | Карточка не отвечает на страх (юр. чистота, обременения) | Уточнить сообщение под конкретный страх аудитории |
| Consideration → Decision | No social proof, unclear pricing | Недоверие к мотивам агента («гонит к быстрой сделке») | Прозрачность цены/комиссии, доказуемые детали вместо обещаний |
| Decision → Fulfillment | Complex signup, payment friction | Срыв сделки на позднем этапе (мошенники, юр. риск) | Юридическая защита сделки видна клиенту заранее, не постфактум |
| Fulfillment → Retention | No clear first value, poor UX | Клиента «бросили» сразу после закрытия сделки | Плановый контакт после сделки, не только до неё |
| Retention → Advocacy | No program, not asked | Не попросили рекомендацию/отзыв напрямую | Прямой, а не подразумеваемый, запрос рекомендации |

## Persona-Based Journeys

Different personas take different paths. Create journey variants for:
- **By role:** Technical evaluator vs executive buyer vs end user
- **By company size:** SMB (self-serve) vs enterprise (sales-assisted)
- **By intent:** Problem-aware vs solution-aware vs product-aware
- **By channel:** Inbound (SEO/content) vs outbound (sales/ads)

## Integration with Other Skills

Проверено против реального состава `.claude/skills/` этого агента 2026-09-11 — оставлены только
скиллы, которые физически установлены; остальные из версии донора удалены как мёртвые ссылки
(`google-analytics`, `retention-churn-prevention`, `icp-research` в этой установке не существуют).

- **`cro-auditor`** — Deep-dive on high-drop-off pages (веб-воронка) или на конкретной точке контакта (сделка через человека).
- **`competitive-brief`** — чем заканчивается путь клиента у конкурента, не только у нас.
- **`lead-magnets`** — что предложить на стадии Awareness/Consideration, чтобы не терять контакт.
