# How to Contribute to Biblio 📚

Thank you for your interest in developing the Biblio library! This document will help you understand how to contribute to the project.

## Table of Contents

- [How to Contribute to Biblio 📚](#how-to-contribute-to-biblio-)
  - [Table of Contents](#table-of-contents)
  - [Types of Contributions](#types-of-contributions)
  - [Process for Adding Materials](#process-for-adding-materials)
    - [1. Preparation](#1-preparation)
    - [2. Creating Material](#2-creating-material)
    - [3. Submission](#3-submission)
  - [Material Format](#material-format)
    - [Languages](#languages)
    - [Structure](#structure)
  - [File Naming Rules](#file-naming-rules)
  - [Metadata Structure](#metadata-structure)
    - [Required Fields](#required-fields)
    - [Categories](#categories)
    - [Subcategories](#subcategories)
  - [Pre-submission Checklist](#pre-submission-checklist)
  - [Code of Conduct](#code-of-conduct)
  - [Questions?](#questions)

## Types of Contributions

We welcome the following types of contributions:

1. **New Materials** - adding prompts, tools, websites, articles
2. **Updating Existing Materials** - fixing errors, adding information
3. **Documentation Improvements** - fixing typos, improving descriptions
4. **Structural Suggestions** - ideas for improving content organization

## Process for Adding Materials

### 1. Preparation

1. Fork the repository
2. Create a new branch: `git checkout -b add-new-material`
3. Make sure the material doesn't already exist in the library

### 2. Creating Material

1. Choose the appropriate [template](../templates/) for your material
2. Create a new file in the corresponding category
3. Fill in all necessary metadata
4. Write quality content in both languages (Russian and English)

### 3. Submission

1. Commit changes: `git add . && git commit -m "Add: [material name]"`
2. Push to your fork: `git push origin add-new-material`
3. Create a Pull Request with a description of the added material

## Material Format

### Languages

All materials should be bilingual:
- Main content in Russian
- Translation to English
- Metadata in both languages

### Structure

Each material should contain:
- YAML frontmatter with metadata
- Main content in Russian
- Translation to English
- Metadata section at the end of the file

## File Naming Rules

Use the following file naming format:
```
[type]-[title-in-english].md
```

Examples:
- `prompt-marketing-copywriter.md`
- `tool-figma-design-system.md`
- `website-color-palette-generator.md`
- `article-ai-prompt-engineering.md`

## Metadata Structure

Each file must contain the following metadata in YAML frontmatter:

```yaml
---
title: "Title in Russian"
title_en: "Title in English"
description: "Brief description in Russian"
description_en: "Brief description in English"
category: "category"
subcategory: "subcategory"
tags: ["tag1", "tag2", "ru", "en"]
author: "Author Name"
date_created: "YYYY-MM-DD"
date_updated: "YYYY-MM-DD"
language: "both"  # ru, en, both
difficulty: "beginner"  # beginner, intermediate, advanced
rating: 5  # 1-5
external_url: "https://example.com"  # if applicable
---
```

### Required Fields

- `title`, `title_en` - titles in both languages
- `description`, `description_en` - descriptions in both languages
- `category` - one of the main categories
- `tags` - minimum language tags ("ru", "en")
- `author` - author name
- `date_created` - creation date in YYYY-MM-DD format

### Categories

Valid values for `category`:
- `ai-tools` - AI tools and prompts
- `development` - development and programming
- `design` - design and UX/UI
- `useful-resources` - useful resources
- `knowledge-base` - knowledge base and articles

### Subcategories

Valid values for `subcategory` (depend on category):

**ai-tools:**
- `chatgpt-prompts`
- `midjourney-prompts`
- `other-ai-tools`

**development:**
- `code-snippets`
- `libraries`
- `frameworks`

**design:**
- `ui-kits`
- `color-palettes`
- `typography`

**useful-resources:**
- `websites`
- `online-tools`
- `browser-extensions`

**knowledge-base:**
- `tutorials`
- `articles`
- `documentation`

## Pre-submission Checklist

Before creating a Pull Request, make sure:

1. ✅ Material matches the selected template
2. ✅ All metadata is filled correctly
3. ✅ Content is presented in both languages
4. ✅ File is named according to rules
5. ✅ Images are added to the `assets/` folder
6. ✅ No grammatical errors
7. ✅ Links work correctly

## Code of Conduct

- Be polite and respectful to other participants
- Provide quality and useful content
- Respect copyright
- Do not add spam or irrelevant materials

## Questions?

If you have questions about contributing, create an Issue in the repository with the `question` label.

---

Thank you for your contribution to the development of Biblio! 🎉