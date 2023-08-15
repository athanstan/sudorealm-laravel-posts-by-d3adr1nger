<p align="center"><a href="https://laravel.com" target="_blank"><img src="http://sudorealm2.0.test/postImages/G1OlNpmtuLFJQbbp54iw74iDtwfxxbBNblRPhI76.png" width="650" alt="Laravel Logo"></a></p>


## Dark Theme with Laravel Tailwind and Alpine.js

Welcome, brave Realmer, to the intriguing world of shadows and code! Are you ready to embark on a journey where dimmed hues reign supreme and aesthetics meet functionality? Prepare to take a nocturnal expedition into the heart of 'Dark Theme with Laravel Tailwind and Alpine.js.' In the realm of modern web design, dark themes are more than a trend; they are a revelation. Providing comfort to the eyes of the night-loving coder and adding a sleek touch to the user interface, the art of mastering a dark theme is akin to wielding a powerful spell.

## The "must install" Laravel project process

### ⼻ Step 1: Create the project 
```bash
composer create-project --prefer-dist laravel/laravel dark-theme

cd dark-theme
npm install 
php artisan -V # make sure that you are on the last laravel version
```
### ⼻ Step 2: Install Tailwind CSS

Install tailwindcss and its peer dependencies via npm, and then run the init command to generate both tailwind.config.js and postcss.config.js.

```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p # create the tailwind.config.js and postcss.config.js files
```
**Configure your template paths**
Add the paths to all of your template files in your tailwind.config.js file.
```bash
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    "./resources/**/*.blade.php",
    "./resources/**/*.js",
    "./resources/**/*.vue",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
**Add the Tailwind directives to your CSS**
Add the @tailwind directives for each of Tailwind’s layers to your ./resources/css/app.css file.
```bash
@tailwind base;
@tailwind components;
@tailwind utilities;
``` 

**Start your build process**
Run your build process with npm run dev.
```bash
npm run dev
```
**Start using Tailwind in your project**
```html
<!DOCTYPE html>
<html lang="{{ str_replace('_', '-', app()->getLocale()) }}">
    <head>
        ...
        <!-- Styles -->
        @vite(['resources/css/app.css'])
    </head>
```

### ⼻ Step 3: Install Alpine.js

```bash
npm install alpinejs
```

**import Alpine into your bundle**
```js
import Alpine from 'alpinejs'
 
window.Alpine = Alpine
 
Alpine.start()
```

**Add the Alpine directives to your HTML**
```html
<!DOCTYPE html>
<html lang="{{ str_replace('_', '-', app()->getLocale()) }}">
    <head>
        ...
        <!-- Styles -->
        @vite(['resources/css/app.css', 'resources/js/app.js'])
    </head>
    <body x-data x-init="alert('Alpine.js installed successfully!')" class="antialiased">
    ...
    </body>
</html>
```

Now we are ready to code! 


