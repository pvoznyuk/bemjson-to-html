# bemjson-to-html 
> BEMJSON to HTML serializer

This is optimized part of jsot-bh for generation HTML from constructed BEMJSON.

[DEMO](https://pvoznyuk.github.io/bemjson-to-html/)

## API

### Installing

`npm install bem-json-to-html --save`

### new BEMJSON([options])

Creates serializer object.

__Options__:

 * `jsAttrScheme` _String_ - If `js`, attribute with js params will be prefixed with `return ` (default: `js`).
 * `jsAttrName` _String_ - Specifies name of attribute, that will contain `jsParams` (default: `onclick`).
 * `defaultTag` _String_ - Default tag name for block without `tag` property (default: `div`).
 * `modificatorSeparator` _String_ - Suffix to use for mods instead of default `_` one. (E.g. `{modificatorSeparator: '--'}`).
 * `addDefautTagAttributes` _Boolean_ - Add default tags attributes like `src`, `href` (defaukt: `false`).

### BEMJSON.toHtml(bemjson)

Returns serialized HTML string.

## Benchmark

```
trivial
4,133,717 op/s » bemjson-to-html
2,371,357 op/s » bh

simple
109,658 op/s » bemjson-to-html
78,604 op/s » bh

full
27,264 op/s » bemjson-to-html
23,367 op/s » bh

stringify
1,508,587 op/s » stringify (no escaping)
843,899 op/s » stringify (escaped with replace)
388,025 op/s » stringify (escaped)
312,156 op/s » bemjson-to-html
220,219 op/s » bh
```

## License

MIT (c) [Vesvolod Strukchinsky](floatdrop@gmail.com), [Pavlo Vozniuk](pavlo.vozniuk@gmail.com)

[npm-url]: https://npmjs.org/package/bem-json-to-html
[npm-image]: http://img.shields.io/npm/v/bem-json-to-html.svg
