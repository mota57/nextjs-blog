
## prerendering
 Next.js generates HTML for each page in advance, instead of having it all done by client-side JavaScript. Pre-rendering can result in better performance and SEO

##  Static Generation and Server-side Rendering.


## getStaticProps


## public directory static files.
Next.js can serve static assets, like images, under the top-level public directory.

## next/Image
 Next.js also has support for Image Optimization by default. This allows for resizing, optimizing, and serving images in modern formats like WebP.

 Images are lazy loaded by default.

## Pages
 a page is a React Component exported from a file in the pages directory.
 Simply create a JS file under the pages directory, and the path to the file becomes the URL path.

## Script
next/script is an extension of the HTML <script> element and optimizes when additional scripts are fetched and executed.

what does next/script simplify for you?
Loading third-party scripts


## Link
 The Link component enables client-side navigation between two pages in the same Next.js app.

## Client-side navigation:
 means that the page transition happens using JavaScript, which is faster.


## CSS modules
CSS modules allow you to locally scope CSS at the component-level by automatically creating unique class name, in order to avoid classes collission.

** Important: To use CSS Modules, the CSS file name must end with .module.css.

 Next.js allows you to import Sass using both the .scss and .sass extensions.

## _app.js
The default export of _app.js is a top-level React component that wraps all the pages in your applicatio

## how to add global css in next.js?
add it to _app.js



## Why are CSS Modules useful?

They scope styles at the component level

https://github.com/vercel/next.js/tree/canary/examples/with-tailwindcss