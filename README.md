# rollup-plugin-strip-banner

[![Greenkeeper badge](https://badges.greenkeeper.io/mjeanroy/rollup-plugin-strip-banner.svg)](https://greenkeeper.io/)
[![Build Status](https://travis-ci.org/mjeanroy/rollup-plugin-strip-banner.svg?branch=master)](https://travis-ci.org/mjeanroy/rollup-plugin-strip-banner)
[![Get it on npm](https://nodei.co/npm/rollup-plugin-strip-banner.png?compact=true)](https://www.npmjs.org/package/rollup-plugin-strip-banner)

A plugin for [rollup](http://rollupjs.org) that can be used to remove banners (such as license
headers) from modules files before generating the final bundle.

## Installation

```npm install --save-dev rollup-plugin-strip-banner```

## Configuration and usage

Add the plugin in your rollup configuration file:

```js
const stripBanner = require('rollup-plugin-strip-banner');

module.exports = {
  entry: 'src/index.js',
  dest: 'dist/index.js',
  plugins: [
    stripBanner()
  ]
}
```

As other rollup plugins, `include` and `exclude` can be configured:

```js
const stripBanner = require('rollup-plugin-strip-banner');

module.exports = {
  entry: 'src/index.js',
  dest: 'dist/index.js',
  plugins: [
    stripBanner({
      include: '**/*.js',
      exclude: 'node_modules/**/*'
    })
  ]
}
```

## License

MIT License (MIT)

## Contributing

If you find a bug or think about enhancement, feel free to contribute and submit an issue or a pull request.
