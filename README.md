# -..
модуль составления и динамического расписания занятий и аудиторий.
# SmartScheduler

Модуль составления и динамического расписания занятий и аудиторий для учебных заведений.

## 🎯 Концепция

SmartScheduler автоматически распределяет занятия по аудиториям с учётом:

- вместимости и оснащения аудиторий (проектор, ПК, лаборатория);
- доступности преподавателей и их пожеланий по времени;
- учебных групп и потоков;
- конфликтов по времени и месту (нельзя две пары в одной аудитории одновременно).

Администратор может вносить изменения в реальном времени (отмена занятия, замена преподавателя), а система автоматически предлагает варианты перестроения расписания.

## 🛠 Технологический стек

| Компонент | Технология |
|---|---|
| Язык | TypeScript (Node.js 20) |
| Backend | Express.js |
| Frontend | React 18 + Vite + Tailwind CSS |
| База данных | PostgreSQL 15 |
| ORM | Prisma |
| Тесты | Jest + Supertest |
| CI | GitHub Actions |

## 📦 Структура проекта

```
SmartScheduler/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.md
│   │   └── feature_request.md
│   └── PULL_REQUEST_TEMPLATE.md
├── prisma/
│   ├── schema.prisma
│   └── migrations/
├── src/
│   ├── config/
│   ├── controllers/
│   ├── services/
│   ├── routes/
│   ├── middleware/
│   ├── utils/
│   └── index.ts
├── client/
│   ├── src/
│   └── vite.config.ts
├── tests/
├── .env.example
├── .gitignore
├── package.json
├── tsconfig.json
└── README.md
```

## 🚀 Быстрый старт

### Требования

- Node.js 20+
- PostgreSQL 15+
- npm 10+

### Установка

```bash
# 1. Клонировать репозиторий
git clone https://github.com/kito05/smart-scheduler.git
cd smart-scheduler

# 2. Установить зависимости
npm install

# 3. Настроить переменные окружения
cp .env.example .env
# отредактировать .env (DATABASE_URL, JWT_SECRET)

# 4. Применить миграции БД
npx prisma migrate dev

# 5. Запустить в режиме разработки
npm run dev
```

Приложение будет доступно по адресу: `http://localhost:3000`

## 📜 Скрипты

| Команда | Назначение |
|---|---|
| `npm run dev` | Запуск с hot-reload |
| `npm run build` | Сборка продакшен-версии |
| `npm start` | Запуск собранного приложения |
| `npm run test` | Запуск тестов |
| `npm run lint` | Проверка кода линтером |

## 🔐 Переменные окружения

Все переменные описаны в `.env.example`. Основные:

| Переменная | Описание |
|---|---|
| `DATABASE_URL` | Строка подключения к PostgreSQL |
| `PORT` | Порт сервера (по умолчанию 3000) |
| `JWT_SECRET` | Секрет для подписи токенов |
| `NODE_ENV` | `development` / `production` |

## 🤝 Участие в разработке

1. Создайте ветку: `git checkout -b feature/название-фичи`
2. Внесите изменения и закоммитьте: `git commit -m "feat: добавил ..."`
3. Отправьте в удалённый репозиторий: `git push origin feature/название-фичи`
4. Откройте Pull Request в `main`

Перед PR убедитесь, что проходят тесты и линтер: `npm run test && npm run lint`

## 📄 Лицензия

Проект распространяется под лицензией MIT. См. файл [LICENSE](LICENSE).
