# 🚀 Sudorealm Laravel Posts by d3adr1nger 🚀
---

Welcome to the epicenter of creativity! This repository houses the live code for various intriguing projects showcased on Sudorealm.com. Dive deep into each post's magic - where every branch 🌳 is a unique story. From fundamentals to the most intricate Laravel nuances, journey with us as we unravel the fabric of web development, one post at a time. Star ⭐ to stay updated, and feel free to fork, contribute or just be inspired! Happy coding! 🔥🖥️🛠️

## 📜 List of Posts (Branches)
Here's a curated list of all the projects/posts available in this repository. Dive into each one by selecting the desired topic:

- [Dark Theme with Laravel Tailwind and Alpine.js](https://github.com/athanstan/sudorealm-laravel-posts-by-d3adr1nger/tree/dark-theme-with-laravel-tailwind-and-alpinejs)

****


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

Now we are ready to code and play with Laravel! 


