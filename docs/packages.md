# Package-related information

## NPM

### `package.json`

#### `devDependencies`
Any cli package invoked in `scripts` section of `package.json` and listed in `devDependencies` will automatically look up local installation and thus doesn't need to be prepended with `npx`. That's why `sass` and `pug-cli` scripts are entered as is.

### NPX
NPM has an [NPX package][1] (it comes pre-installed with `npm`) which allows to run various global packages locally. So any prevously global package can be invoked locally (provided it is listed in `devDependencies`) by appending `npx` to it, i.e. `npx sass --style=compressed --update css:build/styles` will run a version of SASS installed in `node_modules`. It does look up further if it doesn't find it, up to loading from npm registry and running it, but that's not relevant to the local installation.

### `pug-cli`
Pug has a [command-line interface tool][2], which is installed as development dependency, therefore can be invoked through `npx pug`.

[1]: https://github.com/npm/npx
[2]: https://github.com/pugjs/pug-cli