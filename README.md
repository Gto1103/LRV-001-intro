### Ответьте на вопросы

1. Перечислите список composer-пакетов, которые использует фреймворк Laravel после установки.

Они храняться в файле composer.json.

{
"name": "laravel/laravel",
"type": "project",
"description": "The skeleton application for the Laravel framework.",
"keywords": ["laravel", "framework"],
"license": "MIT",
"require": {
"php": "^8.1",
"guzzlehttp/guzzle": "^7.2",
"laravel/framework": "^10.10",
"laravel/sanctum": "^3.2",
"laravel/tinker": "^2.8"
},
"require-dev": {
"fakerphp/faker": "^1.9.1",
"laravel/pint": "^1.0",
"laravel/sail": "^1.18",
"mockery/mockery": "^1.4.4",
"nunomaduro/collision": "^7.0",
"phpunit/phpunit": "^10.1",
"spatie/laravel-ignition": "^2.0"
},
"autoload": {
"psr-4": {
"App\\": "app/",
"Database\\Factories\\": "database/factories/",
"Database\\Seeders\\": "database/seeders/"
}
},
"autoload-dev": {
"psr-4": {
"Tests\\": "tests/"
}
},
"scripts": {
"post-autoload-dump": [
"Illuminate\\Foundation\\ComposerScripts::postAutoloadDump",
"@php artisan package:discover --ansi"
],
"post-update-cmd": [
"@php artisan vendor:publish --tag=laravel-assets --ansi --force"
],
"post-root-package-install": [
"@php -r \"file_exists('.env') || copy('.env.example', '.env');\""
],
"post-create-project-cmd": [
"@php artisan key:generate --ansi"
]
},
"extra": {
"laravel": {
"dont-discover": []
}
},
"config": {
"optimize-autoloader": true,
"preferred-install": "dist",
"sort-packages": true,
"allow-plugins": {
"pestphp/pest-plugin": true,
"php-http/discovery": true
}
},
"minimum-stability": "stable",
"prefer-stable": true
}

2. Изучите директорию `config` и опишите какие файлы хранятся в этой директории.

В этой директории хранятся файлы настроек приложения.

<img src="config.png">

3. В какой директории хранятся основные файлы (классы) с бизнес-логикой приложения?

Они хранятся в директории "арр". В основном в папке "Models".
