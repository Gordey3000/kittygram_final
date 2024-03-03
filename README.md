## Kittygram
### Описание
Данный проект служит интернет-площадкой для котоводов, где владельцы своих котиков могут выставлять их на показ включая имя, цвет, дату рождения и даже фото, а так же отмечать достижения кота. Благодаря данному ресурсу хозяева кошачих смогут создать реестр своих питомцев.

### Инструменты и стек: 
#Python #Django #Docker-compose #API #Nginx #Pillow #Djoser #Gunicorn #Python-dotenv #JSON #YAML #Postman #PyCharm

### Запуск
Для запуска приложения необходим сервер, рассмотрим на примере сервера под управлением ОС Linux.

Подготовим виртуальное окружение в директории проекта создадим файл .env:
nano .env
Добавляем следующие переменные:
POSTGRES_DB=kittygram
POSTGRES_USER=kittygram_user
POSTGRES_PASSWORD=kittygram_password
DB_HOST=db
DB_PORT=5432
SECRET_KEY=...
DEBUG=... # True/False
ALLOWED_HOSTS=127.0.0.1,localhost
Устанавливаем к Docker утилиту Docker Compose:
sudo apt update
sudo apt-get install docker-compose-plugin 
В директорию проекта копируем файл docker-compose.production.yml и запускаем Docker Compose:
sudo docker-compose up
Примеры запросов
Добавить питомца: POST /cats/add

Редактировать питомца: PUTCH /cats/edit

Просмотр питомца: GET /cats/{cat_id}
