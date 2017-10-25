# react-md-links
Render Markdown style links inside any component

## Installing

```
npm install --save react-md-links
```

## Basic usage

```js
var React = require('react');
var ReactDOM = require('react-dom');
var MarkdownLinks = require('react-md-links');

var input = 'Some text that contains a [markdown link](https://en.wikipedia.org/wiki/Markdown) link that will be rendered as an archor';

ReactDOM.render(
    <MarkdownLinks source={input} anchorClassName={'link-class'} />,
    document.getElementById('container')
);
```

## Notes

This module is purely for rendering links with markdown syntax.


## Options

* `source` - *string* The Markdown source to parse (**required**)
* `className` - *string* Class name of the container element (default: `''`).
* `containerTagName` - *string* Tag name for the container element, since Markdown can have many root-level elements, the component need to wrap them in something (default: `div`).
* `containerProps` - *object* An object containing custom element props to put on the container element such as `id` and `htmlFor`.
* `childBefore` - *object* A single child object that is rendered **before** the markdown source but within the container element
* `childAfter` - *object* A single child object that is rendered **after** the markdown source but within the container element

## Developing

```bash
git clone git@github.com:jolyonruss/react-md-links.git
cd react-md-links
npm install
npm test
```

## License

MIT-licensed. See LICENSE.

## Credit

Very much a derivative works of [react-markdown](https://github.com/rexxars/react-markdown)
