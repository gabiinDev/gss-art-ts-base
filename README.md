# gss-art-ts-base

## Features

- Hybrid support - CommonJS and ESM modules
- IIFE bundle for direct browser support without bundler
- Typings bundle
- ESLint - scripts linter
- Stylelint - styles linter
- Prettier - formatter
- Jest - test framework
- Husky + lint-staged - pre-commit git hook set up for formatting

## Install

```bash
git clone https://github.com/kbysiec/vite-vanilla-ts-lib-starter.git
cd vite-vanilla-ts-lib-starter
npm i
```

Enable Git hooks
```bash
npx husky install
```

add this line to package.json
```json
"prepare": "husky install && husky add .husky/pre-commit 'npx lint-staged' && git add .husky/pre-commit"
```



## Usage

The starter contains the following scripts:

- `dev` - starts dev server
- `build` - generates the following bundles: CommonJS (`.cjs`) ESM (`.mjs`) and IIFE (`.iife.js`). The name of bundle is automatically taked from `package.json` name property
- `test` - starts jest and runs all tests
- `test:coverage` - starts jest and run all tests with code coverage report
- `lint:scripts` - lint `.ts` files with eslint
- `lint:styles` - lint `.css` and `.scss` files with stylelint
- `format:scripts` - format `.ts`, `.html` and `.json` files with prettier
- `format:styles` - format `.cs` and `.scss` files with stylelint
- `format` - format all with prettier and stylelint
- `prepare` - script for setting up husky pre-commit hook
