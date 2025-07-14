# Saturn Wiki

Документация Saturn VPN на базе VitePress.

## 🚀 Быстрый старт

### Локальная разработка

```bash
# Установка зависимостей
npm install

# Запуск dev сервера
npm run dev
```

Сайт будет доступен по адресу: http://localhost:8888

### Сборка для продакшена

```bash
npm run build
```

## 📚 Деплой на GitHub Pages

### Настройка репозитория

1. **Создайте репозиторий на GitHub**
2. **Загрузите файлы:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/ВАШ-USERNAME/НАЗВАНИЕ-РЕПО.git
   git push -u origin main
   ```

3. **Настройте GitHub Pages:**
   - Перейдите в Settings → Pages
   - Source: "GitHub Actions"

4. **Обновите конфигурацию:**
   
   В файле `.vitepress/config.js` измените:
   ```js
   // Если репозиторий называется "saturn-wiki"
   base: '/saturn-wiki/',
   
   // Замените все URL с 'saturn-network.com' на:
   // https://ВАШ-USERNAME.github.io/НАЗВАНИЕ-РЕПО/
   ```

### Автоматический деплой

После пуша в ветку `main` сайт автоматически соберется и задеплоится через GitHub Actions.

Ваш сайт будет доступен по адресу:
`https://ВАШ-USERNAME.github.io/НАЗВАНИЕ-РЕПО/`

## 🛠️ Структура проекта

```
wiki/
├── .github/workflows/    # GitHub Actions для деплоя
├── .vitepress/          # Конфигурация VitePress
│   ├── config.js        # Основная конфигурация
│   └── theme/           # Кастомная тема
├── bot-guide/           # Документация бота
├── setup-guide/         # Инструкции по настройке
├── troubleshoot/        # Устранение проблем
└── public/              # Статические файлы
```

## 📝 Редактирование контента

Все страницы написаны в Markdown. Основные разделы:

- `/bot-guide/` - Документация Telegram бота
- `/setup-guide/` - Инструкции по установке приложений
- `/troubleshoot/` - Решение проблем

## 🎨 Кастомизация

Проект использует кастомную тему VitePress с:
- Адаптивным дизайном
- Поддержкой темной темы
- SEO оптимизацией
- Увеличением изображений при клике
- Компактными карточками приложений

## 🔧 Технологии

- **VitePress** - Генератор статических сайтов
- **Vue.js** - Для интерактивных компонентов
- **GitHub Actions** - Автоматический деплой
- **GitHub Pages** - Хостинг 