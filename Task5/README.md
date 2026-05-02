# Task5. Проектирование GraphQL API

## Цель

Перевести REST API сервиса `client-info` на GraphQL API, чтобы потребители могли получать только необходимые поля клиентской карточки и не выполнять несколько REST-запросов в рамках одного сценария.

## Анализ существующего REST API

Существующий Swagger-контракт содержит три основных endpoint:

```http
GET /clients/{id}
GET /clients/{id}/documents
GET /clients/{id}/relatives