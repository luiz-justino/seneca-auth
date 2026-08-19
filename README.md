![Seneca](http://senecajs.org/files/assets/seneca-logo.png)
> A [Seneca.js](http://senecajs.org) plugin

# @seneca/auth

[![npm version](https://img.shields.io/npm/v/seneca-auth.svg)](https://npmjs.com/package/seneca-auth)
[![build](https://github.com/senecajs/seneca-auth/actions/workflows/build.yml/badge.svg)](https://github.com/senecajs/seneca-auth/actions/workflows/build.yml)
[![Coverage Status](https://coveralls.io/repos/senecajs/seneca-auth/badge.svg?branch=master&service=github)](https://coveralls.io/github/senecajs/seneca-auth?branch=master)
[![Known Vulnerabilities](https://snyk.io/test/github/senecajs/seneca-auth/badge.svg)](https://snyk.io/test/github/senecajs/seneca-auth)

| ![Voxgig](https://www.voxgig.com/res/img/vgt01r.png) | This open source module is sponsored and supported by [Voxgig](https://www.voxgig.com). |
|---|---|

A user authentication plugin for Seneca, using [PassportJS](http://passportjs.org) for Express and [Bell](https://github.com/hapijs/bell) for Hapi.

## Install

```sh
npm install seneca-auth
```

## Quick Example

```js
var seneca = require('seneca')()
seneca.use('user')
seneca.use('entity')
seneca.use('auth')
```

## More Examples

See [test/](test/) for more usage examples.

## Motivation

This plugin provides user authentication for Seneca-based applications, supporting PassportJS for Express and Bell for Hapi frameworks.

A large part of the internal functionality is implemented as external plugins:

| Functionality | Loaded by default | Plugin |
|---|---|---|
| Local strategy auth | Yes | [seneca-local-auth](https://github.com/senecajs/seneca-local-auth) |
| Facebook strategy auth | No | [seneca-facebook-auth](https://github.com/senecajs/seneca-facebook-auth) |
| Github strategy auth | No | [seneca-github-auth](https://github.com/senecajs/seneca-github-auth) |
| Google strategy auth | No | [seneca-google-auth](https://github.com/senecajs/seneca-google-auth) |
| LinkedIn strategy auth | No | [seneca-linkedin-auth](https://github.com/senecajs/seneca-linkedin-auth) |
| Twitter strategy auth | No | [seneca-twitter-auth](https://github.com/senecajs/seneca-twitter-auth) |
| Redirect | Yes | [auth-redirect](https://github.com/senecajs/auth-redirect) |
| Cookie token | Yes | [auth-token-cookie](https://github.com/senecajs/auth-token-cookie) |
| Header token | No | [auth-token-header](https://github.com/senecajs/auth-token-header) |
| Url matcher | Yes | [auth-urlmatcher](https://github.com/senecajs/auth-urlmatcher) |
| Restrict Login | No | [auth-restrict-login](https://github.com/senecajs/auth-restrict-login) |

## Support

If you're using this module and need help, you can:

- Post a [github issue](https://github.com/senecajs/seneca-auth/issues)
- Tweet to [@senecajs](http://twitter.com/senecajs)
- Ask on the [Gitter](https://gitter.im/senecajs/seneca)

## API

### login

Login an existing user and set a login token.

- default url path: `/auth/login`
- options property: `urlpath.login`

### logout

Logout an existing user with an active login.

- default url path: `/auth/logout`
- options property: `urlpath.logout`

### user

Get the details of an existing, logged in user.

- default url path: `/auth/user`
- options property: `urlpath.user`

### register

Register a user and login automatically.

- default url path: `/auth/register`
- options property: `urlpath.register`

### create reset

Create a reset token.

- default url path: `/auth/create_reset`
- options property: `urlpath.create_reset`

### load reset

Load a user entity using a reset token.

- default url path: `/auth/load_reset`
- options property: `urlpath.load_reset`

### execute reset

Execute a password reset action.

- default url path: `/auth/execute_reset`
- options property: `urlpath.execute_reset`

### update user

Update user data.

- default url path: `/auth/update_user`
- options property: `urlpath.update_user`

### change password

Change user password.

- default url path: `/auth/change_password`
- options property: `urlpath.change_password`

### JSON API and Redirects

The redirect functionality is implemented as a separate module. See [auth-redirect](https://github.com/senecajs/auth-redirect) for details.

### Restrict Login

Different conditions for login can be added by overriding the default behavior of seneca action with pattern `role: 'auth', restrict: 'login'`.

This function must return:
- `{ ok: true }` if login is allowed
- `{ ok: false, why: 'reason' }` if login is not allowed

See [auth-restrict-login](https://github.com/senecajs/auth-restrict-login) for an example.

## Contributing

The [Senecajs org](https://github.com/senecajs/) encourages open participation. If you feel you can help in any way, be it with documentation, examples, extra testing, or new features please get in touch.

## Background

This plugin was created to provide standardized authentication for the Seneca microservices framework. It is part of the [Voxgig](https://www.voxgig.com) open source initiative.
