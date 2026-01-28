<!--

@license Apache-2.0

Copyright (c) 2026 The Stdlib Authors.

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


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# Kurtosis

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Half-normal][half-normal-distribution] distribution [excess kurtosis][kurtosis].

<section class="intro">

The [excess kurtosis][kurtosis] of a [half-normal][half-normal-distribution] distribution with scale `sigma > 0` is

<!-- <equation class="equation" label="eq:halfnormal_kurtosis" align="center" raw="\gamma_2 = \frac{8(\pi-3)}{(\pi-2)^2}" alt="Excess kurtosis for a half-normal distribution."> -->

```math
\gamma_2 = \frac{8(\pi-3)}{(\pi-2)^2}
```

<!-- <div class="equation" align="center" data-raw-text="\gamma_2 = \frac{8(\pi-3)}{(\pi-2)^2}" data-equation="eq:halfnormal_kurtosis">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@2d398018e6a1275033c4ad59453a233302c3409d/lib/node_modules/@stdlib/stats/base/dists/halfnormal/kurtosis/docs/img/equation_halfnormal_kurtosis.svg" alt="Excess kurtosis for a half-normal distribution.">
    <br>
</div> -->

<!-- </equation> -->

</section>

<!-- /.intro -->



<section class="usage">

## Usage

```javascript
import kurtosis from 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-halfnormal-kurtosis@v0.1.0-esm/index.mjs';
```

#### kurtosis( sigma )

Returns the [excess kurtosis][kurtosis] of a [half-normal][half-normal-distribution] distribution with scale parameter `sigma`.

```javascript
var x = kurtosis( 1.0 );
// returns ~0.869

var y = kurtosis( 4.0 );
// returns ~0.869
```

If provided `sigma <= 0`, the function returns `NaN`.

```javascript
var x = kurtosis( 0.0 );
// returns NaN

var y = kurtosis( -1.0 );
// returns NaN
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="module">

import uniform from 'https://cdn.jsdelivr.net/gh/stdlib-js/random-array-uniform@esm/index.mjs';
import logEachMap from 'https://cdn.jsdelivr.net/gh/stdlib-js/console-log-each-map@esm/index.mjs';
import kurtosis from 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-halfnormal-kurtosis@v0.1.0-esm/index.mjs';

var opts = {
    'dtype': 'float64'
};
var sigma = uniform( 10, 0.0, 20.0, opts );

logEachMap( 'σ: %0.4f, Kurt(X;σ): %0.4f', sigma, kurtosis );

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

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2026. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/stats-base-dists-halfnormal-kurtosis.svg
[npm-url]: https://npmjs.org/package/@stdlib/stats-base-dists-halfnormal-kurtosis

[test-image]: https://github.com/stdlib-js/stats-base-dists-halfnormal-kurtosis/actions/workflows/test.yml/badge.svg?branch=v0.1.0
[test-url]: https://github.com/stdlib-js/stats-base-dists-halfnormal-kurtosis/actions/workflows/test.yml?query=branch:v0.1.0

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/stats-base-dists-halfnormal-kurtosis/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/stats-base-dists-halfnormal-kurtosis?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/stats-base-dists-halfnormal-kurtosis.svg
[dependencies-url]: https://david-dm.org/stdlib-js/stats-base-dists-halfnormal-kurtosis/main

-->

[chat-image]: https://img.shields.io/badge/zulip-join_chat-brightgreen.svg
[chat-url]: https://stdlib.zulipchat.com

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/stats-base-dists-halfnormal-kurtosis/tree/deno
[deno-readme]: https://github.com/stdlib-js/stats-base-dists-halfnormal-kurtosis/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/stats-base-dists-halfnormal-kurtosis/tree/umd
[umd-readme]: https://github.com/stdlib-js/stats-base-dists-halfnormal-kurtosis/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/stats-base-dists-halfnormal-kurtosis/tree/esm
[esm-readme]: https://github.com/stdlib-js/stats-base-dists-halfnormal-kurtosis/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/stats-base-dists-halfnormal-kurtosis/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/stats-base-dists-halfnormal-kurtosis/main/LICENSE

[half-normal-distribution]: https://en.wikipedia.org/wiki/Half-normal_distribution

[kurtosis]: https://en.wikipedia.org/wiki/Kurtosis

</section>

<!-- /.links -->
