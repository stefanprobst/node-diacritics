# node-diacritics

Remove diacritics from strings.

Useful when implementing some kind of search or filter functionality.

## Installation

```sh
yarn add @stefanprobst/diacritics
```

## API

```js
var removeDiacritics = require("diacritics").remove;
console.log(removeDiacritics("Iлｔèｒｎåｔïｏｎɑｌíƶａｔï߀ԉ"));
// prints "Internationalizati0n"
```

## Umlaut handling

This fork treats `Ä`, `ä`, `Ö`, `ö`, `Ü`, `ü` as German umlaut characters, which are transformed to `Ae`, `ae`, `Oe`, `oe`, `Ue`, `ue`. This differs from upstream behavior!
The motivation for this change was to adjust how `netlifycms` creates slugs using this package.
