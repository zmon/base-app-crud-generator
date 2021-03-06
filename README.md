# Modified version of https://github.com/kEpEx/laravel-crud-generator for Savage Soft projects.

# laravel-crud-generator

Updated for Laravel 7

php artisan command to generate fully working crud with grid paginated server side only by having database tables


### Installing

```
COMPOSER_MEMORY_LIMIT=-1 composer require zmon/base-app-crud-generator @dev
```

Add to config/app.php the following line to the 'providers' array:
```
CrudGenerator\CrudGeneratorServiceProvider::class,
```

### Upgrade

```
COMPOSER_MEMORY_LIMIT=-1 composer update zmon/base-app-crud-generator @dev
```


### Usage

Use the desired model name as the input 


CRUD for students table
```
php artisan make:crud student
```
or the whole database
```
php artisan make:crud all
```
whole database with custom layout
```
php artisan make:crud all --master-layout=layouts.master 
```
Because sometimes you need boilerplate code only for view and controller, you can use an existing model with custom controller name
```
php artisan make:crud student --master-layout=master --custom-controller=dashboard	
```
For more options 
```
php artisan help make:crud
```
### Custom Templates

The best power of this plugin relies on you making your own templates and generating the code the way you like

Run this command:
```
php artisan vendor:publish
```
and you will have now in resources/templates/ the files you need to modify

If you want to go back to the default, just delete them

Let me know if you have any questions or if you find this library useful at twitter @[kEpEx](https://twitter.com/kepex)
