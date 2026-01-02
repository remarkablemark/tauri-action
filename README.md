<p align="center">
  <img src="tauri-logo.svg" width="150" alt="Tauri logo">
</p>

# tauri-action

[![GitHub Release](https://img.shields.io/github/v/release/remarkablemark/tauri-action)](https://github.com/remarkablemark/tauri-action/releases)
[![test](https://github.com/remarkablemark/tauri-action/actions/workflows/test.yml/badge.svg)](https://github.com/remarkablemark/tauri-action/actions/workflows/test.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

🔗 Build Tauri apps with GitHub Actions.

## Quick Start

```yaml
# .github/workflows/build.yml
on: push

jobs:
  build:
    runs-on: ${{ matrix.os }}
    strategy:
      matrix:
        os: [ubuntu-latest, macos-latest, windows-latest]

    steps:
      - name: Build Tauri app
        uses: remarkablemark/tauri-action@v1
        id: tauri
        with:
          app-name: My App Name

      - name: Upload Tauri bundle
        uses: actions/upload-artifact@v6
        with:
          name: ${{ runner.os }}
          path: ${{ steps.tauri.outputs.bundle-path }}
```

## Usage

Build a Tauri app given the frontend artifacts are at `dist`:

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

### `app-version`

**Optional**: Your application version. Defaults to `0.1.0`:

```yaml
- uses: remarkablemark/tauri-action@v1
  with:
    app-version: 0.1.0
```

### `window-title`

**Optional**: The window title of your Tauri application. Defaults to the app name:

```yaml
- uses: remarkablemark/tauri-action@v1
  with:
    window-title: My Window Title
```

### `window-width`

**Optional**: The window width in logical pixels. Defaults to `800`:

```yaml
- uses: remarkablemark/tauri-action@v1
  with:
    window-width: 800
```

### `window-height`

**Optional**: The window height in logical pixels. Defaults to `600`:

```yaml
- uses: remarkablemark/tauri-action@v1
  with:
    window-height: 600
```

### `window-fullscreen`

**Optional**: Whether the window starts as fullscreen or not. Defaults to `false`:

```yaml
- uses: remarkablemark/tauri-action@v1
  with:
    window-fullscreen: false
```

### `window-resizable`

**Optional**: Whether the window is resizable or not. Defaults to `true`:

```yaml
- uses: remarkablemark/tauri-action@v1
  with:
    window-resizable: true
```

> [!NOTE]
>
> When resizable is set to `false`, the native window's maximize button is automatically disabled.

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
    force: false
```

### `identifier`

**Optional**: The application [identifier](https://tauri.app/reference/config/#identifier) in reverse domain name notation (e.g. `com.tauri.example`). Defaults to `com.<owner>.<repo>`:

```yaml
- uses: remarkablemark/tauri-action@v1
  with:
    identifier: com.tauri.example
```

### `tauri-version`

**Optional**: The Tauri version (used by the [CLI](https://www.npmjs.com/package/@tauri-apps/cli)). Defaults to `2`:

```yaml
- uses: remarkablemark/tauri-action@v1
  with:
    tauri-version: 2
```

## Outputs

### `bundle-path`

The path to the Tauri bundle directory:

```yaml
- uses: remarkablemark/tauri-action@v1
  id: tauri
  with:
    app-name: My App

- uses: actions/upload-artifact@v6
  with:
    name: ${{ runner.os }}
    path: ${{ steps.tauri.outputs.bundle-path }}
```

> [!NOTE]
>
> On Linux and macOS, the bundle path is `src-tauri/target/release/bundle`.
>
> On Windows, the bundle path is `src-tauri\target\release\bundle`.

## FAQ

### macOS app is damaged

If you get the error when opening your macOS app:

> "Your App" is damaged and can't be opened. You should move it to the Trash.

Then configure [ad-hoc signing](https://tauri.app/distribute/sign/macos/#ad-hoc-signing):

```yml
- name: uses: remarkablemark/tauri-action@v1
  with:
    app-name: My App
  env:
    APPLE_SIGNING_IDENTITY: '-'
```

## License

[MIT](LICENSE)
