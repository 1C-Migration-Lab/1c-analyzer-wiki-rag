# Примеры использования

## Пример анализа мини-конфигурации "Заказы"

### 1. Структура тестовой конфигурации
```
mini-configs/orders/
├─ Configuration.xml
├─ Catalogs/
│  ├─ Товары/
│  │  └─ Ext/
│  │      └─ ObjectModule.bsl
│  └─ Контрагенты/
└─ Documents/
   └─ ЗаказПокупателя/
      └─ Ext/
          └─ ObjectModule.bsl
```

### 2. Парсинг конфигурации
```bash
python parser/main.py --config=mini-configs/orders/Configuration.xml
```

Результат:
```json
{
  "name": "Заказы",
  "catalogs": [
    {
      "name": "Товары",
      "uuid": "...",
      "properties": [...]
    },
    {
      "name": "Контрагенты",
      "uuid": "...",
      "properties": [...]
    }
  ],
  "documents": [
    {
      "name": "ЗаказПокупателя",
      "uuid": "...",
      "properties": [...],
      "methods": [
        {
          "name": "ПриПроведении",
          "description": "..."
        }
      ]
    }
  ]
}
```

### 3. Генерация Wiki
```bash
python wiki-generator/main.py --source=output.json --out=wiki/
```

Создаст файлы:
- wiki/Document_ЗаказПокупателя.md
- wiki/Catalog_Товары.md
- wiki/Catalog_Контрагенты.md

### 4. Пример запроса к боту
```
Q: Как работает проведение документа ЗаказПокупателя?
A: При проведении документа "Заказ покупателя" выполняются следующие операции:
1. Проверяется наличие товаров
2. Резервируется количество на складе
3. Формируются движения по регистрам
...
