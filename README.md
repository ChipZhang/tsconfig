# A TypeScript shareable config featuring separate configs of Node.js and React environment

## Overview

### For Node.js

If you extend the config for Node.js in your project, the config will set the target to `ES2019`, and it will produce
declaration files when compiling. This config is for Node.js projects with Node.js version 12+.

### For React

If you extend the config for React in your project, the config will set the target to `ES2020`, and it will preserve JSX
syntax, not produce declaration files when compiling. This config is for React projects, with Babel transpiling. The
compiled file should then be handled by Babel.

## Usage

- First, install this package as a development dependency. Note this package will not install `typescript`
  automatically.

```shell
npm i -D @chipzhang/tsconfig
```

- Then add a key `extends` to your `tsconfig.json` file

  - For Node.js project `{"extends": "@chipzhang/tsconfig/tsconfig.node.json"}`.

  - For React project `{"extends": "@chipzhang/tsconfig/tsconfig.react.json"}`.

- You can add custom settings in your `tsconfig.json` file.

## TypeScript Version

The configuration is tested for TypeScript version 4.2.4, and this package requires `peerDependencies`:

```json
{
  "typescript": "4.2.4"
}
```

## License

GNU AFFERO GENERAL PUBLIC LICENSE Version 3
