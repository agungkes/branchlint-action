# Branchlint ![CI](https://github.com/lekterable/branchlint-action/workflows/CI/badge.svg) [![codecov](https://codecov.io/gh/lekterable/branchlint-action/branch/master/graph/badge.svg)](https://codecov.io/gh/lekterable/branchlint-action) [![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square)](https://github.com/prettier/prettier) [![management: perfekt👌](https://img.shields.io/badge/management-perfekt👌-red.svg?style=flat-square)](https://github.com/lekterable/perfekt)

Lint your git branch names using github action.

## Usage

```yaml
name: Branchlint
on: pull_request
jobs:
  lint:
    runs-on: ubuntu-latest
    steps:
      - name: Lint branch name
        uses: lekterable/branchlint-action@v1.0.0
        with:
          allowed: |
            development
            /(epic|feat|fix|chore)/DEV-\d{4}/i
```

**_allowed_** - _(required)_ a list of allowed branch names separated by a new line

**NOTE:** you can use both strings and valid regular expressions.

## License

[MIT](LICENSE)
