[![npm][npm]][npm-url]
[![deps][deps]][deps-url]

<div align="center">
  <img width="200" height="200"
    src="https://cdn3.iconfinder.com/data/icons/lexter-flat-colorfull-file-formats/56/png-256.png">
  <a href="https://github.com/webpack/webpack">
    <img width="200" height="200"
      src="https://webpack.js.org/assets/icon-square-big.svg">
  </a>
  <h1>PNG Mask Loader</h1>
  <p>A loader for webpack that exports the grayscale values of a PNG.</p>
</div>

## Install

```bash
npm install --save-dev png-mask-loader
```

## Options

**grayOnly**: Whether to return the image gray, width, and size or just an array of gray values.

## Usage

Use the loader either via your webpack config, CLI or inline.

### Via webpack config (recommended)

**webpack.config.js**
```javascript
module.exports = {
  module: {
    rules: [
      {
        test: /\.mask\.png$/,
        use: 'png-mask-loader',
        options: {
          grayOnly: false
        }
      }
    ]
  }
}
```

**In your application**
```js
var mask = require('./image.mask.png');
```

### CLI

```bash
webpack --module-bind 'mask.png=png-mask-loader'
```

**In your application**
```js
var mask = require('./image.mask.png');
```

### Inline

**In your application**
```js
var mask = require('raw-loader!./image.mask.png')
```

[npm]: https://img.shields.io/npm/v/png-mask-loader.svg
[npm-url]: https://npmjs.com/package/png-mask-loader

[deps]: https://david-dm.org/dantheman827/png-mask-loader.svg
[deps-url]: https://david-dm.org/dantheman827/png-mask-loader
