# Select Vacancies API

Production-ready приложение на **FastAPI + Docker + PostgreSQL** с автоматическим парсингом вакансий каждые 5 минут (APScheduler).

### Что было исправлено (8 багов):
- Опечатка в Pydantic Settings (`DATABSE` → `DATABASE`)
- `bash` → `sh` в python:3.11-slim
- Правильный `sqlalchemy.url` в `alembic.ini`
- Исправлена вложенность папок в Dockerfile
- Удалены битые версии в `requirements.txt`
- Улучшен healthcheck PostgreSQL
- Обработка `NoneType` в парсере (`city.name`)
- Другие мелкие правки

### Как запустить:
```bash
docker compose up --build

Swagger: http://localhost:8000/docs
Эндпоинт: GET /api/v1/vacancies/
Отчёт по отладке: Grigoryan_report.pdf
