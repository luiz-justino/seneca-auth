![Seneca](http://senecajs.org/files/assets/seneca-logo.png)

> A [Seneca.js](http://senecajs.org) Auth Plugin

# seneca-auth

[![npm version][npm-badge]][npm-url]
[![Build Status][travis-badge]][travis-url]
[![Coverage Status][coveralls-badge]][coveralls-url]

| ![Voxgig](https://www.voxgig.com/res/img/vgt01r.png) | This open source module is sponsored and supported by [Voxgig](https://www.voxgig.com). |
|---|---|

## Install

```sh
npm install seneca-auth
```

## Quick Example

```js
var seneca = require('seneca')()
seneca.use('auth')
```

## More Examples

See the [test folder](test/) for detailed usage examples and scenarios.

## Motivation

This plugin provides user authentication for Seneca-based applications,
supporting PassportJS for Express and Bell for Hapi frameworks.

## Support

If you have any questions, [open an issue](https://github.com/senecajs/seneca-auth/issues)
or contact the [Senecajs team](https://senecajs.org/).

## API

### login

Login a user.

### logout

Logout a user.

### register

Register a new user.

## Contributing

The [Senecajs org](https://github.com/senecajs/) encourages open participation.
If you feel you can help in any way, be it with documentation, examples,
extra testing, or new features please get in touch.

## Background

This plugin was created to provide standardized authentication for the
Seneca microservices framework. It is part of the
[Voxgig](https://www.voxgig.com) open source initiative.

## License

Copyright (c) 2013-2024, Richard Rodger and other contributors.
Licensed under [MIT][].

[MIT]: ./LICENSE
[npm-badge]: https://img.shields.io/npm/v/seneca-auth.svg
[npm-url]: https://npmjs.com/package/seneca-auth
[travis-badge]: https://travis-ci.org/senecajs/seneca-auth.svg
[travis-url]: https://travis-ci.org/senecajs/seneca-auth
[coveralls-badge]: https://coveralls.io/repos/senecajs/seneca-auth/badge.svg?branch=master
[coveralls-url]: https://coveralls.io/github/senecajs/seneca-auth?branch=master
