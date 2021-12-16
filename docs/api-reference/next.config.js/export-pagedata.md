---
description: Export stats about built pages.
---

# Generating page statistics on build

While building, Next.js can generate a `page-data.json` file containing metrics of your application.
This data can be used to monitor trends in bundle sizes or to page count.

`exportPageData` toggles the behaviour of this feature. By default, it is disabled. If enabled, the build step will create an additonal file called `page-data.json` in your output folder. See below for example data.

```js
module.export = {
  exportPageData: true,
}
```

<details>
  <summary><b>Example Data</b></summary>

```json
{
  "pages": [
    {
      "size": 40536,
      "totalSize": 113749,
      "static": true,
      "isSsg": false,
      "isWebSsr": false,
      "isHybridAmp": false,
      "ssgPageRoutes": null,
      "initialRevalidateSeconds": false,
      "pageDuration": 78,
      "name": "/"
    },
    {
      "size": 0,
      "totalSize": 73213,
      "static": false,
      "isSsg": false,
      "isWebSsr": false,
      "isHybridAmp": false,
      "ssgPageRoutes": null,
      "initialRevalidateSeconds": false,
      "name": "/_app"
    },
    {
      "size": 194,
      "totalSize": 73407,
      "static": true,
      "isSsg": false,
      "isWebSsr": false,
      "isHybridAmp": false,
      "ssgPageRoutes": null,
      "initialRevalidateSeconds": false,
      "name": "/404"
    },
    {
      "size": 0,
      "totalSize": 73213,
      "static": false,
      "isSsg": false,
      "isWebSsr": false,
      "isHybridAmp": false,
      "ssgPageRoutes": null,
      "initialRevalidateSeconds": false,
      "name": "/api/capture"
    }
  ],
  "sizeData": {
    "commonFiles": [
      "static/chunks/webpack-2b99834efceef160.js",
      "static/chunks/framework-91d7f78b5b4003c8.js",
      "static/chunks/main-50347007aa2c3e11.js",
      "static/css/dcd8253babfbb6e3.css",
      "static/chunks/pages/_app-73bb641067073568.js"
    ],
    "uniqueFiles": [
      "static/chunks/897-7ba0711baf91294e.js",
      "static/css/9eb0190d44a36315.css",
      "static/chunks/pages/index-90f84d886ae8d55d.js",
      "static/chunks/pages/_error-2280fa386d040b66.js"
    ],
    "sizeUniqueFiles": {
      "static/chunks/897-7ba0711baf91294e.js": 38044,
      "static/css/9eb0190d44a36315.css": 1738,
      "static/chunks/pages/index-90f84d886ae8d55d.js": 2492,
      "static/chunks/pages/_error-2280fa386d040b66.js": 194
    },
    "sizeCommonFile": {
      "static/chunks/webpack-2b99834efceef160.js": 773,
      "static/chunks/framework-91d7f78b5b4003c8.js": 42031,
      "static/chunks/main-50347007aa2c3e11.js": 29917,
      "static/css/dcd8253babfbb6e3.css": 424,
      "static/chunks/pages/_app-73bb641067073568.js": 492
    },
    "sizeCommonFiles": 73213
  },
  "sharedCssFiles": ["static/css/dcd8253babfbb6e3.css"],
  "sharedFiles": {
    "static/chunks/webpack-2b99834efceef160.js": 773,
    "static/chunks/framework-91d7f78b5b4003c8.js": 42031,
    "static/chunks/main-50347007aa2c3e11.js": 29917,
    "static/css/dcd8253babfbb6e3.css": 424,
    "static/chunks/pages/_app-73bb641067073568.js": 492
  },
  "hasCustomApp": "/_app.tsx"
}
```

</details>
