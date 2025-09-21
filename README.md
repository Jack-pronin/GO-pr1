# Практическая работа 1 Пронин Евгений Анатольевич ЭФМО-01-25

## Описание проекта и требования

Проект реализует минимальный HTTP-сервер на Go с тремя основными маршрутами:

* /hello — возвращает текст "Hello, world!"
* /user — возвращает JSON с сгенерированным UUID и именем "Gopher"
* /health — возвращает JSON с текущим статусом "ok" и временем сервера в формате RFC3339

Сервер позволяет задавать порт через переменную окружения APP_PORT. Если переменная не задана, используется порт 8080 по умолчанию.

---

## Скриншоты

### Версии

<img width="484" height="69" alt="image" src="https://github.com/user-attachments/assets/c322734c-eede-4509-b42f-b1ea6883d85c" />

### Ответы

<img width="628" height="93" alt="image" src="https://github.com/user-attachments/assets/a1ffdc3f-cb04-4b25-8327-482a8131d87a" />

<img width="618" height="100" alt="image" src="https://github.com/user-attachments/assets/14b188db-22c0-403f-9458-b2c058e441a7" />

<img width="623" height="108" alt="image" src="https://github.com/user-attachments/assets/469a4a94-f24c-46af-ab14-ac988f3bfbf0" />



## Требования

* Go 1.25.1
* Git 2.51.0

## Запуск


```
# по умолчанию порт: 8080
go run ./cmd/server

# в реультате будет
Starting on :8080 ...

# другой порт (пример: 8081)
$env:APP_PORT="8081"
go run ./cmd/server

# в результате будет
Starting on :8081 ...
```

##Сборка
