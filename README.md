safe-t.js
=========

Javascript API for Archos Safe-T.

This library is a mofified version of the [trezor.js](https://github.com/trezor/trezor.js) Javascript API, aiming at the support of Archos Safe-T mini.

See https://safe-t.io for more information

Install with npm
-----

`npm install --save safe-t.js`

We use some ES6 methods (Array.find etc), that aren't in all browsers as of now, so if you are targetting older browsers/mobile browsers, you have to add babel polyfill. See https://www.npmjs.com/package/babel-polyfill and https://babeljs.io/docs/usage/polyfill/

#### Examples

Example of usage is in `example/example.js`.

#### Flow
safe-t.js is annotated with [Flow](https://github.com/facebook/flow) types; if you want to use Flow and use the previous setup, it will use the right types. Note that you might have to set up `.flowconfig` to include all the modules and interface files in [our flowconfig](https://github.com/archos-safe-t/safe-t.js/blob/master/src/.flowconfig)

Using safe-t.js in a web app
----
If you are using safe-t.js in a web app, the *end user* has to install the transport layer [Safe-T bridge](https://github.com/archos-safe-t/safe-t-daemon-go). Also, the web app's URL has to be whitelisted specifically by Archos.

#### Whitelisting

You cannot connect to transport layers from anywhere on the internet. Your URL needs to be specifically whitelisted by Archos.

`localhost` is specifically whitelisted, so you can experiment on `http://localhost/*`. If you want to add your url in order to make a SAFE-T web application, [make a pull request to this file](https://github.com//archos-safe-t/safe-t-common/blob/master/signer/config.json).

safe-t.js API
-----

API is explained in [API.md](https://github.com/archos-safe-t/safe-t.js/blob/master/API.md)
