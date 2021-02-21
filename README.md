# fetch-opengraph

[![npm version](https://badgen.net/npm/v/fetch-opengraph)](https://npm.im/fetch-opengraph) [![CI-CD](https://github.com/purphoros/fetch-opengraph/workflows/CI%20CD/badge.svg)](https://github.com/purphoros/fetch-opengraph/actions) [![Build Status](https://travis-ci.com/purphoros/fetch-opengraph.svg?branch=master)](https://travis-ci.com/purphoros/fetch-opengraph) [![Coverage Status](https://coveralls.io/repos/github/purphoros/fetch-opengraph/badge.svg?branch=master)](https://coveralls.io/github/purphoros/fetch-opengraph?branch=master) [![License](https://img.shields.io/npm/l/@jsdevtools/npm-publish.svg)](LICENSE)


Fetch opengraph information from an url.

## Install

```
npm install fetch-opengraph --save
```

or

```
yarn add fetch-opengraph
```

## Usage

### Node example

Just a basic index.js running `node .`
```javascript
const fetchOpengraph = require('fetch-opengraph');

(async () => {
  const data = await fetchOpengraph.fetch('https://github.com/purphoros/fetch-opengraph');
  console.log(data)
})()

```

Running in a web environment

```javascript
import fetchOpengraph from 'fetch-opengraph';

(async () => {
  const data = await fetchOpengraph.fetch('https://github.com/purphoros/fetch-opengraph');
  console.log(data)
})()
```

### Expected result

```javascript
{
  description: 'Fetch opengraph information from an url.',
  'twitter:image:src': 'https://avatars.githubusercontent.com/u/4297636?s=400&amp;v=4',
  'twitter:card': 'summary',
  'twitter:title': 'purphoros/fetch-opengraph',
  'twitter:description': 'Fetch opengraph information from an url.',
  'og:image': 'https://avatars.githubusercontent.com/u/4297636?s=400&amp;v=4',
  'og:type': 'object',
  'og:title': 'purphoros/fetch-opengraph',
  'og:url': 'https://github.com/purphoros/fetch-opengraph',
  'og:description': 'Fetch opengraph information from an url.',
  image: 'https://avatars.githubusercontent.com/u/4297636?s=400&amp;v=4',
  url: 'https://github.com/purphoros/fetch-opengraph'
}