Данный проект - сервис для подсчёта арифметических выражений.
Он представляет собой веб-сервис в котором пользователь отправляет арифметическое выражение по HTTP и получает в ответ его результат.

##### Приложение поддерживает post запросы с json формата {"expression": "ваше выражение"}
### Пример работы
##### status code 200
```bash
curl --location http://localhost:8080/api/v1/calculate --header 'Content-Type: application/json' --data '{"expression": "2+2*2"}'
```
##### status code 422
```bash
curl --location http://localhost:8080/api/v1/calculate --header 'Content-Type: application/json' --data '{"expression": "2+2*2/0"}'
```
