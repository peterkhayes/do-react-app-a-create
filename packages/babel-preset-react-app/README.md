# babel-preset-react-app

This package includes the Babel preset used by [Do React App A Create](https://github.com/peterkhayes/do-react-app-a-create).<br>
Please refer to its documentation:

- [Getting Started](https://github.com/peterkhayes/do-react-app-a-create/blob/master/README.md#getting-started) – How to create a new app.
- [User Guide](https://github.com/peterkhayes/do-react-app-a-create/blob/master/packages/react-scripts/template/README.md) – How to develop apps bootstrapped with Do React App A Create.

## Usage in Do React App A Create Projects

The easiest way to use this configuration is with [Do React App A Create](https://github.com/peterkhayes/do-react-app-a-create), which includes it by default. **You don’t need to install it separately in Do React App A Create projects.**

## Usage Outside of Do React App A Create

If you want to use this Babel preset in a project not built with Do React App A Create, you can install it with following steps.

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

## Usage with TypeScript

To use this package with [`@babel/preset-typescript`](https://www.npmjs.com/package/@babel/preset-typescript), you need to disable `@babel/preset-flow` first.

You can achieve this by doing:

```
{
  "presets": [
    ["react-app", {
        "flow": false
    }],
    "@babel/typescript"
  ]
}
```
