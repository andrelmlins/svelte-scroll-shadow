# Svelte Scroll Shadow

[![npm version](https://badge.fury.io/js/svelte-scroll-shadow.svg)](https://www.npmjs.com/package/svelte-scroll-shadow) &bull; [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/andrelmlins/svelte-scroll-shadow/blob/master/LICENSE) &bull; [![Build Status](https://travis-ci.com/andrelmlins/svelte-scroll-shadow.svg?branch=master)](https://travis-ci.com/andrelmlins/svelte-scroll-shadow) &bull; [![Dependencies](https://david-dm.org/andrelmlins/svelte-scroll-shadow.svg)](https://david-dm.org/andrelmlins/svelte-scroll-shadow) &bull; [![Netlify Status](https://api.netlify.com/api/v1/badges/a16b6807-8f05-4e03-8ed4-33e5162155bb/deploy-status)](https://app.netlify.com/sites/svelte-scroll-shadow/deploys) &bull; [![Language grade: JavaScript](https://img.shields.io/lgtm/grade/javascript/g/andrelmlins/svelte-scroll-shadow.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/andrelmlins/svelte-scroll-shadow/context:javascript)

Component that customizes the image and inserts shadow when scrolling exists

## Installation

```
npm i svelte-scroll-shadow
// OR
yarn add svelte-scroll-shadow
```

## Demo [Link](https://svelte-scroll-shadow.netlify.com/)

Local demo:

```
git clone https://github.com/andrelmlins/svelte-scroll-shadow.git
cd svelte-scroll-shadow
yarn && yarn start
```

## Examples

```js
<script>
  import SvelteScrollShadow from "svelte-scroll-shadow";
</script>

<SvelteScrollShadow>
  <ul>
    <li>Teste</li>
    <li>Teste</li>
    <li>Teste</li>
    <li>Teste</li>
  </ul>
</SvelteScrollShadow>
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