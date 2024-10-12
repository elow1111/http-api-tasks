# Виды API

В этом упражнении мы познакомимся с тем, как работает [JSON RPC](https://ru.wikipedia.org/wiki/JSON-RPC).

Пример запроса:

```
curl -X POST \
 -H 'Content-Type: application/json' \
 -d '{"jsonrpc":"2.0","id":1,"method":"echo","params":{"text": "Hello, World!"}}' \
 http://localhost:8080/rpc
```

## greet

Метод `greet` принимает параметр `name` и отправляет в ответ приветствие.

- Используя _curl_, выполните запрос к _localhost_ на порт 8080 по пути `/json-rpc`. Передайте в теле запроса метод `greet` и параметр `name` со значением `Tota`.
- Запишите получившуюся команду в файл _greet_.

## get_users

Метод `get_users` возвращает в ответ список пользователей.

Используя _curl_, выполните запрос к _localhost_ на порт 8080 по пути `/json-rpc`. Передайте в теле запроса метод `get_users`. Данный метод не принимает никаких параметров.
Запишите получившуюся команду в файл _get_users_.

## Подсказки

- Не забудьте указать `id` в теле запроса, этого требует спецификация.