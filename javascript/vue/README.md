# Akkadu VueJS Styleguide

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

* [Each Component Should Be Tested](#each-component-should-be-tested)

## Each Component Should Be Tested

If a component is a singleton (does not import any external components from within the project), then it should include a unit test file. If a component is complex, a task should be submitted in the roadmap to include an e2e integration test for it in CI.
