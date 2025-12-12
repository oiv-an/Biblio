---
title: "Debounce функция на JavaScript"
title_en: "JavaScript Debounce Function"
description: "Универсальная debounce функция для оптимизации обработки событий"
description_en: "Universal debounce function for optimizing event handling"
category: "development"
subcategory: "code-snippets"
tags: ["code", "javascript", "snippet", "performance", "optimization", "ru", "en"]
author: "Ivan Olyanskiy"
date_created: "2025-12-12"
date_updated: "2025-12-12"
language: "both"
difficulty: "intermediate"
rating: 5
external_url: ""
---

## Описание / Description

Debounce - это техника программирования, которая откладывает выполнение функции до тех пор, пока не пройдёт определённое время с момента последнего вызова. Это особенно полезно для оптимизации обработки событий, таких как ввод текста, изменение размера окна или прокрутка.

Debounce is a programming technique that delays the execution of a function until a certain amount of time has passed since the last call. This is especially useful for optimizing event handling, such as text input, window resizing, or scrolling.

## Код / Code

### Базовая реализация / Basic Implementation

```javascript
/**
 * Debounce функция
 * @param {Function} func - Функция для debounce
 * @param {number} wait - Время задержки в миллисекундах
 * @returns {Function} - Debounce версия функции
 */
function debounce(func, wait) {
  let timeout;
  
  return function executedFunction(...args) {
    const later = () => {
      clearTimeout(timeout);
      func(...args);
    };
    
    clearTimeout(timeout);
    timeout = setTimeout(later, wait);
  };
}

/**
 * Debounce function
 * @param {Function} func - Function to debounce
 * @param {number} wait - Delay time in milliseconds
 * @returns {Function} - Debounced version of the function
 */
function debounce(func, wait) {
  let timeout;
  
  return function executedFunction(...args) {
    const later = () => {
      clearTimeout(timeout);
      func(...args);
    };
    
    clearTimeout(timeout);
    timeout = setTimeout(later, wait);
  };
}
```

### Продвинутая реализация с immediate / Advanced Implementation with Immediate

```javascript
/**
 * Debounce функция с опцией immediate
 * @param {Function} func - Функция для debounce
 * @param {number} wait - Время задержки в миллисекундах
 * @param {boolean} immediate - Выполнить сразу при первом вызове
 * @returns {Function} - Debounce версия функции
 */
function debounce(func, wait, immediate = false) {
  let timeout;
  
  return function executedFunction(...args) {
    const callNow = immediate && !timeout;
    
    clearTimeout(timeout);
    timeout = setTimeout(() => {
      timeout = null;
      if (!immediate) func(...args);
    }, wait);
    
    if (callNow) func(...args);
  };
}

/**
 * Debounce function with immediate option
 * @param {Function} func - Function to debounce
 * @param {number} wait - Delay time in milliseconds
 * @param {boolean} immediate - Execute immediately on first call
 * @returns {Function} - Debounced version of the function
 */
function debounce(func, wait, immediate = false) {
  let timeout;
  
  return function executedFunction(...args) {
    const callNow = immediate && !timeout;
    
    clearTimeout(timeout);
    timeout = setTimeout(() => {
      timeout = null;
      if (!immediate) func(...args);
    }, wait);
    
    if (callNow) func(...args);
  };
}
```

## Примеры использования / Usage Examples

### Поиск при вводе текста / Search on Text Input

```javascript
const searchInput = document.getElementById('search');
const searchResults = document.getElementById('results');

// Функция поиска / Search function
function performSearch(query) {
  console.log('Searching for:', query);
  // Здесь код для выполнения поиска / Code for performing search
}

// Создаем debounce версию / Create debounced version
const debouncedSearch = debounce(performSearch, 300);

// Добавляем обработчик события / Add event listener
searchInput.addEventListener('input', (e) => {
  debouncedSearch(e.target.value);
});
```

### Изменение размера окна / Window Resize

```javascript
// Функция обработки изменения размера / Resize handler function
function handleResize() {
  console.log('Window resized:', window.innerWidth, window.innerHeight);
  // Код для адаптации интерфейса / Code for adapting interface
}

// Создаем debounce версию / Create debounced version
const debouncedResize = debounce(handleResize, 250);

// Добавляем обработчик события / Add event listener
window.addEventListener('resize', debouncedResize);
```

## Советы / Tips

- Используйте debounce для событий, которые происходят часто: `input`, `resize`, `scroll`
- Выбирайте задержку в зависимости от контекста: 100-300ms для поиска, 250-500ms для resize
- Используйте опцию `immediate: true`, если функция должна выполниться сразу при первом вызове

- Use debounce for events that occur frequently: `input`, `resize`, `scroll`
- Choose delay depending on context: 100-300ms for search, 250-500ms for resize
- Use `immediate: true` option if the function should execute immediately on first call

## Вариации / Variations

### TypeScript версия / TypeScript Version

```typescript
function debounce<T extends (...args: any[]) => any>(
  func: T,
  wait: number,
  immediate?: boolean
): (...args: Parameters<T>) => void {
  let timeout: NodeJS.Timeout | null = null;
  
  return function executedFunction(...args: Parameters<T>) {
    const callNow = immediate && !timeout;
    
    if (timeout) clearTimeout(timeout);
    timeout = setTimeout(() => {
      timeout = null;
      if (!immediate) func(...args);
    }, wait);
    
    if (callNow) func(...args);
  };
}
```

## Связанные материалы / Related Materials

- [Throttle функция на JavaScript](snippet-javascript-throttle.md)
- [JavaScript Throttle Function](snippet-javascript-throttle.md)
- [Оптимизация производительности в JavaScript](../../articles/javascript-performance.md)
- [JavaScript Performance Optimization](../../articles/javascript-performance.md)

---

## Метаданные / Metadata

- **Автор / Author:** Ivan Olyanskiy
- **Дата создания / Created:** 2025-12-12
- **Обновлено / Updated:** 2025-12-12
- **Категория / Category:** development
- **Подкатегория / Subcategory:** code-snippets
- **Теги / Tags:** code, javascript, snippet, performance, optimization, ru, en
- **Сложность / Difficulty:** intermediate
- **Рейтинг / Rating:** 5/5