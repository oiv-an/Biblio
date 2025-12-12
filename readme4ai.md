# Biblio AI Assistant Instructions

## Проект / Project

Biblio - это открытая библиотека знаний для хранения MD-файлов с описаниями, промптами, интересными программами, сайтами, QR-кодами и другими полезными ресурсами.

Biblio is an open knowledge library for storing MD files with descriptions, prompts, interesting programs, websites, QR codes, and other useful resources.

## Структура проекта / Project Structure

```
Biblio/
├── categories/          # Основные категории контента
│   ├── ai-tools/       # AI-инструменты и промпты
│   ├── development/    # Разработка и программирование
│   ├── design/         # Дизайн и UX/UI
│   ├── useful-resources/ # Полезные ресурсы
│   └── knowledge-base/ # База знаний и статьи
├── tags/               # Система тегов
├── templates/          # Шаблоны для разных типов контента
├── assets/             # Изображения, QR-коды и медиа
└── search/             # Дополнительные способы поиска
```

## Категории контента / Content Categories

### 1. AI-инструменты (categories/ai-tools/)

**Подкатегории:**
- `chatgpt-prompts/` - Промпты для ChatGPT
- `midjourney-prompts/` - Промпты для Midjourney
- `other-ai-tools/` - Другие AI-инструменты

**Что добавлять:**
- Промпты для нейросетей
- Инструкции по работе с AI
- Описания AI-инструментов

### 2. Разработка (categories/development/)

**Подкатегории:**
- `code-snippets/` - Сниппеты кода
- `libraries/` - Библиотеки
- `frameworks/` - Фреймворки

**Что добавлять:**
- Полезные фрагменты кода
- Описания библиотек и фреймворков
- Примеры реализации

### 3. Дизайн (categories/design/)

**Подкатегории:**
- `ui-kits/` - UI-киты
- `color-palettes/` - Цветовые палитры
- `typography/` - Типографика

**Что добавлять:**
- UI-компоненты и киты
- Цветовые схемы
- Рекомендации по шрифтам

### 4. Полезные ресурсы (categories/useful-resources/)

**Подкатегории:**
- `websites/` - Полезные сайты
- `online-tools/` - Онлайн-инструменты
- `browser-extensions/` - Расширения браузеров

**Что добавлять:**
- Описания полезных сайтов
- Онлайн-сервисы и инструменты
- Расширения для браузеров

### 5. База знаний (categories/knowledge-base/)

**Подкатегории:**
- `tutorials/` - Обучающие материалы
- `articles/` - Статьи
- `documentation/` - Документация

**Что добавлять:**
- Туториалы и инструкции
- Аналитические статьи
- Техническая документация

## Правила именования файлов / File Naming Rules

Используй формат:
```
[тип]-[название-на-английском].md
```

Примеры:
- `prompt-marketing-copywriter.md`
- `tool-figma-design-system.md`
- `website-color-palette-generator.md`
- `snippet-javascript-debounce.md`
- `article-ai-prompt-engineering.md`

## Шаблоны / Templates

Используй соответствующие шаблоны из папки `templates/`:

1. **Для промптов:** `templates/prompt-template.md`
2. **Для инструментов:** `templates/tool-template.md`
3. **Для сайтов:** `templates/website-template.md`
4. **Для статей:** `templates/article-template.md`

## Метаданные / Metadata

Каждый файл должен содержать YAML frontmatter с обязательными полями:

```yaml
---
title: "Название на русском"
title_en: "Title in English"
description: "Краткое описание на русском"
description_en: "Brief description in English"
category: "категория"
subcategory: "подкатегория"
tags: ["тег1", "тег2", "ru", "en"]
author: "Имя автора"
date_created: "ГГГГ-ММ-ДД"
date_updated: "ГГГГ-ММ-ДД"
language: "both"  # ru, en, both
difficulty: "beginner"  # beginner, intermediate, advanced
rating: 5  # 1-5
external_url: "https://example.com"  # если применимо
---
```

## Теги / Tags

**Обязательные теги:**
- `ru` - для материалов на русском
- `en` - для материалов на английском
- `both` - для двуязычных материалов

**Тематические теги:**
- `ai`, `prompt`, `chatgpt`, `midjourney`
- `code`, `javascript`, `python`, `php`
- `design`, `ui`, `ux`, `color`, `typography`
- `tool`, `website`, `online-tool`, `extension`
- `tutorial`, `article`, `documentation`

## Алгоритм обработки запроса / Request Processing Algorithm

1. **Определи тип контента** по ключевым словам:
   - "промпт", "prompt" → ai-tools/chatgpt-prompts/
   - "код", "snippet", "function" → development/code-snippets/
   - "сайт", "website", "инструмент" → useful-resources/websites/
   - "статья", "туториал" → knowledge-base/articles/

2. **Выбери подходящий шаблон** из templates/

3. **Заполни метаданные** согласно правилам

4. **Сгенерируй контент** на обоих языках

5. **Создай файл** с правильным именем в нужной папке

6. **Обнови индексные файлы**:
   - Добавь материал в соответствующий README категории
   - Обнови tags/index.md
   - Обнови search/by-date.md

## Пример обработки запроса / Example Request Processing

**Запрос пользователя:**
"Нужен промпт для написания маркетинговых текстов для email-рассылок"

**Обработка:**
1. Тип: промпт → ai-tools/chatgpt-prompts/
2. Шаблон: prompt-template.md
3. Имя файла: prompt-email-marketing.md
4. Метаданные: tags=["prompt", "chatgpt", "marketing", "email", "ru", "en"]
5. Создать файл и обновить индексы

## Важные замечания / Important Notes

- Все материалы должны быть двуязычными
- Используй существующие теги когда возможно
- Следуй структуре метаданных из шаблонов
- Обновляй индексные файлы после добавления материала
- Проверяй уникальность имени файла

---

Этот файл служит инструкцией для AI-ассистента по обработке и распределению контента в проекте Biblio.

This file serves as an instruction for AI assistant for processing and distributing content in the Biblio project.