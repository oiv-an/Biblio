# Инструкции по созданию репозитория Biblio на GitHub

## Шаг 1: Создание репозитория на GitHub

1. Перейдите на сайт [GitHub](https://github.com)
2. Войдите в свой аккаунт или создайте новый
3. Нажмите на кнопку "+" в правом верхнем углу и выберите "New repository"
4. Введите название репозитория: **Biblio**
5. Выберите "Public" (открытый репозиторий)
6. Отметьте галочкой "Add a README file" (можно не отмечать, так как у нас уже есть README)
7. Нажмите "Create repository"

## Шаг 2: Связывание локального репозитория с удалённым

После создания репозитория на GitHub, выполните в терминале следующие команды:

```bash
# Ваш никнейм на GitHub: oiv-an
git remote add origin https://github.com/oiv-an/Biblio.git

# Отправка кода на GitHub
git push -u origin master
```

## Шаг 3: Проверка загрузки

1. Перейдите на страницу вашего репозитория: `https://github.com/oiv-an/Biblio`
2. Убедитесь, что все файлы загрузились корректно
3. Проверьте, что README.md отображается правильно

## Альтернативный способ (если команды выше не работают)

Если возникли проблемы с push, можно попробовать:

```bash
# Принудительная отправка (используйте осторожно)
git push -f origin master

# Или сначала pull, затем push
git pull origin master --allow-unrelated-histories
git push origin master
```

## Что должно получиться

После успешной загрузки вы увидите:
- Все файлы проекта в репозитории
- Правильную структуру директорий
- README.md как главную страницу репозитория
- LICENSE файл
- Все категории и примеры контента

## Следующие шаги

После загрузки репозитория:

1. **Настройте GitHub Pages** (опционально):
   - Перейдите в Settings → Pages
   - Выберите "Deploy from a branch"
   - Выберите ветку "master" и папку "/root"
   - Сохраните настройки

2. **Добавьте описание репозитория**:
   - На главной странице репозитория нажмите на иконку шестерёнки
   - Добавьте описание: "Открытая библиотека знаний, промптов, полезных ресурсов и инструментов"

3. **Добавьте темы**:
   - В поле Topics добавьте: `knowledge-library`, `prompts`, `ai-tools`, `resources`, `bilingual`

## Полезные ссылки

- [Документация GitHub](https://docs.github.com/ru)
- [GitHub Pages](https://pages.github.com/)
- [Markdown руководство](https://docs.github.com/ru/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

---

После выполнения этих шагов ваш репозиторий Biblio будет полностью готов к использованию!