# babel-preset-react-app

This package includes the Babel preset used by [Create React App](https://github.com/facebook/create-react-app).<br>
Please refer to its documentation:

* [Getting Started](https://github.com/facebook/create-react-app/blob/master/README.md#getting-started) – How to create a new app.
* [User Guide](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md) – How to develop apps bootstrapped with Create React App.

## Usage in Create React App Projects

The easiest way to use this configuration is with [Create React App](https://github.com/facebook/create-react-app), which includes it by default. **You don’t need to install it separately in Create React App projects.**

## Usage Outside of Create React App

If you want to use this Babel preset in a project not built with Create React App, you can install it with following steps.

First, [install Babel](https://babeljs.io/docs/setup/).

Then install babel-preset-react-app.

```sh
npm install babel-preset-react-app --save-dev
```

Then create a file named `.babelrc` with following contents in the root folder of your project:

```js
{
  "presets": ["react-app"]
}
```

This preset uses the `useBuiltIns` option with [transform-object-rest-spread](http://babeljs.io/docs/plugins/transform-object-rest-spread/) and [transform-react-jsx](http://babeljs.io/docs/plugins/transform-react-jsx/), which assumes that `Object.assign` is available or polyfilled.

## Usage with Flow

To use this package with [`@babel/preset-flow`]https://www.npmjs.com/package/@babel/preset-flow), you only need to have a `.flowconfig` file at the root directory and it will be detected automatically. Alternatively, you can edit `.babelrc` with the following:

```
{
  "presets": [["react-app", { "flow": true }]]
}
```


## Usage with TypeScript

To use this package with [`@babel/preset-typescript`]https://www.npmjs.com/package/@babel/preset-typescript), you only need to have a `tsconfig.json` file at the root directory and it will be detected automatically. Alternatively, you can edit `.babelrc` with the following:

```
{
  "presets": [["react-app", { "typescript": true }]]
}
```

TSLint is also automatically supported, you only need to create a `tslint.json` (and optionally a `tslint.prod.json`) file at the root directory.