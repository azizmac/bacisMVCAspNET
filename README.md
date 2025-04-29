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
- PostgreSQL 14.0+
- Visual Studio 2022 или выше

## Настройка и запуск

### 1. Настройка базы данных PostgreSQL

1. Установите PostgreSQL, если он еще не установлен
2. Создайте базу данных с именем `authapp`:
   ```sql
   CREATE DATABASE authapp;
   ```
3. При необходимости, измените строку подключения в файле `appsettings.json`:
   ```json
   "ConnectionStrings": {
     "DefaultConnection": "Host=localhost;Port=5432;Database=authapp;Username=postgres;Password=postgres"
   }
   ```

### 2. Запуск приложения

#### Через Visual Studio:
1. Откройте проект в Visual Studio
2. Выполните команду в Package Manager Console для создания базы данных:
   ```
   Update-Database
   ```
3. Запустите приложение через IIS Express или ASP.NET Development Server

#### Через командную строку:
1. Примените миграции:
   ```
   dotnet ef database update
   ```
2. Запустите приложение:
   ```
   dotnet run
   ```

## Структура проекта

- `Areas/Identity/Pages/Account/` - страницы для регистрации и авторизации
- `Data/` - контекст базы данных и миграции
- `Pages/` - основные страницы приложения
- `wwwroot/` - статические файлы (стили, скрипты) 