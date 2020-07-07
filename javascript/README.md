# Akkadu Javascript Styleguide

<!-- Hall of Fame -->
[![0](https://sourcerer.io/fame/HoukasaurusRex/Akkadu/styleguide/images/0)](https://sourcerer.io/fame/HoukasaurusRex/Akkadu/styleguide/links/0)
[![1](https://sourcerer.io/fame/HoukasaurusRex/Akkadu/styleguide/images/1)](https://sourcerer.io/fame/HoukasaurusRex/Akkadu/styleguide/links/1)
[![2](https://sourcerer.io/fame/HoukasaurusRex/Akkadu/styleguide/images/2)](https://sourcerer.io/fame/HoukasaurusRex/Akkadu/styleguide/links/2)
[![3](https://sourcerer.io/fame/HoukasaurusRex/Akkadu/styleguide/images/3)](https://sourcerer.io/fame/HoukasaurusRex/Akkadu/styleguide/links/3)
[![4](https://sourcerer.io/fame/HoukasaurusRex/Akkadu/styleguide/images/4)](https://sourcerer.io/fame/HoukasaurusRex/Akkadu/styleguide/links/4)
[![5](https://sourcerer.io/fame/HoukasaurusRex/Akkadu/styleguide/images/5)](https://sourcerer.io/fame/HoukasaurusRex/Akkadu/styleguide/links/5)
[![6](https://sourcerer.io/fame/HoukasaurusRex/Akkadu/styleguide/images/6)](https://sourcerer.io/fame/HoukasaurusRex/Akkadu/styleguide/links/6)
[![7](https://sourcerer.io/fame/HoukasaurusRex/Akkadu/styleguide/images/7)](https://sourcerer.io/fame/HoukasaurusRex/Akkadu/styleguide/links/7)
<!-- Badges -->
[![Contributors][contributors-shield]][contributors-url]
[![Issues][issues-shield]][issues-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]
<!-- Links -->
[contributors-shield]: https://img.shields.io/github/contributors/Akkadu/styleguide.svg?style=flat-square
[contributors-url]: https://github.com/Akkadu/styleguide/graphs/contributors
[issues-shield]: https://img.shields.io/github/issues/Akkadu/styleguide.svg?style=flat-square
[issues-url]: https://github.com/Akkadu/styleguide/issues
[forks-shield]: https://img.shields.io/github/forks/Akkadu/styleguide.svg?style=flat-square
[forks-url]: https://github.com/Akkadu/styleguide/network/members
[stars-shield]: https://img.shields.io/github/stars/Akkadu/styleguide.svg?style=flat-square
[stars-url]: https://github.com/Akkadu/styleguide/stargazers
[license-shield]: https://img.shields.io/github/license/Akkadu/styleguide.svg?style=flat-square
[license-url]: https://github.com/Akkadu/styleguide/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/company/akkadu/

Best practices rules and guides for contributing to Akkadu repositories.

[Contribute to the Guide][issues-url]

## Table of Contents

* [JSDoc Exported Symbols](#jsdoc-exported-symbols)

## JSDoc Exported Symbols

> We strive for complete documentation. Every exported symbol ideally should have a documentation line.

[_deno styleguide_](https://deno.land/manual/contributing/style_guide#use-jsdoc-for-exported-symbols)

Documentation should be human readable and provide non-obvious descriptions to all function definitions, prioritizing intellisense understanding of each symbol.

### Oneline JSDoc Comments

We configure our editors to intellisense our function parameters and return values, so the description is the only consistently valuable information to add to each exported symbol.

### Example

_do_

```js
/** Searches an object and returns the key-val of result */
export const objectSearch = (params) => {
  // ...
}
```

_don't_

```js
/**
 * Searches an object and returns the key-val of result
 * @param {{ ... }} params
 * @returns {{ ... }}
 */
export const objectSearch = (params) => {
  // ...
}
```