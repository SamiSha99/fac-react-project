# Deploying Your React Parcel App

This app is frontend only, so you can deploy on any static host (like [surge](https://surge.sh), Github Pages or [Netlify](https://netlify.com).

If you're making an SPA with client-side routing you need to set up your hosting correctly. This will ensure that all routes point to your `index.html`, allowing your JS to render the correct view. Without this your host may return a 404 when trying to directly access endpoint e.g. `www.mysite/endpoint` (since `endpoint.html` won't exist).

## Parcel Build Script
Add the following build script to your `package.json`:

`"build": parcel build index.html --public-url ./`

## Surge Instuctions
- [surge deploying](https://surge.sh/)
- [surge setup for client side routing](https://surge.sh/help/adding-a-200-page-for-client-side-routing)

## Netlify Instuctions
- [netlify steps for continuous deployment](https://www.netlify.com/docs/continuous-deployment/)
- [netlify setup for client side routing](https://www.netlify.com/docs/redirects/#history-pushstate-and-single-page-apps)
- If you get build errors using Parcel with Netlify it may be because they build using an older Node version by default (v6!). You can tell them to use whatever version you're using by setting an environment variable of `NODE_ENV` in the 'Deploy Settings' (scroll down to 'Build environment variables').
