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
```

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
## app running
<img width="1630" height="682" alt="image" src="https://github.com/user-attachments/assets/92b468a5-f3fe-407b-9847-cd46a4bea2de" />

---

## build container
<img width="1732" height="561" alt="image" src="https://github.com/user-attachments/assets/412fcd75-b472-43f9-ba65-f9c20bba2bb3" />

---

## run container
<img width="1736" height="390" alt="image" src="https://github.com/user-attachments/assets/94ec7298-b886-4091-a155-bb3a74915c0f" />
<img width="1095" height="208" alt="image" src="https://github.com/user-attachments/assets/57a9a229-3893-4f5b-8210-0ea157601890" />

---

## GITHUB ACTIONS SUCCESS pipeline
<img width="1261" height="1153" alt="image" src="https://github.com/user-attachments/assets/9cd5ede2-d539-4980-8257-b682c55a8f29" />

---

## Telegram message

<img width="1626" height="1171" alt="image" src="https://github.com/user-attachments/assets/8630d4f5-0398-45dd-a195-ebe5eed0782e" />








---

## 🔐 Безопасность
Token хранится в GitHub Secrets
Никогда не хранится в коде
Не попадает в репозиторий
