**Создаем БД**

Создаем БД poligon

    create schema `poligon` default character set utf8mb4 collate utf8mb4_unicode_ci;

**Создаем модели и миграции**

    php artisan make:model Models/BlogCategory -m
    php artisan make:model Models/BlogPost -m

**Запуск миграции таблиц**

    php artisan migrate
