# Система регистрации и авторизации пользователей

Веб-приложение на ASP.NET Core с использованием Identity, PostgreSQL и Bootstrap.

## Особенности системы

- Регистрация и авторизация пользователей
- Использование локальной базы данных PostgreSQL
- Защита от SQL-инъекций
- Хранение сессий через Cookies
- Современный UI с использованием Bootstrap

## Требования

- .NET 9.0+
- PostgreSQL 16.0+

## Настройка и запуск

### 1. Настройка базы данных PostgreSQL

1. Запустите dockerfile
2. При необходимости, измените строку подключения в файле `appsettings.json`:
   ```json
   "ConnectionStrings": {
     "DefaultConnection": "Host=localhost;Port=5432;Database=authapp;Username=postgres;Password=postgres"
   }
   ```

### 2. Запуск приложения

   ```
   dotnet build && dotnet run
   ```

## Структура проекта

- `Areas/Identity/Pages/Account/` - страницы для регистрации и авторизации
- `Data/` - контекст базы данных и миграции
- `Pages/` - основные страницы приложения
- `wwwroot/` - статические файлы (стили, скрипты) 
