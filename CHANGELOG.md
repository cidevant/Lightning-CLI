# Changelog

## v2.12.0

*27 jul 2023*

- Fixed issue with rollup typescript project throwing error when accessing process env ([#235](https://github.com/rdkcentral/Lightning-CLI/issues/235))
- Added "include" config in tsconfig.json for lng create command
- Added support for getting "esEnv" from settings.json file for lng dist ([#224](https://github.com/rdkcentral/Lightning-CLI/issues/224))
- Added support for transpiling .mjs files to ES5 with rollup
- Fixed the issue related to Babel ignore is not possible to use in a babel.config.json ([#177](https://github.com/rdkcentral/Lightning-CLI/issues/177))

## v2.11.0

*28 apr 2023*

- Removed license texts from fixtures, so new Apps created with the CLI don't come with unnecessary licenses anymore ([#226](https://github.com/rdkcentral/Lightning-CLI/issues/226))
- Fixed build issue related to rollup path when using NPX. Solves issue for Metrological CLI. ([#222](https://github.com/rdkcentral/Lightning-CLI/issues/222))
- Fixed issue where sourcemap files were not generated when using esbuild ([#228](https://github.com/rdkcentral/Lightning-CLI/issues/228))
- Added support for CORS in `lng serve` via a new environment variable (`LNG_SERVE_CORS`)

## v2.10.0

*15 feb 2023*

- Fixed `.gitignore` is rewritten on each build. ([#209](https://github.com/rdkcentral/Lightning-CLI/issues/209))
- Removed `lng upload` command.
- Fixed `_states()` is broken for esbuild bundle when NODE_ENV=production. ([#213](https://github.com/rdkcentral/Lightning-CLI/issues/213))
- Replaced WebSockets with Socket.io for live reload.
- Added support for using environment variables set on the `process.env` in addition to variables defined in `.env` files ([#214](https://github.com/rdkcentral/Lightning-CLI/issues/214))


## v2.9.1

*24 oct 2022*

- Fixed typo

## v2.9.0

*20 oct 2022*

- Added support for `--es5` and `--es6` options to `build` command. (#200)
- Added support for Preserving Symbolic Links in the build process for rollup. (#201)
- Added support for environment variable `LNG_LIVE_RELOAD_HOST` and updated the documentation relevant to it. (#203)
- Added support for creating a project in typescript. (#195)
- Replaced 'metrological' with 'domain' in reverse DNS app identifier.

## v2.8.1

*22 aug 2022*

- Added browser build support
- Fixed issue related to ES5 polyfill path
- Fixed issue related to Dist with Monorepo setup
- Added Safari 12.0 as target for es6 configs in both rollup and esbuild bundlers

## v2.8.0

*21 jun 2022*

- Added mono repo support
- Added basic Typescript support (in app code)
- Added Source map support for rollup (es5 config) and esbuild (es5 and es6 configs)
- Fixed custom build folder issue in `.env` file
- Updated documentation related to `lng dist --watch` command
- Fixed the issue to have default value for app identifier matches the app name

## v2.7.2

*25 jan 2022*

- Updated http-server NPM dependency fixing the colors.js corruption issue

## v2.7.1

*29 nov 2021*

- Updated rollup commonjs plugin (issue #156)
- Fixed broken link in documentation

## v2.7.0

*22 nov 2021*

- Upgraded esbuild to version 0.12
- Added watcher support for `lng dist`
- Added `LNG_BUILD_FAIL_ON_WARNINGS` environment variable

## v2.6.0

*20 oct 2021*

- Added support for using `process.env.NODE_ENV` in Apps
- Added using the minified lightning library file in dist builds
- Added minification for esbuild bundler
- Improved error messages and handling
- Added babel-step to es6 config (for rollup and esbuild) to enable usage of class properties proposal syntax

## v2.5.1

*29 jun 2021*

- Fixes dynamic imports in rollup created bundle

## v2.5.0

*23 apr 2021*

- Updated CLI documentation
- Added es5 support for esbuild bundler
- Added support for different `settings.json`-files per environment
- Improved error messages
- Fixed missing `.gitignore`-file when creating new project with GIT options selected
- Fixed App specific environment variables not repopulating between builds in esbuild bundler
- Fixed version not showing in VersionLabel for dist version of App
- Added warning when upload package too large

## v2.2.0

*6 nov 2020*

- Added rollup image-plugin to bundle up image assets (as base64-images)

## v2.1.0

*30 oct 2020*

- Added `LNG_SERVE_PROXY` environment variable
- Added fix for polyfills not being copied over when using `lng dist --es5`-command
- Fixed auto-update functionality
- Added `lng update`-command

## v2.0.2

*19 oct 2020*

- Added fix for Lightning library not being copied over when using `lng dist`-command

## v2.0.1

*14 oct 2020*

- Changed package name from `wpe-lightning-cli` to `@lightningjs/cli` (and published on NPM)
- Updated minimum requirement to Node.js 10
- Support for building apps with new `@lightningjs/sdk` Loghtning-SDK (continued support for legacy `wpe-lightning-sdk`)
- Various smaller updates
