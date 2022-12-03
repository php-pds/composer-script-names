# pds/composer-script-names

This publication describes a standard suitable for all PHP packages regarding
Composer script names.

Please see <https://github.com/php-pds/composer-script-names_research> for
background information.

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD",
"SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this publication are to be
interpreted as described in [RFC 2119](http://tools.ietf.org/html/rfc2119).

## Summary

Script names in the `composer.json` file MUST be lower-case, and MUST use dashes
as word separators.

The `composer.json` file MUST use these script names for these purposes:

| If the `composer.json` file defines a script to ...                       | ... then it MUST be named: |
|-------------------------------------------------------------------------- | -------------------------- |
| Run tests using a default configuration                                   | `test`                     |
| Run tests using a default configuration, with coverage generation         | `test-coverage`            |
| Run tests using alternative configurations or approaches                  | `test-*` (see below)       |
| Run a coding style fixer and/or code linter using a default configuration | `cs-fix`                   |
| Run static analysis using a default configuration                         | `analyse` OR `analyze`     |
| Run multiple QA scripts or commands in sequence                           | `check`                    |

## Naming Convention

Script names in the `composer.json` file MUST be lower-case, and MUST use dashes
as word separators.

Examples of compliant script names:

- `foo`
- `foo-bar`
- `foo-bar-baz`

Examples of non-compliant script names:

- `Foo`
- `foo:bar`
- `foo_bar:Baz`

## Script Names

### `test`

If the `composer.json` file defines a script to run tests using a default
configuration, it MUST be named `test`.

This publication does not otherwise define the test tooling.

### `test-coverage`

If the `composer.json` file defines a script to run tests using a default
configuration, with coverage generation, it MUST be named `test-coverage`.

This publication does not otherwise define the test coverage tooling.

### `test-*`

If the `composer.json` file defines a script to run tests using alternative
configurations or approaches, it MUST use the prefix `test-` with a descriptive
suffix.

Examples:

- `test-behavior`
- `test-filter`
- `test-integation`
- `test-system`

Aside from `test-coverage`, this publication does not otherwise define the
meaning of any `test-*` descriptive suffix.

### `cs-fix`

If the `composer.json` file defines a script to run a coding style fixer
and/or code linter using a default configuration, it MUST be named `cs-fix`.

This publication does not otherwise define the style fixer or code linter
tooling.

### `analyse` or `analyze`

If the `composer.json` file defines a script to run static analysis using a
default configuration, it MUST be named EITHER `analyse` OR `analyze`.

N.b.: The naming alternatives reflect differences in typical usage by American
and British English speakers.

This publication does not otherwise define the static analysis tooling.

### `check`

If the `composer.json` file defines a script to run multiple quality-assurance
scripts or commands in sequence, it MUST be named `check`.

This publication does not otherwise define the specific scripts or commands,
nor the order in which they are to run.
