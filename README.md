
# SmartScheduler

Модуль составления и динамического расписания занятий и аудиторий.

## 🎯 Концепция

Система автоматически распределяет занятия по аудиториям с учётом:
- вместимости и оснащения аудиторий;
- доступности преподавателей;
- учебных групп;
- конфликтов по времени.

Администратор может менять расписание в реальном времени, а система предлагает варианты перестроения.

## 🛠 Стек

- **Backend:** Node.js 20 + Express + TypeScript
- **Frontend:** React 18 + Vite + Tailwind CSS
- **БД:** PostgreSQL 15 + Prisma
- **Тесты:** Jest

## 📦 Структура

```
src/       — серверная логика
client/    — React-приложение
prisma/    — схема БД и миграции
tests/     — тесты
.github/   — шаблоны Issue/PR и CI
```

## 🚀 Запуск

```bash
git clone https://github.com/kito05/smart-scheduler.git
cd smart-scheduler
npm install
cp .env.example .env
npx prisma migrate dev
npm run dev
```

Приложение: `http://localhost:3000`

## 📜 Скрипты

| Команда | Назначение |
|---|---|
| `npm run dev` | Запуск с hot-reload |
| `npm run build` | Сборка |
| `npm run test` | Тесты |
| `npm run lint` | Линтер |

## 📄 Лицензия

MIT
