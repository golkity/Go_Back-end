


```shell
go get -u github.com/gin-gonic/gin
go get -u github.com/labstack/echo/v4

go get -u gorm.io/gorm
go get -u gorm.io/driver/postgres
go get -u gorm.io/driver/mysql    

go get -u github.com/jackc/pgx/v5
go get -u github.com/golang-jwt/jwt/v5
go get -u github.com/go-playground/validator/v10
go get -u github.com/sirupsen/logrus
go get -u github.com/grsmv/timeutil
go get -u github.com/robfig/cron/v3
go get -u github.com/go-gomail/gomail
go get -u github.com/go-telegram-bot-api/telegram-bot-api/v5
go get -u github.com/stretchr/testify

go install github.com/swaggo/swag/cmd/swag@latest
go get -u github.com/swaggo/gin-swagger
go get -u github.com/swaggo/files
go get -u github.com/redis/go-redis/v9
go get -u github.com/go-resty/resty/v2
```

# Инициализация модуля
```shell
go mod init booking-service
```
# Запуск приложения
```shell
go run cmd/main.go
```

```
booking-service/
    ├── cmd/                    # Точка входа
    │   └── main.go             # Запуск приложения
    ├── configs/                # Конфигурации
    │   └── config.yaml         # Настройки (порты, база данных, API-ключи)
    ├── internal/               # Основная логика
    │   ├── auth/               # Аутентификация и авторизация
    │   │   ├── middleware.go   # JWT или OAuth2 middleware
    │   │   └── auth.go         # Логика авторизации
    │   ├── booking/            # Модуль бронирований
    │   │   ├── handler.go      # HTTP-обработчики
    │   │   ├── service.go      # Логика бронирования
    │   │   └── repository.go   # Доступ к базе данных
    │   ├── resource/           # Модуль ресурсов (комнаты, столики)
    │   │   ├── handler.go      # HTTP-обработчики
    │   │   ├── service.go      # Логика управления ресурсами
    │   │   └── repository.go   # Доступ к базе данных
    │   └── utils/              # Утилиты
    │       ├── logger.go       # Логирование
    │       └── validation.go   # Проверка входных данных
    ├── migrations/             # Скрипты для создания таблиц
    ├── pkg/                    # Вспомогательные пакеты (переиспользуемые)
    ├── test/                   # Тесты
    │   ├── booking_test.go     # Юнит-тесты модуля бронирования
    │   └── auth_test.go        # Тесты авторизации
    ├── go.mod                  # Модуль Go
    ├── go.sum                  # Зависимости
    └── README.md               # Документация

```