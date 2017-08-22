# Build a Task List with Laravel 5.4 and Vue 2

Results of the tutorial from [Connor Leech](https://medium.com/@connorleech/build-a-task-list-with-laravel-5-4-and-vue-2-9be0bba06801) extended by using [Laradock](http://laradock.io).

Follow the [Laradock installation guide](http://laradock.io/getting-started/#A1).

Then run the following steps to configure mysql:

```
cd laradock
docker-compose up -d ngnix mysql phpmyadmin
docker-compose exec mysql bash
mysql -u root -p
```

When prompted set the password to `root`.


Change the `DB_HOST` in Laravel's *.env* file to `mysql`:

```
DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=laravue
DB_USERNAME=root
DB_PASSWORD=root
```

Clear the Laravel config cache:

```
docker-compose exec workspace bash
php artisan config:cache
```

