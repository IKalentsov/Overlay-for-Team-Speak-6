# Скиллы проекта

53 скилла из базы `IKalentsov/Harness` (коммит `1bc318f`). Лежат в `.dsh/skills/<папка>/SKILL.md`.

Две таблицы: **сверху** — скиллы, которые модель запускает сама; **ниже** — те, что запускает
только человек. Метка после имени: `.NET` — серверные и SQL Server, `фронт` — React и UI,
без метки — общие.

## Модель запускает сама — 33

Скиллы видны в каталоге сессии: агент вызывает их через инструмент `skill`, когда задача
совпадает с описанием. Человеку достаточно попросить словами.

| Скилл | Запуск | Когда | Коротко |
|---|---|---|---|
| [analyzing-dotnet-performance](skills/analyzing-dotnet-performance/SKILL.md) `.NET` | `skill` → `analyzing-dotnet-performance` | Аудит .NET: аллокации, async, горячие пути | Статический скан, не профилировщик |
| [architecture-drift-check](skills/architecture-drift-check/SKILL.md) | `skill` → `architecture-drift-check` | Изменились структура, контракты или стек; надо сверить код с `ARCHITECTURE.md` | Нужен `ARCHITECTURE.md` |
| [better-accessibility](skills/better-accessibility/SKILL.md) `фронт` | `skill` → `better-accessibility` | Доступность, WCAG | Проверять на каждом экране |
| [better-colors](skills/better-colors/SKILL.md) `фронт` | `skill` → `better-colors` | Цветовая система, палитры, контраст | Семантические токены |
| [better-interface](skills/better-interface/SKILL.md) `фронт` | `skill` → `better-interface` | Сводный ревью всех `better-*` | Один проход вместо шести |
| [better-layout](skills/better-layout/SKILL.md) `фронт` | `skill` → `better-layout` | Группировка, выравнивание, порядок чтения | Раскрытие по мере надобности |
| [better-typography](skills/better-typography/SKILL.md) `фронт` | `skill` → `better-typography` | Шкала, кегли, шрифты, переносы | Типографика как система |
| [better-ui](skills/better-ui/SKILL.md) `фронт` | `skill` → `better-ui` | Полировка UI: радиусы, тени, иконки, hit-area | Финальный слой после структуры |
| [better-writing](skills/better-writing/SKILL.md) `фронт` | `skill` → `better-writing` | Тексты продукта | Коротко и по делу |
| [code-review](skills/code-review/SKILL.md) | `skill` → `code-review` | Ревью ветки, PR или изменений «с момента X» | Нужна git-точка отсчёта |
| [codebase-design](skills/codebase-design/SKILL.md) | `skill` → `codebase-design` | Проектирование интерфейса модуля, поиск углублений и швов | Полезнее всего до кода |
| [vercel-composition-patterns](skills/composition-patterns/SKILL.md) `фронт` | `skill` → `vercel-composition-patterns` | Композиция React, compound components, провайдеры | Учитывает React 19 |
| [create-datadriven-aspnetcore](skills/create-datadriven-aspnetcore/SKILL.md) `.NET` | `skill` → `create-datadriven-aspnetcore` | CRUD-страницы и эндпоинты на EF Core без CLI-скаффолдинга | Только ASP.NET + EF Core |
| [diagnosing-bugs](skills/diagnosing-bugs/SKILL.md) | `skill` → `diagnosing-bugs` | «Продиагностируй», падение, баг, тормоза | Сначала воспроизведение, потом правка |
| [domain-modeling](skills/domain-modeling/SKILL.md) | `skill` → `domain-modeling` | Термины, `GLOSSARY.md`, ADR | Запускать при смене домена |
| [dotnet-webapi](skills/dotnet-webapi/SKILL.md) `.NET` | `skill` → `dotnet-webapi` | Эндпоинты, OpenAPI, обработка ошибок | Не для стиля C# и EF-запросов |
| [grilling](skills/grilling/SKILL.md) | `skill` → `grilling` | Стресс-тест плана или решения | Тот же допрос, но инициирует агент |
| [karpathy-guidelines](skills/karpathy-guidelines/SKILL.md) | `skill` → `karpathy-guidelines` | Любое написание, ревью или рефакторинг кода | Читать до кода |
| [optimizing-ef-core-queries](skills/optimizing-ef-core-queries/SKILL.md) `.NET` | `skill` → `optimizing-ef-core-queries` | Медленные запросы EF Core | EF Core, не Dapper и не ADO.NET |
| [pr](skills/pr/SKILL.md) | `skill` → `pr` | Написать тело PR | Только текст PR, нужен дифф |
| [prototype](skills/prototype/SKILL.md) | `skill` → `prototype` | Одноразовый прототип для вопроса дизайна | Код выбрасывается |
| [vercel-react-best-practices](skills/react-best-practices/SKILL.md) `фронт` | `skill` → `vercel-react-best-practices` | React/Next: производительность и паттерны | 70 правил, применять точечно |
| [vercel-react-view-transitions](skills/react-view-transitions/SKILL.md) `фронт` | `skill` → `vercel-react-view-transitions` | Анимации переходов, View Transition API | Без сторонних библиотек |
| [research](skills/research/SKILL.md) | `skill` → `research` | Исследовать вопрос по первоисточникам | Результат — `.md` в репозитории |
| [sqlserver-agent-job-failure-triage](skills/sqlserver-agent-job-failure-triage/SKILL.md) `.NET` | `skill` → `sqlserver-agent-job-failure-triage` | Упал SQL Server Agent job | Сначала причина, потом вмешательство |
| [sqlserver-blocking-troubleshooting](skills/sqlserver-blocking-troubleshooting/SKILL.md) `.NET` | `skill` → `sqlserver-blocking-troubleshooting` | Блокировки, таймауты, «кто держит лок» | Нужен доступ к серверу и DMV |
| [sqlserver-index-verification](skills/sqlserver-index-verification/SKILL.md) `.NET` | `skill` → `sqlserver-index-verification` | Проверить рекомендацию по индексу | Валидация до внедрения |
| [sqlserver-query-store-tuning](skills/sqlserver-query-store-tuning/SKILL.md) `.NET` | `skill` → `sqlserver-query-store-tuning` | Регрессии планов, Query Store | Нужна история в Query Store |
| [tdd](skills/tdd/SKILL.md) | `skill` → `tdd` | Red-green-refactor, тесты первыми | Обычно внутри `implement` |
| [web-design-guidelines](skills/web-design-guidelines/SKILL.md) `фронт` | `skill` → `web-design-guidelines` | Ревью UI на Web Interface Guidelines | Правила из первоисточника |
| [wizard](skills/wizard/SKILL.md) | `skill` → `wizard` | Шаги, доступные только человеку: инфра, креды, дашборд | Генерит bash-визард |
| [writing-for-agents](skills/writing-for-agents/SKILL.md) | `skill` → `writing-for-agents` | Правка скиллов, `AGENTS.md` или `CLAUDE.md` | Правила письма для агентов |
| [writing-guidelines](skills/writing-guidelines/SKILL.md) `фронт` | `skill` → `writing-guidelines` | Ревью документации и прозы | Правила из первоисточника |

## Запускает только человек — 20

Эти скиллы скрыты из каталога (`disable-model-invocation: true`), `skill` их не видит.
Запуск — только командой `/имя` в чате.

| Скилл | Запуск | Когда | Коротко |
|---|---|---|---|
| [ask-matt](skills/ask-matt/SKILL.md) | `/ask-matt` | Не понятно, какой скилл или флоу подходит | Роутер: только направляет |
| [break](skills/break/SKILL.md) `фронт` | `/break` | Прогнать компонент во всех состояниях | Временная страница, не коммитить |
| [explain-interface](skills/explain-interface/SKILL.md) `фронт` | `/explain-interface` | Разобрать, как что-то сделано на вебе | Разбор чужого интерфейса |
| [grill-me](skills/grill-me/SKILL.md) | `/grill-me` | Жёсткий допрос плана без рабочей папки | Интервью, не реализация |
| [grill-with-docs](skills/grill-with-docs/SKILL.md) | `/grill-with-docs` | То же, но с созданием ADR и глоссария | Для проекта с документацией |
| [handoff](skills/handoff/SKILL.md) | `/handoff` | Сжать разговор в документ для следующего агента | Перед сменой сессии или контекста |
| [implement](skills/implement/SKILL.md) | `/implement` | Реализовать работу по спеке или тикетам | Нужны `/to-spec` и `/to-tickets` |
| [implement-spec](skills/implement-spec/SKILL.md) | `/implement-spec` | Реализовать всю спеку сразу субагентами | Альтернатива `implement` |
| [improve-codebase-architecture](skills/improve-codebase-architecture/SKILL.md) | `/improve-codebase-architecture` | Найти возможности углубления в кодовой базе | Выдаёт HTML-отчёт, код не правит |
| [interface-review](skills/interface-review/SKILL.md) `фронт` | `/interface-review` | Детальный ревью UI по категориям | Список находок, не правка |
| [retro](skills/retro/SKILL.md) | `/retro` | Ретроспектива сессии | После крупной работы |
| [setup-matt-pocock-skills](skills/setup-matt-pocock-skills/SKILL.md) | `/setup-matt-pocock-skills` | Первый запуск пайплайна: трекер, лейблы, доки | Один раз до остальных |
| [teach](skills/teach/SKILL.md) | `/teach` | Объяснить концепцию или навык | Код не меняет |
| [to-questionnaire](skills/to-questionnaire/SKILL.md) | `/to-questionnaire` | Вопрос, который решает кто-то другой | Анкета для внешнего человека |
| [to-spec](skills/to-spec/SKILL.md) | `/to-spec` | Превратить разговор в спеку | Без интервью, только синтез |
| [to-tickets](skills/to-tickets/SKILL.md) | `/to-tickets` | Разбить спеку на тикеты с зависимостями | После `/to-spec` |
| [triage](skills/triage/SKILL.md) | `/triage` | Разбор входящих issue и внешних PR | Ведёт по состояниям, пишет брифы |
| [variant](skills/variant/SKILL.md) `фронт` | `/variant` | Несколько вариантов компонента на выбор | Итерации до одного варианта |
| [wait-what](skills/wait-what/SKILL.md) | `/wait-what` | Последний ответ не дошёл — переформулировать | Сигнал остановиться и объяснить заново |
| [wayfinder](skills/wayfinder/SKILL.md) | `/wayfinder` | Огромный туманный объём работ на много сессий | Карта решений, выводит на `/to-spec` |

## Пайплайн

`/setup-matt-pocock-skills` (один раз) → `/ask-matt` → `/grill-with-docs` или `grilling` →
`/to-spec` → `/to-tickets` → `/implement` (или `/implement-spec`) → `code-review` → `pr`.
`diagnosing-bugs`, `retro` и `architecture-drift-check` работают вне этого потока.

## Если скилл нужен модели, а он «только человеческий»

Дать агенту путь к файлу: `.dsh/skills/<папка>/SKILL.md`. `skill` такой скилл не достанет,
а ссылка на файл — сработает.
