# Пошаговое руководство по созданию приложения

## Создаем каркс приложения
1. Необходимо установить (или проверить) что на компьютере установлена утилита Composer, 
сайт: https://getcomposer.org/.
Если её нет, то устанавливаем.
2. Будем использовать среду разработки PHPStorm, сайт: http://www.jetbrains.com/phpstorm/.
3. Создаём репозиторий на github в котором будет размещен проект.
4. Создаем проект в PHPStorm из репозитория размещенного в github.
5. В локальном каталоге запускаем команду "composer create-project laravel/laravel --prefer-dist projectname" для создания каркаса приложения, где "projectname" это название проекта.
Из каталога "projectname" переносим файлы в каталг проекта, т.к. новый проект нельзя создать в не пустом каталоге.
Ставим файлы проекта под версионный контроль из среды PHPStorm или из командной строки.
Не забываем, что папка "vendor" не ставитчя под версионный контроль!

## Настройки приложения
1. Название приложения указываем командой "php artisan app:name testLaravel".
2. Папки внутри "storage" должны быть доступны веб-серверу для записи, не забываем сделать "chmod -R 777 storage" на хостинге.

Настройки среды выполнения
1. Настройки хранятся в файле ".env", он под версионный контроль по уолчанию не ставится, см. исклбчения в файле ".gitignore".
2. Для каждого варианта среды выполнения создаем свой ".env" и на месте разворачивания приложения переименовываем его в ".env"
3. создаем файл ".env.local" для локальных настроек при разработке.
4. создаем файл ".env.testing" для тестовых настроек.
5. создаем файл ".env.production" для рабочих настроек.
6. см. [Получение и установка значений настроек](notes_env.md).

## Описываем подключение к БД
В файле ".env", следующие параметры отвечают за подключение к БД:
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=homestead
DB_USERNAME=homestead
DB_PASSWORD=secret
```

## [Официальная документация](https://laravel.com/docs/5.5/)
### Основы
1. Роутинг (Routing): https://laravel.com/docs/5.5/routing
2. Посредники Middleware: https://laravel.com/docs/5.5/middleware
3. Контроллеры (Controllers): https://laravel.com/docs/5.5/controllers
4. HTTP-запросы (HTTP Requests): https://laravel.com/docs/5.5/requests
5. HTTP-ОТКЛИКИ (HTTP Responses): https://laravel.com/docs/5.5/responses
6. Шаблоны (Views): https://laravel.com/docs/5.5/views
7. Ссылки (URL Generation): https://laravel.com/docs/5.5/urls
8. HTTP сессия (HTTP Session): https://laravel.com/docs/5.5/session
9. Валидация (Validation): https://laravel.com/docs/5.5/validation
10. Ошибки и логирование (Errors & Logging): https://laravel.com/docs/5.5/errors 
### Фронтенд
1. Шаблоны Blade (Blade Templates): https://laravel.com/docs/5.5/blade
2. Локализация (Localization): https://laravel.com/docs/5.5/localization
3. Фронтенд (Frontend Scaffolding): https://laravel.com/docs/5.5/frontend
4. Сборка фронтенда (Compiling Assets): https://laravel.com/docs/5.5/mix
### Безопасность
1. Аутентификация (Authentication): https://laravel.com/docs/5.5/authentication
2. Авторизация (Authorization): https://laravel.com/docs/5.5/authorization
