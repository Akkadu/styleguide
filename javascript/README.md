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

### Examples

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

### Variable type declarations

We should strive to document types of our variables, this makes using the code easier, especially by
those who have not written it. Type declarations created inline will be picked up by intellisense.
When reading this, remember that
- 0 and empty string '' equal to falsy
- We don't store information with index 0 in the database, no data will be queried with zero

_do_

```js

// this will define the right types in intellisense, remember that 0 and empty string are falsy.
// In addition we don't have items with id=0 in the database because numbering starts at 1.

/** Does a thing **/
export const paramsWithDefaultVars = (paramEventId = 0, paramVideoId = 0) =>{
  // ...
}

// You can define default variables a destructure them in the call.
// This will lead to an error however if called without a object variable.
// Calling the empty default callback is always safe.

/** Does another thing **/
const objectConfigWithDefaults = ({ myBool = false, myString = '', myNum = 0, myCallback = ()=>{} })=>{
 console.log(myBool)
 console.log(myString)
 console.log(!!myString)
 console.log(myNum)
 console.log(!!myNum)
 myCallback()
}

// a way to prevent this would be to do 

/** Does another other thing **/
const myFuncNoObject = (config = {})=>{
 const { myBool = false, myString = '', myNum = 0, myCallback = ()=>{} } = config
 console.log(myBool)
 console.log(myString)
 console.log(!!myString)
 console.log(myNum)
 console.log(!!myNum)
 callback()
}
```

_don't_

```js
/**
 * Does a thingaling
 * @param {{ myBool:boolean, myString:string, myNum:number }} params
 * @returns {{ ... }}
 */
export const doAThing = ({ myBool, myString, myNum }) => {
  // ...
}
```