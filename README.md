# Installing laravel and react

Download xampp apache server with php version 7.1.3 (or newer)
https://www.apachefriends.org/index.html
Download composer
https://getcomposer.org/download/

#### Next command dowloads the global installer:
```
composer global require "laravel/installer"
```
#### following command will create a fresh Laravel installation in the directory you specify.
```
laravel new blog
```
#### Install jquery and bootstrap
```
npm install jquery
npm install bootstrap
```
## Set up frontend preset
### you can delete Vue by:
```
php artisan preset none
```
### Install react
```
php artisan preset react
```
#### Now run:
```
npm install 
npm run dev
```

# Tools

## Start local development server
```
php artisan serve
```
## Compiling assets
```
npm run dev
```
Or use watch:
```
npm run watch
```




