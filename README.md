### Table of Contents

- [**Sass Boilerplate**](#sass-boilerplate)
- [What this boilerplate contains](#what-this-boilerplate-contains)
- [How to use this boilerplate](#how-to-use-this-boilerplate)
- [Explanation](#explanation)
  - [Font Awesome & Animate CSS](#font-awesome--animate-css)
  - [Folder Structure](#folder-structure)
  - [Node Packages](#node-packages)
  - [Media Query Manager](#media-query-manager)



# Sass Boilerplate

![Logo](./public/favicon.png)

> **This is a Sass boilerplate that can be used to initialize any basic Sass project**

---

## What this boilerplate contains

- **Font-Awesome** and **Animate CSS** is built in !
- **7-1 Folder** Architecture
- Global **Reset**
- **Gitignore** Included
- **Media Query** Manager
- JavaScript **Babel** Compilation 
- **Development scripts** : compile, serve and watch
- **Production scripts** : compile, prefix and compress.

---

## How to use this boilerplate

Simply clone this repo in your local system, and you will get all the files & folders setup.

-  Go to package.json and change any settings that you wish.
-  run **`npm install`** to install the dependencies
-  run **`npm start`** to start the development server
   -  will compile sass, concat vendors, compile js and run live server & watch
-  run **`npm run build`** to build all the files for production
   -  will compile, prefix and compress sass and vendors , and also compile js

---

## Explanation

-  You can simple remove anything that you don't wish to add in your project.

### Font Awesome & Animate CSS

-  They are already included in the HTML and you can use them out of the box

### Folder Structure

-  **./Public -** contains files for production
-  **./src -** contains files you will be working on (vendors, sass, js)
   -  Sass uses 7-1 folder architecture

### Node Packages

-  For Development

   -  **`babel:watch` -** watches `src/main.js` and compiles to `public/js/script.js`
   -  **`sass:watch` -** watches `src/main.scss` and compiles to `public/css/style.css`
   -  **`concat` -** concatenates all `src/vendor/*` into one `public/src/vendors.css`
   -  **`serve` -** serves the public folder
   -  **`start` -** runs all the above parallelly.

-  For Production
   -  **`babel` -** compiles `src/main.js` to `public/js/script.js`
   -  **`sass` -** compiles `src/main.scss` to `public/css/style.css`
   -  **`prefix` -** adds prefixes to `public/css/style.css` & `public/css/vendors.css`
   -  **`compress` -** compresses both `public/css/styles.css` & `public/css/vendors.css`
   -  **`build` -** runs all the above sequentially (also concatenates vendors)

### Media Query Manager

-  It is written in `src/scss/abstracts/mixins`, therefor is a mixin and can be included in any file where you want to add media query.

-  Sizes premade are

   -  **big-desktop :** 1800px
   -  **tab-land :** 1200px
   -  **tab-port :** 900px
   -  **phone :** 600px
   -  **phone-small :** 450px
   -  **phone-vsmall :** 390px

-  Code to use it is

```CSS
@include respond(device-name) {  //device name will be replaced with device you wish
   font-size: 8px;
}
```

---

Hope it helps, Keep Coding ! 😊
