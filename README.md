
## FETCH
Note: Next.js polyfills fetch() on both the client and server. You don't need to import it.

## prerendering
 Next.js generates HTML for each page in advance, instead of having it all done by client-side JavaScript. Pre-rendering can result in better performance and SEO

##  Static Generation and Server-side Rendering.

Static Generation is the pre-rendering method that generates the HTML at build time. The pre-rendered HTML is then reused on each request.
Server-side Rendering is the pre-rendering method that generates the HTML on each request.

## how to statically generate pages with dynamic routes?
let say you want the following poath  /posts/<id>

1.0- create a page at /pages/posts/[id].js
1.1- create a react component that render the page.
2.0- getStaticPath wich returns an array of all possible values for id.
3.0- getStaticProps which fetches necessary data for the posts with id.


## API ROUTES
https://nextjs.org/docs/pages/building-your-application/routing/api-routes

## WRITING SERVER SIDE CODE.
https://nextjs.org/docs/pages/building-your-application/data-fetching/get-static-props#write-server-side-code-directly


## getStaticProps
getStaticProps is primarily used for data fetching during static site generation. (you can call an api or query a database)
In production, the data fetched with getStaticProps is pre-rendered and reused for all requests, making it efficient.

getStaticProps only runs on the server-side. It will never run on the client-side.


You should use getServerSideProps only if you need to pre-render a page whose data must be fetched at request time.


## getStaticPaths
can fetch data from any data source. API, FILE SYSTEM etc..

## getServerSideProps
is called at request time, and allows render at the server, for each request. It contains a context parameter.

## Client side rendering
when you don't need to pre-render your data, or when the content of your pages needs to update frequently.



## how to create a 404 page?
To create a custom 404 page, create pages/404.js

## Router
If you want to access the Next.js router, you can do so by importing the useRouter hook from next/router.

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


https://nextjs.org/docs/advanced-features/custom-error-page

## Why are CSS Modules useful?

They scope styles at the component level

https://github.com/vercel/next.js/tree/canary/examples/with-tailwindcss


## Catch-all Routes
pages/posts/[...id].js matches /posts/a, but also /posts/a/b, /posts/a/b/c and so on.

If you do this, in getStaticPaths, you must return an array as the value of the id key like so: