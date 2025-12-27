# tauri-action

[![version](https://badgen.net/github/release/remarkablemark/tauri-action)](https://github.com/remarkablemark/tauri-action/releases)
[![test](https://github.com/remarkablemark/tauri-action/actions/workflows/test.yml/badge.svg)](https://github.com/remarkablemark/tauri-action/actions/workflows/test.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

🔗 Build Tauri apps with GitHub Actions.

## Quick Start

```yaml
# .github/workflows/build.yml
on: push
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Build Tauri app
        uses: remarkablemark/tauri-action@v1
```

## Usage

**Basic:**

```yaml
- uses: remarkablemark/tauri-action@v1
```

See [action.yml](action.yml)

## Inputs

### `version`

**Optional**: The version. Defaults to `1.2.3`:

```yaml
- uses: remarkablemark/tauri-action@v1
  with:
    version: 1.2.3
```

## License

[MIT](LICENSE)
