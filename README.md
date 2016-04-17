# Deprecation Notice

:warning: This project is now *deprecated*; use [postcss-minify-font-values]
instead.

[postcss-minify-font-values]: https://github.com/TrySound/postcss-minify-font-values


# [postcss][postcss]-font-family

> Normalize font family declarations with PostCSS.

## Install

With [npm](https://npmjs.org/package/postcss-font-family) do:

```
npm install postcss-font-family --save
```

## Example

This module will try to minimise the `font-family` and `font` shorthand
properties; it can unquote font families where necessary, detect & remove
duplicates, and cut short a declaration after it finds a keyword. For more
examples, see the [tests](test.js).

### Input

```css
h1 {
    font-family: "Helvetica Neue", Arial, sans-serif, Helvetica;
}
```

### Output

```css
h1 {
    font-family: Helvetica Neue,Arial,sans-serif;
}
```

## API

### fontFamily([options])

#### options

##### removeAfterKeyword

Type: `boolean`
Default: `true`

Pass `false` to disable the module from removing font families after it
encounters a font keyword, for example `sans-serif`.

##### removeDuplicates

Type: `boolean`
Default: `true`

Pass `false` to disable the module from removing duplicated font families.

##### removeQuotes

Type: `boolean`
Default: `true`

Pass `false` to disable the module from removing quotes from font families.
Note that oftentimes, this is a *safe optimisation* & is done safely. For more
details, see [Mathias Bynens' article][mathias].

## Usage

See the [PostCSS documentation](https://github.com/postcss/postcss#usage) for
examples for your environment.

## Contributing

Pull requests are welcome. If you add functionality, then please add unit tests
to cover it.

## License

MIT © [Ben Briggs](http://beneb.info)

[postcss]: https://github.com/postcss/postcss

[mathias]: https://mathiasbynens.be/notes/unquoted-font-family
