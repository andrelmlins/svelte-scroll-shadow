# Svelte Scroll Shadow

[![npm version](https://badge.fury.io/js/svelte-scroll-shadow.svg)](https://www.npmjs.com/package/svelte-scroll-shadow) &bull; [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/andrelmlins/svelte-scroll-shadow/blob/master/LICENSE) &bull; [![Build Status](https://travis-ci.com/andrelmlins/svelte-scroll-shadow.svg?branch=master)](https://travis-ci.com/andrelmlins/svelte-scroll-shadow) &bull; [![Dependencies](https://david-dm.org/andrelmlins/svelte-scroll-shadow.svg)](https://david-dm.org/andrelmlins/svelte-scroll-shadow) &bull; [![Netlify Status](https://api.netlify.com/api/v1/badges/53827e2d-1e33-4e5b-a563-b05436626172/deploy-status)](https://app.netlify.com/sites/svelte-scroll-shadow/deploys) &bull; [![Language grade: JavaScript](https://img.shields.io/lgtm/grade/javascript/g/andrelmlins/svelte-scroll-shadow.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/andrelmlins/svelte-scroll-shadow/context:javascript)

Component that customizes the scroll and inserts shadow when scrolling exists

## Installation

```
npm i svelte-scroll-shadow
// OR
yarn add svelte-scroll-shadow
```

<em>Note: to use this library in sapper, install as devDependency. See the [link](https://github.com/sveltejs/sapper-template#using-external-components).</em>

## Demo [Link](https://svelte-scroll-shadow.netlify.com/)

Local demo:

```
git clone https://github.com/andrelmlins/svelte-scroll-shadow.git
cd svelte-scroll-shadow
yarn && yarn start
```

## Examples

An example of how to use the library:

```js
<script>
  import ScrollShadow from "svelte-scroll-shadow";
</script>

<ScrollShadow>
  <ul>
    <li>Teste</li>
    <li>Teste</li>
    <li>Teste</li>
    <li>Teste</li>
  </ul>
</ScrollShadow>
```

## Properties

Component props:

| Prop             | Default                                                                   | Type    | Description             |
| ---------------- | ------------------------------------------------------------------------- | ------- | ----------------------- |
| scrollColor      | #c5c5c5                                                                   | string  | Scroll color            |
| scrollColorHover | #a6a6a6                                                                   | string  | Scroll color when hover |
| scrollWidth      | 5                                                                         | number  | Scroll Width            |
| scrollPadding    | 0                                                                         | number  | Left scroll padding     |
| isShadow         | true                                                                      | boolean | View shadow             |
| shadow           | '0 2px 4px rgba(0, 0, 0, 0.2) inset, 0 -2px 4px rgba(0, 0, 0, 0.2) inset' | string  | Shadow                  |

## NPM Statistics

Download stats for this NPM package

[![NPM](https://nodei.co/npm/svelte-scroll-shadow.png)](https://nodei.co/npm/svelte-scroll-shadow/)

## License

Svelte Scroll Shadow is open source software [licensed as MIT](https://github.com/andrelmlins/svelte-scroll-shadow/blob/master/LICENSE).
