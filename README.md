# Personal AI Hub Gateway

Self-hosted платформа для создания личного AI-ассистента с использованием Docker, NextChat и балансировщика OpenRouter. Проект позволяет использовать топовые нейросети (Gemini 2.0, Llama 3.3, DeepSeek) абсолютно бесплатно, обходя региональные ограничения.

## 🏗 Архитектура

Проект построен по принципу API-шлюза с изолированным сетевым контуром:
1. **Frontend / Backend:** `chatgpt-next-web` в Docker-контейнере.
2. **API Gateway:** OpenRouter.ai (маршрутизация к бесплатным LLM).
3. **Network Routing:** Локальный SOCKS5-туннель (Wireproxy / Cloudflare WARP) для обхода региональных блокировок Google/Meta.
4. **Security:** Zero Trust авторизация (доступ только по заранее заданным Access Codes).

## 🚀 Особенности
* Полная изоляция в Docker.
* Горячее переключение моделей через UI (без перезагрузки сервера).
* Защита от утечки лимитов (HIDE_USER_API_KEY).
* Развертывание в одну команду.

## 🛠 Установка и запуск

1. Клонируйте репозиторий:
   ```bash
   git clone [https://github.com/Ubertin0/personal-ai-hub.git](https://github.com/Ubertin0/personal-ai-hub.git)
   cd personal-ai-hub