# Веб-сервис Аренды вещей на Java Spring Boot
Стек - Java, Spring Boot, PostgreSQL, JPA, Hibernate ORM, Maven, Lombok, Docker, REST API, Mockito, JUnit, Lombok.

## О проекте
Пользователи могут арендовать и отдавать в аренду свои вещи, оставлять заявки на отсутствующие в каталоге вещи, осуществалять поиск вещей по параметрам и комментировать завершенные аренды.

## Основная функциональность
- POST /users - добавление пользователя
- PATCH /users/{userId} - обновление данных пользователя
- GET /users/{userId} - получение данных пользователя
- GET /users/ - получение списка пользователей

- POST /items - добавление вещи
- PATCH /items/{itemId} - обновление данных вещи
- GET /items/{itemId} - получение данных вещи
- GET /items/ - получение списка вещей
- GET /items/search - поиск вещей по тексту в параметре text
- POST /items/{itemId}/comment - добавление отзыва к вещи после завершенного бронирования

- POST /requests - добавление запроса на бронирование
- GET /requests/{requestId} - получение бронирования
- GET /items/all - получение списка бронирований
- GET /items - получение списка бронирований по id пользователя в заголовке запроса

- PATCH /bookings/{bookingId} - обновление данных бронирования
- PATCH /bookings/{bookingId} - одобрение или отклонение бронирования по параметру approved
- GET /bookings/{bookingId} - получение данных о бронировании
- GET /bookings/ - получение бронирований по фильтрам state, from, size
- GET /bookings/owner - получение бронирований пользователя по фильтрам state, from, size

## Микросервисная архитектура
Docker контейнеры под каждый микросервис:
* Gateway - для валидации запросов
* Server - содержbn бизнес-логику
* PostgreSQL - база данных

## Схема БД

## Postman тесты
