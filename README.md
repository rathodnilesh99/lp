# Install Composer
Composer is a dependency manager for PHP and is required for managing Laravel dependencies.

To install Composer globally:

**bash
curl -sS https://getcomposer.org/installer | php
sudo mv composer.phar /usr/local/bin/composer**

Verify the installation by running:
**composer --version**

Run Composer to create a new Laravel application:

**composer create-project --prefer-dist laravel/laravel my-laravel-app**

Set Directory Permissions
Laravel requires proper permissions to the storage and bootstrap/cache directories.

**cd /var/www/my-laravel-app
sudo chmod -R 775 storage bootstrap/cache**

Set Up Environment Configuration
Laravel uses .env file for environment configuration.

**cp .env.example .env**

Generate Application Key
Laravel requires an application key for encryption. Generate it with the following command:

**php artisan key:generat**

Run Database Migrations (Optional)
If your Laravel app uses a database and has migrations, run the migrations:

**php artisan migrate**

Configure Virtual Host (For Apache)
Create a new virtual host configuration file for your Laravel app. For Apache:

**sudo nano /etc/apache2/sites-available/my-laravel-app.conf**

Run Laravel's Development Server
Laravel includes a built-in development server to serve your application locally.
Run the built-in server: From the project directory, run the following Artisan command:

**php artisan serve**

You're all set up! Now you can start developing your Laravel application.

Create Routes: Open routes/web.php to add your app's routes.

Create Controllers: Use Artisan to generate controllers:
**php artisan make:controller MyController**


Run Migrations: If you're using a database, run migrations:
**php artisan migrate**

