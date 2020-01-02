**Создаем БД**

Создаем БД poligon

    create schema `poligon` default character set utf8mb4 collate utf8mb4_unicode_ci;

**Создаем модели и миграции**

    php artisan make:model Models/BlogCategory -m
    php artisan make:model Models/BlogPost -m

###### **Запуск миграции таблиц**

    php artisan migrate

**Создаем сиды**

    php artisan make:seeder UsersTableSeeder
    php artisan make:seeder BlogCategoriesTableSeeder
    
###### **Запуск сидов**
    php artisan db:seed
    php artisan db:seed --class=UserTableSeeder
    php artisan migrate:refresh --seed
**Создаем фабрики**

    php artisan make:factory BlogPostFactory
    
###### **Запуск фабрик**    
