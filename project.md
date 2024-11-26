# Инструменты

Для эффективного ведения проектов в **Sagtech** используются различные инструменты, обеспечивающие слаженную работу команды и отслеживание прогресса.

- **GitHub:**  
  Весь код проектов хранится в репозиториях GitHub. Это основная платформа для контроля версий, где осуществляется вся разработка и хранение изменений.

- **RMB-элементы:**  
  Для каждого проекта предусмотрены два RMB-окружения:  
  - **Staging** — среда для тестирования, где проверяются изменения перед выпуском.  
  - **Production** — рабочая среда, представляющая собой реалистичное приложение в лайв-режиме. Она позволяет тестировать продукт так, как его увидит конечный пользователь.

- **Asana:**  
  Asana служит платформой для управления задачами и проектами. Здесь ведется учет всех задач, описывается их статус и обновления. В большинстве случаев работа организована по спринтам, если не оговорен другой формат. Каждый спринт длится две недели, за которые команда фокусируется на завершении конкретного набора задач.

- **Оценка задач:**  
  В качестве оценок задач мы используем:  
  - **Story-пойнты** — оценка сложности задачи.  
  - **Эстимейты по времени** — оценка предполагаемого срока завершения. Эстимейты устанавливаются не по часам, а определенно, например, "до пятницы".

Эти инструменты помогают поддерживать высокий уровень координации и качества работы, обеспечивая прозрачность и эффективность на каждом этапе разработки.

----

# Процесс работы

В **Sagtech** процесс работы организован на доске **Development Board** в Asana. На этой доске задачи распределены по нескольким колонкам, каждая из которых обозначает определенный этап выполнения задачи в рамках спринта или скоупа задач.

## Основные этапы

- **Backlog:**  
  Здесь задачи находятся на этапе первоначальной оценки. Каждая задача получает эстимейт по времени или сложности, который позволяет определить её приоритетность и срок выполнения.

- **ToDo:**  
  Оценённые и утверждённые задачи перемещаются в колонку ToDo. Эти задачи готовы к выполнению и распределяются между членами команды.

- **In Progress:**  
  Задачи, которые выполняются в данный момент времени. Лимит на количество задач от одного исполнителя не должен превышать одного тикета, кроме предоговорённых условий.

- **Pull Request:**  
  На этом этапе задачи, завершённые разработчиком, проходят проверку путём pull request. Проверка осуществляется специалистами той же экспертизы:
  - Фронтендеры проверяют фронтендеров.
  - Бэкендеры — бэкендеров.  
  Если коллеги с аналогичной экспертизой отсутствуют, проверку выполняют лиды, такие как Иван Босак, Андрей Стригалев или Евгений Арол.

- **DevComplete:**  
  Задача может быть перемещена в DevComplete только после успешной проверки pull request и отображения валидных изменений на стейджинг-среде. Эта колонка служит сигналом для тестировщиков, что задача готова для тестирования.

- **QA:**  
  В этой колонке тестировщики проверяют задачи. Если проверка проходит без выявления дефектов, задача перемещается на следующий этап.

- **PO Approval:**  
  На этом этапе управляющий проектом оценивает задачу с учётом бизнес-логики и функциональности. Для каждой задачи на этапе QA должно быть записано демо, в котором тестировщик демонстрирует работу функционала. После подтверждения корректности выполнения задача закрывается. В случае обнаружения дефектов задача возвращается на доработку.

## Работа с багами

Мы стремимся минимизировать количество багов, поскольку они отслеживаются и влияют на общую статистику проекта. Баги классифицируются по степени критичности (**severity**), например:

- **UI-баги:**  
  Недочёты в интерфейсе, такие как неверно воспроизведённые шаблоны, считаются менее допустимыми.

- **Логические баги:**  
  Ошибки в функциональности, которые могут быть допустимыми в определённых случаях.

Особенно важно избегать багов на production-среде, так как их наличие может привести к обсуждению эффективности работы и качества выполнения задач. Важнейшая задача команды — с самого начала делать работу качественно, использовать переиспользуемую логику и проявлять внимательность к деталям.

## Проактивный подход

Если в процессе выполнения задачи вы замечаете изменения, которые могут повлиять на другие части проекта (например, что-то перестало работать или возникли новые зависимости), важно закрыть эти моменты самостоятельно ещё на этапе разработки. При обнаружении значительных изменений, влияющих на логику или сроки выполнения задачи, следует уведомить лидов, чтобы они могли учесть эту информацию при планировании и, если нужно, скорректировать дедлайны.

## Показатели перформанса

Эффективность работы над проектом измеряется по следующим показателям:
- Количество выполненных задач.
- Количество задач, выполненных в срок.
- Общее количество выявленных багов.

Эти метрики учитываются при проведении **перформанс-ревью** сотрудника, что влияет на возможность повышения его заработной платы. Высокие показатели повышают шансы на положительное решение по повышению зарплаты, в то время как низкие могут замедлить этот процесс.