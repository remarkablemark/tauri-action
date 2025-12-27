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
        with:
          app-name: My App Name
```

## Usage

**Basic:**

```yaml
- uses: remarkablemark/tauri-action@v1
  with:
    app-name: My App Name
```

See [action.yml](action.yml)

## Inputs

### `app-name`

**Required**: The name of your Tauri application:

```yaml
- uses: remarkablemark/tauri-action@v1
  with:
    app-name: My App Name
```

### `window-title`

**Optional**: The window title of your Tauri application. Defaults to app name:

```yaml
- uses: remarkablemark/tauri-action@v1
  with:
    window-title: My Window Title
```

### `tauri-path`

**Optional**: The path of the Tauri project to use (relative to the cwd). Defaults to `.`:

```yaml
- uses: remarkablemark/tauri-action@v1
  with:
    tauri-path: .
```

### `frontend-dist`

**Optional**: The web assets location, relative to `<project-dir>/src-tauri`. Defaults to `../dist`:

```yaml
- uses: remarkablemark/tauri-action@v1
  with:
    frontend-dist: ../dist
```

### `before-build-command`

**Optional**: A shell command to run before `tauri build` kicks in. Defaults to `exit 0`:

```yaml
- uses: remarkablemark/tauri-action@v1
  with:
    before-build-command: npm run build
```

### `force`

**Optional**: Force init to overwrite the src-tauri folder. Defaults to `false`:

```yaml
- uses: remarkablemark/tauri-action@v1
  with:
    force: true
```

### `cli-version`

**Optional**: The [CLI version](https://www.npmjs.com/package/@tauri-apps/cli?activeTab=versions). Defaults to `2`:

```yaml
- uses: remarkablemark/tauri-action@v1
  with:
    cli-version: 2
```

## License

[MIT](LICENSE)
