**Контроллер категорий**

Создание маршрутов
    
    ...
    Route::resource(categories, 'CategoryController')
        ->only($methods)
        ->names('blog.admin.categories')
    ...    

Создание контроллера
    
    php artisan make:controller Blog/Admin/CategoryController --resource
