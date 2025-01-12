# RAG System для 1С документации

## Назначение
Модуль реализует систему Retrieval-Augmented Generation для эффективного поиска и использования информации из документации 1С.

## Основные компоненты

### Embeddings
- Разбиение wiki-страниц на смысловые чанки
- Генерация векторных представлений текста
- Хранение embeddings в векторной БД (Milvus/Qdrant/FAISS)

### Graph Database (опционально)
- Хранение связей между объектами конфигурации
- Построение графа зависимостей
- Использование Neo4j/ArangoDB для навигации

## Планируемая структура
```
rag-system/
├─ embeddings/
│  ├─ chunker.py      # Разбиение текста на чанки
│  ├─ vectorizer.py   # Генерация embeddings
│  └─ storage.py      # Работа с векторной БД
├─ graph/
│  ├─ builder.py      # Построение графа
│  └─ queries.py      # Запросы к графовой БД
├─ search/
│  └─ engine.py       # Поисковая логика
└─ main.py           # Точка входа
```

## Технологии
- Sentence Transformers / OpenAI Embeddings
- Milvus / Qdrant / FAISS
- Neo4j / ArangoDB (опционально)

## TODO
- [ ] Реализовать базовый chunker
- [ ] Добавить генерацию embeddings
- [ ] Настроить векторную БД
- [ ] Реализовать поисковые запросы
