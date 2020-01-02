**XAMPP Версия 7.3.11**

    https://www.apachefriends.org/ru/download.html

**httpd-vhosts.conf**

    <VirtualHost *:80 >
        ServerAdmin webmaster@dummy-host2.example.com
        DocumentRoot "c:/xampp/htdocs/laravel/poligon.local/public"
        ServerName poligon.local
        ServerAlias www.poligon.local
        
        <Directory /xampp/htdocs/laravel/poligon.local/public>
            Options Indexes FollowSymLinks MultiViews
            AllowOverride All
            Order Allow,Deny
            Allow from all
        </Directory>
        
        ErrorLog "logs/poligon-error.log"
        CustomLog "logs/poligon-access.log" common
    </VirtualHost>
    
**C:/Windows/System32/drivers/etc/hosts**

    127.0.0.1   poligon.local

**Установка Composer**

    https://getcomposer.org/download/

    php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
    php -r "if (hash_file('sha384', 'composer-setup.php') === 'baf1608c33254d00611ac1705c1d9958c817a1a33bce370c0595974b342601bd80b92a3f46067da89e3b06bff421f182') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
    php composer-setup.php
    php -r "unlink('composer-setup.php');"
    
**Установка Laravel**

    Install last version
    php composer.phar create-project --prefer-dist laravel/laravel
    
    Install certain version 
    php composer.phar create-project --prefer-dist laravel/laravel laravel "5.7.0"

**Устанавливаем разрешения для папок фреймворка**

    sudo chmod 777 -R storage && sudo chmod 777 -R bootstrap/cache    

**Устанавливаем плагин Laravel для PhpStorm**

    File -> Settings -> Plugins

**Устанавливаем пакет Laravel IDE Helper Generator**
    
    https://github.com/barryvdh/laravel-ide-helper
    
    Установка пакета
    https://github.com/barryvdh/laravel-ide-helper
    
    Добавитьв composer.json в секцию scripts
    "post-update-cmd": [
        "Illuminate\\Foundation\\ComposerScripts::postUpdate",
        "@php artisan ide-helper:generate",
        "@php artisan ide-helper:meta"
    ]
    
**Обновление пакетов в composer.json**

    php composer.phar update

**Устанавливаем пакет Laravel Debugbar**

    https://github.com/barryvdh/laravel-debugbar
    
    Установка пакета
    composer require barryvdh/laravel-debugbar --dev
