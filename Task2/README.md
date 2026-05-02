# Task2. Динамическое масштабирование контейнеров

## Цель

Настроить динамическое масштабирование приложения в Kubernetes.

В рамках задания проверяются два сценария:

1. Масштабирование по утилизации оперативной памяти.
2. Масштабирование по количеству запросов в секунду через Prometheus.

## Тестовое приложение

Тестовое приложение предоставляет два endpoint:

- `GET /` — возвращает идентификатор pod;
- `GET /metrics` — возвращает метрики в формате Prometheus.

Приложение доступно на порту `8080`.

## Структура директории

```text
Task2/
  README.md
  deployment.yaml
  service.yaml
  hpa-memory.yaml
  locustfile.py
  prometheus-values.yaml
  service-monitor.yaml
  prometheus-adapter-values.yaml
  hpa-rps.yaml
  screenshots/