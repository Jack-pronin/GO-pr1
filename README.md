# Практическая работа №1 Пронин Евгений Анатольевич ЭФМО-01-25

## Описание проекта и требования

Проект реализует минимальный HTTP-сервер на Go с тремя основными маршрутами:

* ```/hello``` — возвращает текст "Hello, world!"
* ```/user``` — возвращает JSON с сгенерированным UUID и именем "Gopher"
* ```/health``` — возвращает JSON с текущим статусом "ok" и временем сервера в формате RFC3339

Сервер позволяет задавать порт через переменную окружения APP_PORT. Если переменная не задана, используется порт 8080 по умолчанию.

---

## Скриншоты

### Версии

<img width="484" height="69" alt="image" src="https://github.com/user-attachments/assets/c322734c-eede-4509-b42f-b1ea6883d85c" />

### Ответы

<img width="620" height="240" alt="image" src="https://github.com/user-attachments/assets/4c1198b3-084f-4056-a755-090cddb8be6d" />


<img width="620" height="240" alt="image" src="https://github.com/user-attachments/assets/33554ad6-4cd7-4fb1-9223-0c800bd391c9" />


<img width="620" height="240" alt="image" src="https://github.com/user-attachments/assets/000557ac-0976-49bb-8e54-7120fa0358fd" />



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

## Сборка

```
go build -o helloapi.exe ./cmd/server
./helloapi.exe
```

## Эндпоинты

```
# 1) /hello → text/plain
curl http://localhost:8080/hello

# 2) /user → application/json { "id": "<uuid>", "name": "..." }
curl http://localhost:8080/user

# 3) /health → application/json { "status":"ok", "time":"<RFC3339>" }
curl http://localhost:8080/health
```

## Конфигурация

```APP_PORT``` — порт HTTP-сервера (строка без двоеточия, например ```8080```). Если не задана — используется ```8080```.

## Проверка качества
```
go fmt ./...
go vet ./...
```
Ожидаемо — без предупреждений.

## Структура проекта

```
helloapi/
  cmd/
    server/
      main.go
  go.mod
  go.sum   
```
