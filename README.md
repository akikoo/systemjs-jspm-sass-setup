# jspm and SystemJS sample project 
 
Sample ES6 JavaScript project setup with jspm, SystemJS, Babel and React.

[![Build Status](https://travis-ci.org/akikoo/systemjs-jspm-setup.svg?branch=master)](https://travis-ci.org/akikoo/systemjs-jspm-setup)

## Environment setup 

```sh
  $ npm install
  $ jspm install
```

## Development

Start a mini-server (provided by Browsersync):

```sh
  $ npm start
```

## Run tests

```sh
  $ npm test
```

## Bundling 

WIP. Current options documented below.

### Using SystemJS Builder

Create minified `dist/main.js` and `dist/main.css` files.

```sh
  $ npm run bundle
```

### Bundle all the modules without using Builder script

Script is injected (no HTML script tag changes are needed).

```sh
  $ jspm bundle src/main dist/main.js --inject
```

### Create a self-executing, minified bundle 
 
HTML script tag changes are needed.
 
```sh
  $ jspm bundle-sfx --minify src/main dist/main.js
```

### Move back to separate file mode 

Clear out any injected bundle configuration. This runs the following script with node: `jspm unbundle`

```sh
  $ npm run dev 
```

To install packages, run `jspm install <package-name>`. For example, to install React, run this:

```sh
  $ jspm install npm:react
```