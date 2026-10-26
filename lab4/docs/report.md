# Отчёт по лабораторной работе №4 (n8n)

## 1. Краткое описание выполненного
В ходе работы я установила n8n через Docker, освоила создание workflow (ручной запуск, Code, IF, Set, 
HTTP Request, Schedule), а также настроила Redis через Docker и реализовала два workflow для 
создания/чтения и удаления ключа.

## 2. Использованные AI-промпты
- «Как в n8n настроить ноду Code, чтобы она возвращала объект с полем payload?»
- «Как в n8n настроить IF-ноду для ветвления по числу (больше 20)?»
- «Как подключить Redis к n8n через Docker (host.docker.internal)?»
- «Напиши workflow для Redis: Set ключа, затем Get этого ключа».

## 3. Освоенные ноды
- **Manual Trigger** — ручной запуск.
- **Code** — выполнение JS (let, const, if/else, циклы, массивы).
- **IF** — ветвление.
- **Edit Fields (Set)** — изменение полей (topic, timestamp, payload).
- **HTTP Request** — GET-запрос к API.
- **Schedule Trigger** — запуск по расписанию.
- **Redis** — Set, Get, Delete.
- **NoOp** — «пустая» нода для завершения.

## 4. Скриншоты
Все скриншоты в папке `screenshots/`:
- `01-version.png` — n8n запущен.
- `01-manual-set.png` — flow 2.1 (Manual → Set → Code).
- `02-code.png` — flow 2.2 (Code).
- `03-if.png` — flow 2.3 (IF).
- `04-set.png` — flow 2.4 (Set).
- `05-http.png` — flow 2.5 (HTTP Request).
- `06-schedule.png` — flow 2.6 (Schedule).
- `07-redis-credentials.png` — настройка Redis credentials.
- `08-redis-create-read.png` — Redis Set + Get.
- `09-redis-delete.png` — Redis Delete + Get (проверка).

## 5. Выводы
В ходе работы я освоила n8n как low-code платформу для автоматизации. Поняла, как работают ноды 
и как передаются данные между ними (через JSON). Самым интересным было настроить Redis: я увидела, 
как приложение может хранить данные в отдельной базе и удалять их по запросу. Работа 
с Docker стала понятнее: контейнеры изолируют сервисы, но могут общаться друг с другом через сеть.
