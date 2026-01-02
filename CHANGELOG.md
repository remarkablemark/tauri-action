# Changelog

## [1.1.0](https://github.com/remarkablemark/tauri-action/compare/v1.0.6...v1.1.0) (2026-01-02)


### Features

* **action:** add input `fullscreen` ([f49274f](https://github.com/remarkablemark/tauri-action/commit/f49274f85ed2ad72275abc3b95e3fce0369565fc))
* **action:** add input `resizable` ([0d3abea](https://github.com/remarkablemark/tauri-action/commit/0d3abea3335f01e64cc9f7ee293343efc9e58ed6))

## [1.0.6](https://github.com/remarkablemark/tauri-action/compare/v1.0.5...v1.0.6) (2026-01-01)


### Bug Fixes

* **action:** set Windows `bundle-path` to `src-tauri\target\release\bundle` ([#18](https://github.com/remarkablemark/tauri-action/issues/18)) ([043d383](https://github.com/remarkablemark/tauri-action/commit/043d3837ec274d68acc0675c2e6cff2663f46b00))

## [1.0.5](https://github.com/remarkablemark/tauri-action/compare/v1.0.4...v1.0.5) (2025-12-31)


### Code Refactoring

* **action:** remove redundant inputs default and tidy steps ([#16](https://github.com/remarkablemark/tauri-action/issues/16)) ([6944b32](https://github.com/remarkablemark/tauri-action/commit/6944b328db7bfc2c2036486d439791d4e13eda36))

## [1.0.4](https://github.com/remarkablemark/tauri-action/compare/v1.0.3...v1.0.4) (2025-12-29)


### Bug Fixes

* **action:** don't use realpath of `bundle-path` ([#14](https://github.com/remarkablemark/tauri-action/issues/14)) ([3f4a4e8](https://github.com/remarkablemark/tauri-action/commit/3f4a4e8ac8eed777919712dd8bda023d6a0daecc))

## [1.0.3](https://github.com/remarkablemark/tauri-action/compare/v1.0.2...v1.0.3) (2025-12-28)


### Bug Fixes

* **action:** set default for input `identifier` and remove runner temp ([#12](https://github.com/remarkablemark/tauri-action/issues/12)) ([a2ed997](https://github.com/remarkablemark/tauri-action/commit/a2ed997841471bccca8d874c899b48b0e8745a24))

## [1.0.2](https://github.com/remarkablemark/tauri-action/compare/v1.0.1...v1.0.2) (2025-12-28)


### Bug Fixes

* **action:** replace TAURI_CONF with path ([#10](https://github.com/remarkablemark/tauri-action/issues/10)) ([40ec7f4](https://github.com/remarkablemark/tauri-action/commit/40ec7f4ee8d6c27790106c1680d446f0999438e4))

## [1.0.1](https://github.com/remarkablemark/tauri-action/compare/v1.0.0...v1.0.1) (2025-12-28)


### Bug Fixes

* **action:** override environment variable IDENTIFIER ([#8](https://github.com/remarkablemark/tauri-action/issues/8)) ([ff73435](https://github.com/remarkablemark/tauri-action/commit/ff7343518c8ed50944f8c85512fc83275dddcd0c))

## 1.0.0 (2025-12-28)


### Features

* **action:** add input `app-version` ([#5](https://github.com/remarkablemark/tauri-action/issues/5)) ([ad3b1f3](https://github.com/remarkablemark/tauri-action/commit/ad3b1f39c2814396eb102815350017e1d50d06d7))
* **action:** add inputs `window-width` and `window-height` ([#6](https://github.com/remarkablemark/tauri-action/issues/6)) ([a530aa3](https://github.com/remarkablemark/tauri-action/commit/a530aa351b74c4389c1dcc24d62fdf104adc460a))
* **action:** add output `bundle-path` ([#7](https://github.com/remarkablemark/tauri-action/issues/7)) ([a9120cd](https://github.com/remarkablemark/tauri-action/commit/a9120cda44ed0eab22e8b9663d203dc598561e39))
* **action:** build Tauri app and generate bundles ([#4](https://github.com/remarkablemark/tauri-action/issues/4)) ([8c6be68](https://github.com/remarkablemark/tauri-action/commit/8c6be68e57af1b6db40537250ced2c940abcadb9))
* **action:** init Tauri project with inputs passed as options ([96aaa38](https://github.com/remarkablemark/tauri-action/commit/96aaa38894919b26983e620b9f50d95640295235))
* **action:** install Tauri CLI and set default version to 2 ([#1](https://github.com/remarkablemark/tauri-action/issues/1)) ([e4e4300](https://github.com/remarkablemark/tauri-action/commit/e4e4300f3155f68a4c129bc6952f7a0840ed4a69))


### Bug Fixes

* **action:** wrap variables in double quotes ([b4e5d25](https://github.com/remarkablemark/tauri-action/commit/b4e5d25310a646fcc49d087b7a31b1416e2698bc))
