---
title: Get Started
description: Get started with ArcGIS REST JS.
---

# Get Started

ArcGIS REST JS takes advantage of web standards that are supported in all modern desktop browsers and most mobile browsers.

* [`Fetch` Support](https://caniuse.com/#feat=fetch)
* [`Promises` Support](https://caniuse.com/#feat=promises)
* [`FormData` Support](https://caniuse.com/#feat=xhr2)
* [`ECMAScript 5` Support](https://caniuse.com/#feat=es5)


## Browser Support

ArcGIS REST JS is supported in the same browsers as the [ArcGIS API for JavaScript](https://developers.arcgis.com/javascript/latest/guide/system-requirements/index.html#supported-browsers).

* Chrome
* Edge
* Firefox
* Safari 9 and later
* iOS Safari
* IE11

IE11 and older mobile browsers require polyfills.

* [`Promise` polyfill](https://github.com/stefanpenner/es6-promise)
* [`Fetch` polyfill](https://github.com/matthew-andrews/isomorphic-fetch)

## Node.js Support

ArcGIS REST JS is supported in Node.js 6.x and 8.x. It requires additional packages to polyfill `Fetch` and `FormData`.

We recommend the ones below:

* [`isomorphic-fetch`](https://www.npmjs.com/package/isomorphic-fetch) - to polyfill `Fetch`
* [`isomorphic-form-data`](https://github.com/form-data/isomorphic-form-data) - to polyfill `FormData`

Other versions of Node.js may also work with appropriate polyfills but we cannot guarantee support.

## Get started from CDN

Coming soon&hellip;

## Get started with a bundler (webpack, rollup, ect&hellip;)

Coming soon&hellip;

## Get started with Node.js

Make sure you have polyfills for [`fetch`](https://github.com/matthew-andrews/isomorphic-fetch) and [`FormData`](https://github.com/form-data/isomorphic-form-data) installed before using any ArcGIS REST JS library,

```bash
npm install isomorphic-fetch isomorphic-form-data @esri/arcgis-rest-request
```

```js
require("isomorphic-fetch");
require("isomorphic-form-data");

const { request } = require("@esri/arcgis-rest-request");

request("https://www.arcgis.com/sharing/rest/info").then(response => {
  console.log(response);
});
```

[Demo express application](https://github.com/Esri/arcgis-rest-js/tree/master/demos/express)