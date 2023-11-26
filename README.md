Інструкція по Запуску


Білд Docker Image
docker build -t web-server .
Запуск Docker Container
docker run -d -p 5000:5000 web-server



Перевірка
Перейдіть за адресою http://localhost:3000 для перевірки додатку.

Запуск Бази Даних



Запуск контейнера
docker run -d -p 3306:3306 --name mysql -e MYSQL_ROOT_PASSWORD=password mysql


Підключення до Бази
docker exec -it mysql mysql -u root -p


Зупинка контейнера
docker stop mysql


Запуск існуючого контейнера
docker start mysql
