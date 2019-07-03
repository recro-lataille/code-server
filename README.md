## Build
- If you also plan on developing, set the `OUT` environment variable: `
  export OUT=/path/to/some/directory`. Otherwise it will build in this
  directory which will cause issues because then `yarn watch` will try to
  compile the build directory as well.
- Run `yarn build ${vscodeVersion} ${target} ${arch}`in this directory (for example:
  `yarn build 1.35.0 linux x64`).

## Development
- Clone VS Code.
- Run `yarn` in the VS Code root directory.
- Clone this repository to `src/vs/server` in the VS Code source.
- Run `yarn` in this directory.
- Run `yarn watch` in this directory.
- Wait for the initial compilation to complete.
- Run `yarn start` in this directory.
- Visit `http://localhost:8443`.
