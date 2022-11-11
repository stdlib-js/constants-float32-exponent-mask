<!--

@license Apache-2.0

Copyright (c) 2022 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# FLOAT32_EXPONENT_MASK

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Mask for the exponent of a [single-precision floating-point number][ieee754].



<section class="usage">

## Usage

<!-- eslint-disable id-length -->

To use in Observable,

```javascript
FLOAT32_EXPONENT_MASK = require( 'https://cdn.jsdelivr.net/gh/stdlib-js/constants-float32-exponent-mask@umd/browser.js' )
```

To vendor stdlib functionality and avoid installing dependency trees for Node.js, you can use the UMD server build:

```javascript
var FLOAT32_EXPONENT_MASK = require( 'path/to/vendor/umd/constants-float32-exponent-mask/index.js' )
```

To include the bundle in a webpage,

```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/constants-float32-exponent-mask@umd/browser.js"></script>
```

If no recognized module system is present, access bundle contents via the global scope:

```html
<script type="text/javascript">
(function () {
    window.FLOAT32_EXPONENT_MASK;
})();
</script>
```

#### FLOAT32_EXPONENT_MASK

Mask for the exponent of a [single-precision floating-point number][ieee754].

<!-- eslint-disable id-length -->

```javascript
// 0x7f800000 = 2139095040 => 0 11111111 00000000000000000000000
var bool = ( FLOAT32_EXPONENT_MASK === 0x7f800000 );
// returns true
```

</section>

<!-- /.usage -->

<section class="notes">

</section>

<!-- /.notes -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/number-float32-base-to-word@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/constants-float32-exponent-mask@umd/browser.js"></script>
<script type="text/javascript">
(function () {

var x = 11.5;
var w = toWord( x ); // 0 10000010 01110000000000000000000
// returns 1094189056

// Mask off all bits except for the exponent bits:
var out = w & FLOAT32_EXPONENT_MASK; // 0 10000010 00000000000000000000000
// returns 1090519040

// Mask on the exponent bits and leave other bits unchanged:
out = w | FLOAT32_EXPONENT_MASK; // 0 11111111 01110000000000000000000
// returns 2142765056

})();
</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- C interface documentation. -->



<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2022. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/constants-float32-exponent-mask.svg
[npm-url]: https://npmjs.org/package/@stdlib/constants-float32-exponent-mask

[test-image]: https://github.com/stdlib-js/constants-float32-exponent-mask/actions/workflows/test.yml/badge.svg?branch=v0.0.1
[test-url]: https://github.com/stdlib-js/constants-float32-exponent-mask/actions/workflows/test.yml?query=branch:v0.0.1

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/constants-float32-exponent-mask/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/constants-float32-exponent-mask?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/constants-float32-exponent-mask.svg
[dependencies-url]: https://david-dm.org/stdlib-js/constants-float32-exponent-mask/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/constants-float32-exponent-mask/tree/deno
[umd-url]: https://github.com/stdlib-js/constants-float32-exponent-mask/tree/umd
[esm-url]: https://github.com/stdlib-js/constants-float32-exponent-mask/tree/esm
[branches-url]: https://github.com/stdlib-js/constants-float32-exponent-mask/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/constants-float32-exponent-mask/main/LICENSE

[ieee754]: https://en.wikipedia.org/wiki/IEEE_754-1985

</section>

<!-- /.links -->
