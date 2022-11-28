# Тестовое задание с использованием Striple

Задание:
1. `GET /buy/{id}`, c помощью которого можно получить Stripe Session Id для оплаты выбранного Item. При выполнении этого метода c бэкенда с помощью python библиотеки stripe должен выполняться запрос stripe.checkout.Session.create(...) и полученный session.id выдаваться в результате запроса
2. `GET /item/{id}`, c помощью которого можно получить простейшую HTML страницу, на которой будет информация о выбранном Item и кнопка Buy. По нажатию на кнопку Buy должен происходить запрос на /buy/{id}, получение session_id и далее  с помощью JS библиотеки Stripe происходить редирект на Checkout форму stripe.redirectToCheckout(sessionId=session_id)


### Копирование репозитория и установка зависимостей
*  #### git clone https://github.com/Battal99/stripe_api
*  #### cd stripe_api
* #### virtualenv venv
* #### source venv/bin/activate
* #### pip install -r requirements.txt

### Установить environment variables в папке project_api_stripe
создать файл .env и заполнить eго ключами
1. #### STRIPE_SK = <stripe_sk>
2. #### SECRET_KEY = <secret_key>
3. #### STRIPE_PUBLIC_KEY = <your_public_key>

### Применение миграций, создания суперпользователя и запуск проекта
- #### python manage.py migrate
- #### python manage.py createsuperuser
- #### python manage.py runserver

### Команда для запуска через docker
#### docker-compose up --build
