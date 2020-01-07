**Контроллер категорий**

Создание маршрутов
    
    ...
    Route::resource(categories, 'CategoryController')
        ->only($methods)
        ->names('blog.admin.categories')
    ...    

Создание контроллера
    
    php artisan make:controller Blog/Admin/CategoryController --resource

Создание надстройки для Request
    
    php artisan make:request BlogCategoryUpdateRequest
