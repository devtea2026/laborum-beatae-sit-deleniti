# @devtea2026/laborum-beatae-sit-deleniti <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

ES Object-related atoms: Object, ToObject, RequireObjectCoercible.

## Example

```js
const assert = require('assert');

const $Object = require('@devtea2026/laborum-beatae-sit-deleniti');
const ToObject = require('@devtea2026/laborum-beatae-sit-deleniti/ToObject');
const RequireObjectCoercible = require('@devtea2026/laborum-beatae-sit-deleniti/RequireObjectCoercible');

assert.equal($Object, Object);
assert.throws(() => ToObject(null), TypeError);
assert.throws(() => ToObject(undefined), TypeError);
assert.throws(() => RequireObjectCoercible(null), TypeError);
assert.throws(() => RequireObjectCoercible(undefined), TypeError);

assert.deepEqual(RequireObjectCoercible(true), true);
assert.deepEqual(ToObject(true), Object(true));

const obj = {};
assert.equal(RequireObjectCoercible(obj), obj);
assert.equal(ToObject(obj), obj);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

## Security

Please email [@ljharb](https://github.com/ljharb) or see https://tidelift.com/security if you have a potential security vulnerability to report.

[package-url]: https://npmjs.org/package/@devtea2026/laborum-beatae-sit-deleniti
[npm-version-svg]: https://versionbadg.es/ljharb/@devtea2026/laborum-beatae-sit-deleniti.svg
[deps-svg]: https://david-dm.org/ljharb/@devtea2026/laborum-beatae-sit-deleniti.svg
[deps-url]: https://david-dm.org/ljharb/@devtea2026/laborum-beatae-sit-deleniti
[dev-deps-svg]: https://david-dm.org/ljharb/@devtea2026/laborum-beatae-sit-deleniti/dev-status.svg
[dev-deps-url]: https://david-dm.org/ljharb/@devtea2026/laborum-beatae-sit-deleniti#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@devtea2026/laborum-beatae-sit-deleniti.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@devtea2026/laborum-beatae-sit-deleniti.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/es-object.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@devtea2026/laborum-beatae-sit-deleniti
[codecov-image]: https://codecov.io/gh/ljharb/@devtea2026/laborum-beatae-sit-deleniti/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/ljharb/@devtea2026/laborum-beatae-sit-deleniti/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/ljharb/@devtea2026/laborum-beatae-sit-deleniti
[actions-url]: https://github.com/devtea2026/laborum-beatae-sit-deleniti/actions
