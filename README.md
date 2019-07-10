## Build
- If you also plan on developing, set the `OUT` environment variable: `
  export OUT=/path/to/some/directory`. Otherwise it will build in this
  directory which will cause issues because then `yarn watch` will try to
  compile the build directory as well.
- For now `@coder/nbin` is a global dependency.
- Run `yarn build ${codeServerVersion} ${vscodeVersion} ${target} ${arch}` in
  this directory (for example: `yarn build development 1.35.0 linux x64`).
- You can run the built code with `node path/to/build/out/vs/server/main.js` or run
  `yarn binary` with the same arguments in the previous step to package the
  code into a single binary.

## Development
```fish
git clone https://github.com/microsoft/vscode
cd vscode
git clone https://github.com/cdr/code-server src/vs/server
cd src/vs/server
yarn patch:apply
yarn
yarn watch
# Wait for the initial compilation to complete (it will say "Finished compilation").
yarn start
# Visit http://localhost:8443
```
