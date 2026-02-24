Стек технологий: Python 3.11-slim (Django), Nginx (Reverse Proxy), Docker & Docker Compose 
Разработка велась в PyCharm и Docker Desktop. Использование подсистемы WSL2 позволило достичь нативной производительности Linux-контейнеров в ОС Windows
Архитектура проекта:
Запросы проходят через Nginx (порт 80), который проксирует их на внутренний сервис backend (порт 8080).
User (Port 80) -> Nginx Container -> Backend Container (Port 8080)
Структура проекта:
learn/
    backend/
        polls/
        store/
        db.sqlite3
        Dockerfile
        manage.py
        requirements.txt
    nginx/
    .gitignore
    docker-compose.yml
    README.md
Как запустить:
Склонируйте репозиторий.
Выполните команду: docker-compose up --build
Как проверить результат: откройте http://localhost или выполните команду curl http://localhost
Ожидаемый ответ: Hello from Effective Mobile!
