# fraktur.css

Fraktur font as a node packaged module.

[![latest version][npm-img]][npm-url] [![build status][travis-img]][travis-url] [![stability][stability-img]][stability-url] [![downloads][downloads-img]][npm-url]

[npm-img]: https://img.shields.io/npm/v/fraktur.css.svg?style=flat-square
[npm-url]: https://www.npmjs.com/package/fraktur.css
[travis-img]: https://img.shields.io/travis/bcomnes/fraktur.css.svg?style=flat-square
[travis-url]: https://travis-ci.org/bcomnes/fraktur.css
[stability-img]: https://img.shields.io/badge/stability-stable-brightgreen.svg?style=flat-square
[stability-url]: https://iojs.org/api/documentation.html#documentation_stability_index
[downloads-img]: https://img.shields.io/npm/dm/fraktur.css.svg?style=flat-square

## Install

```sh
# npm package
$ npm install fraktur.css
```

The css is exported from the package.json main field and can be imported using a css bundler or copied out of `node_modules` as part of a larger build process.

## Usage

```css
@import 'fraktur.css';

body { font-family: Fraktur BT, serif; }
```

### PostCSS

You can use PostCSS to inline and import this css module using the following `postcss.config.js`:

```js
module.exports = (ctx) => ({
  plugins: {
    'postcss-import': { root: ctx.file.dirname }, // Inline module css
    'postcss-url': { // Copy assets from node_modules
      url: 'copy',
      useHash: true,
      assetsPath: 'assets'
    }
  }
})
```

```
$ postcss styles.css -o dist/bundle.css
```
- [postcss/postcss](https://ghub.io/postcss)
- [jantimon/postcss-inline](https://github.com/jantimon/postcss-inline)
- [postcss/postcss-url](https://github.com/postcss/postcss-url)

## Credits

- 𝔘𝔫𝔦𝔠𝔬𝔡𝔢
- [substack/fraktur](https://github.com/substack/fraktur)

## See also

- [style.css](https://github.com/ungoldman/style.css)
- [top-bar.css](https://github.com/ungoldman/top-bar.css)
- [go-fonts.css](https://github.com/bcomnes/go-fonts.css)
- [chigaco.css](https://github.com/bcomnes/chicago.css)
- [big-cursors.css](https://github.com/bcomnes/big-cursors.css)
