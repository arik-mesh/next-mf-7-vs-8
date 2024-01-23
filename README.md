# host-app-no-source-maps
A minimal reproduction of source maps not generating when using NextFederationPlugin

1. cd host-app-next-mp-8
2. npm install
3. npm run build
4. npm run export
5. deploy 'out' to a static host with security headers that don't allow 'unsafe-eval' (see example https://d214kpu06u9q9h.cloudfront.net/)
6. console errors:

    share.esm.js:91 Uncaught EvalError: Refused to evaluate a string as JavaScript because 'unsafe-eval' is not an allowed source of script in the following Content Security Policy directive: "script-src 'self' 'unsafe-inline'
    at new Function (<anonymous>)
    at 1026 (share.esm.js:91:22)
    at __webpack_require__ (bootstrap:24:23)
    at 9083 (index.cjs.js:3:15)
    at __webpack_require__ (bootstrap:24:23)
    at 6093 (main-2296636e816d6003.js:1:111)
    at __webpack_require__ (bootstrap:24:23)
    at main-2296636e816d6003.js:1:193475
    at r (jsonp chunk loading:75:28)
    at main-2296636e816d6003.js:1:51
