# devops-ci-project

# DevOps CI/CD Project (Docker + GitHub Actions + Telegram)

## 📌 Описание проекта

Этот проект представляет собой простое веб-приложение на Python (Flask), упакованное в Docker-контейнер и автоматизированное через CI/CD pipeline с использованием GitHub Actions.

При каждом push в репозиторий автоматически выполняется:
- сборка Docker-образа
- проверка успешной сборки
- отправка уведомления в Telegram через Bot API

---

## 🧱 Используемые технологии

- Python 3.11
- Flask
- Docker
- GitHub Actions (CI/CD)
- Telegram Bot API

---

## 🚀 Функциональность приложения

Приложение запускает веб-сервер и отображает сообщение:
* DevOps CI/CD running in Codespaces 🚀


---

## 🐳 Запуск через Docker (локально / Codespaces)

```bash
docker build -t devops-ci-app .
docker run -p 5000:5000 devops-ci-app

После запуска приложение доступно на:
http://localhost:5000


---


## ⚙️ CI/CD (GitHub Actions)

Pipeline запускается автоматически при push в main branch.

### Этапы:
* Checkout репозитория
* Сборка Docker образа
* Отправка уведомления в Telegram

---

## 📩 Telegram уведомления

При успешной сборке отправляется сообщение в Telegram бот.

Используется:

* TELEGRAM_TOKEN (GitHub Secrets)
* TELEGRAM_CHAT_ID (GitHub Secrets)

---

## 🔐 Безопасность
Token хранится в GitHub Secrets
Никогда не хранится в коде
Не попадает в репозиторий
