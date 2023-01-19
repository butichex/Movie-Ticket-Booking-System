# Movie-Ticket-Booking-System
 Бэкенд сервиса, который помогает посетителям кинотеатра посмотреть предстоящие сеансы и забронировать их.

## Установка

- Установите Python3.9.5
- Установите зависимости через `pip install -r requirements.txt`

## Создание файла зависимостей

- pip3 freeze > requirements.txt

## Запуск Virtual ENV

- source venv/bin/activate

## Запуск приложения

- python app.py

## Сущности БД

<table><thead><tr><th>Table Name</th><th>Columns</th></tr></thead><tbody><tr><td>movie</td><td>id (Integer, primary key), created_at (DateTime), name (String(100)), lang (String(10)), description (Text), poster_url (Text), trailer_url (Text), duration (Integer), is_blockbuster (Boolean), last_screening_id (Integer, foreign key referencing <code>screening.id</code>), last_screening_timing (DateTime)</td></tr><tr><td>screening</td><td>id (Integer, primary key), created_at (DateTime), movie_id (Integer, foreign key referencing <code>movie.id</code>), timing (DateTime)</td></tr><tr><td>booking</td><td>id (Integer, primary key), created_at (DateTime), status (Boolean), user_id (Integer, foreign key referencing <code>user.id</code>), user_name (String(100)), movie_id (Integer, foreign key referencing <code>movie.id</code>), movie_name (String(100)), screening_id (Integer, foreign key referencing <code>screening.id</code>), screening_time (DateTime), number_seats (Integer)</td></tr></tbody></table>
