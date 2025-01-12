# Инструкция по использованию

## Требования
- Python 3.8+
- Git

## Установка
```bash
git clone [repository-url]
cd 1c-analyzer-wiki-rag
# Дополнительные шаги установки будут добавлены позже
```

## Использование

### Парсинг конфигурации
```bash
python parser/main.py --config=mini-configs/example.xml
```

### Генерация Wiki
```bash
python wiki-generator/main.py --source=output.json --out=wiki/
```

### Запуск RAG системы
```bash
# Команды будут добавлены позже
```

### Запуск бота
```bash
# Команды будут добавлены позже
```

## Добавление новой конфигурации
1. Выгрузите конфигурацию в XML формате
2. Поместите файлы в директорию `mini-configs/`
3. Запустите парсер
