Частина 1: Створення Git Репозиторію з Додатком та Dockerfile
Створення GitHub Репозиторію:

Увійдіть на GitHub та створіть новий репозиторій.
Підготовка Вихідного Коду Додатку:

Виберіть простий додаток, наприклад, HTTP сервер.
Завантажте вихідний код у ваш локальний репозиторій.
Написання Dockerfile:

У кореневій директорії вашого проекту створіть Dockerfile.
Встановіть базовий образ, додайте команди для запуску додатку і вкажіть використовуваний порт. Наприклад:

FROM node:14
COPY . /app
WORKDIR /app
RUN npm install
EXPOSE 3000
CMD ["node", "server.js"]
Інструкція для Білду та Запуску:

Створіть README.md.
Опишіть процес створення Docker Image та запуску контейнера. Наприклад:
perl
Copy code
# Запуск Додатку

## Створення Docker Image
docker build -t my-http-server .

## Запуск Docker Container
docker run -d -p 3000:3000 my-http-server

## Перевірка
Відкрийте http://localhost:3000 в браузері.
Запуште Код у Репозиторій:

Використайте Git для додавання, комітування та пушу коду та Dockerfile на GitHub.
Частина 2: Інструкція для Запуску Бази Даних в Docker
Dockerfile для Бази Даних:

Якщо ви використовуєте популярну базу даних, як PostgreSQL, можете використовувати готовий образ.
В Dockerfile або docker-compose.yml встановіть необхідні налаштування.
Інструкція для Бази Даних:

Додайте секцію у README.md:
shell

## Запуск PostgreSQL

### Створення контейнера
docker run -d -p 5432:5432 --name postgres -e POSTGRES_PASSWORD=password postgres

### Підключення до Бази
docker exec -it postgres psql -U postgres

### Зупинка контейнера
docker stop postgres

### Запуск існуючого контейнера
docker start postgres

## Перевірка Збереження Даних
