# 1c-analyzer-wiki-rag

**1c-analyzer-wiki-rag** — это открытый проект, где мы создаём **инструмент** для **анализа** конфигурации 1С:Предприятие и **автоматического** построения:
- **Wiki** (база знаний со статьями о каждом объекте и процедуре).
- **RAG** (Retrieval-Augmented Generation) — векторная и графовая база для поиска по коду и метаданным.
- **AI-бота**, который сможет отвечать на вопросы о конфигурации, опираясь на реальную структуру и логику 1С.

## Кому это нужно?

- **1С-разработчикам**, у которых есть большие/сложные конфигурации и необходимость их изучения.
- Тем, кто хочет проще понимать чужие решения, видеть цепочки вызовов и быстро отвечать на «кто вызывает процедуру X?», «как устроен процесс проведения?» и т.д.

## Что планируется?

1. **Парсинг** XML (метаданные).
2. Построение [**AST**](https://github.com/1C-Migration-Lab/.github/blob/main/docs/levels-of-abstraction.md#abstract-syntax-tree), [**IR**](https://github.com/1C-Migration-Lab/.github/blob/main/docs/levels-of-abstraction.md#intermediate-representation), [(**Dependency Graph**)](https://github.com/1C-Migration-Lab/.github/blob/main/docs/levels-of-abstraction.md#dependency-graph).
3. **Суммаризация** кода (объяснение логики) с помощью LLM.
4. Генерация **Wiki** (статьи о каждом объекте).
5. Создание **векторной** и **графовой** базы для быстрого поиска и контекстной выдачи.
6. **AI-бот**, который обогащает ответы ссылками на конкретные модули и объекты конфигурации.

## Текущий статус

Репозиторий пока пуст — формируем структуру, задачи и план работ. В ближайшее время появятся:
- [Техническое Задание (TECH-SPEC.md)](./docs/TECH-SPEC.md)
- **Примеры** анализа «мини-конфигурации» 1С.
- **Задачи (Issues)** для желающих внести вклад.

## Как присоединиться?

1. **Подпишитесь** на обновления репозитория.
2. Посещайте раздел [Issues](../../issues) — выбирайте задачи `help wanted`.
3. Делитесь **идеями** и **опросами** в обсуждениях.

**1c-analyzer-wiki-rag** стремится сделать анализ конфигураций 1С удобным и «умным». Присоединяйтесь и помогите нам создать современный инструмент для 1С-сообщества!

---
