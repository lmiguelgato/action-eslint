# action-eslint
> TypeScript/JavaScript ESLint with custom path [action](https://github.com/features/actions)

## Usage

`.github/workflows/lint.yml`
```yml
on:
  push:
  pull_request:

jobs:
  eslint:
    name: eslint
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v1
    - name: install node v12
      uses: actions/setup-node@v1
      with:
        node-version: 12
    - name: yarn install
      run: yarn install
    - name: eslint
      uses: lmiguelgato/action-eslint@v1
      with:
        custom-glob: apps # only if a different glob is needed, default: src
        custom-path: static # only if a different path is needed, default is the root directory
```

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## Author
Originally authored by:
**action-eslint** © [iCrawl](https://github.com/iCrawl)

This version is maintained by [lmiguelgato](https://github.com/lmiguelgato).
