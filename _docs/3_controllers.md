**Контроллеры**

 Создание REST-контроллера

    php artisan make:controller RestTestController --resource 

 Список контроллеров
    
    php artisan route:list
    php artisan route:list > routes.txt
 
 Контроллеры приложения
 
 Базовый контроллер блога
    
    php artisan make:controller Blog/BaseController
    
 Контроллер статей блога
    
    php artisan make:controller Blog/PostController --resource
