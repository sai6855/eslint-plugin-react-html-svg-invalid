# eslint-plugin-react-html-svg-invalid

## ESLint plugin to avoid invalid HTML and svg elements

## Installation

You'll first need to install [ESLint](http://eslint.org):

```
$ npm i eslint --save-dev
```

Next, install `npm i eslint-plugin-react-html-svg-invalid`:

```
$ npm install eslint-plugin-html-svg-invalid --save-dev
```

**Note:** If you installed ESLint globally (using the `-g` flag) then you must also install `npm i eslint-plugin-react-html-svg-invalid` globally.

## Usage

Add `react-html-svg-invalid` to the plugins section of your `.eslintrc` configuration file. You can omit the `eslint-plugin-` prefix:

```json
{
  "plugins": ["react-html-svg-invalid"]
}
```

Then configure the rules you want to use under the rules section.

```json
{
  "rules": {
    "react-html-svg-invalid/html-svg-invalid": 2
  }
}
```

You can change rule from 2 to 1 which is warning or you can disable with zero.

## Rule Details

This rule aims to dissallow invalid html and svg elements in react app.

Examples for **incorrect** code for this rule:

```jsx
class Component extends React.Component {
  render() {
    <spa>Hello world!!</spa>;
  }
}
class Component extends React.Component {
  render() {
    <h12>Hello world!!</h12>;
  }
}
class Component extends React.Component {
  render() {
    <circl>Hello world!!</circl>;
  }
}
```

Examples for **correct** code for this rule:

```jsx
class Component extends React.Component {
  render() {
    <span>Hello world!!</span>;
  }
}
class Component extends React.Component {
  render() {
    <h1>Hello world!!</h1>;
  }
}
class Component extends React.Component {
  render() {
    <circle>Hello world!!</circle>;
  }
}
```
