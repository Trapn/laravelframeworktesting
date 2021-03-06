# Installing laravel and react

Download nodeJS
https://nodejs.org/en/

Download xampp apache server with php version 7.1.3 (or newer)
https://www.apachefriends.org/index.html

Download composer
https://getcomposer.org/download/

#### Next command downloads the global installer:
```
composer global require "laravel/installer"
```
#### Following command will create a fresh Laravel installation in the directory you specify.
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
# Using blade templating and basic routing
#### If you want you can install laravel blade snippets and syntax highlight support for Visual Studio Code.
![alt text](https://github.com/Trapn/laravelframeworktesting/blob/master/Screenshots/syntaxBladeVS.PNG)
### Make a new folder layouts in the directory views and copy/paste this code into a file layout.blade.php
```HTML
<!doctype html>
<html lang="{{ app()->getLocale() }}">
    <head>
        <meta charset="utf-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1">

        <title>Laravel</title>

        <!-- Fonts -->
        <link href="https://fonts.googleapis.com/css?family=Raleway:100,600" rel="stylesheet" type="text/css">

    </head>
    <body>

        @yield('content')

    </body>
</html>
```
### In the directory views you change the code of welcome.blade.php
```HTML
@extends('layouts.layout')

@section('content')
<h1>Index</h1>
<p>This is the first page</p>
@endsection
```
### Also in view you make a file called about.blade.php
```HTML
@extends('layouts.layout')

@section('content')
<h1>About</h1>
<p>About what?</p>
@endsection
```
### There is no route for the about.blade.php we can make this by opening the directory routes and open the file web.php two method can be used for creating a simple view route
#### Like this:
```
Route::view('/about', 'about');
```
#### Or like this:
```
Route::get('/about', function () {
    return view('about');
});
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
## Information commands
### Show the routes in the application:
```
php artisan route:list
```



