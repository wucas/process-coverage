# coverage-for-codecov

This GitHub action uploads coverage data for GAP packages to codecov.

## Usage

The action `coverage-for-codecov` has to be called by the workflow of a GAP
package.
By default it
- processes the coverage data gathered during the action
  [gap-actions/run-test-for-packages](https://github.com/gap-actions/run-test-for-packages)
- uploads the coverage data to `codecov.io`.

### Example

The following is a minimal example to run this action.

```yaml
name: CI

on:
  push:
  pull_request:

jobs:
  # The CI test job
  test:
    name: CI test
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v2
      - uses: gap-actions/setup-gap-for-packages@v1
      - uses: gap-actions/run-test-for-packages@v2
      - uses: gap-actions/coverage-for-codecov@v1
```

## Contact
Please submit bug reports, suggestions for improvements and patches via
the [issue tracker](https://github.com/gap-actions/coverage-for-codecov/issues)
or via email to
[Sergio Siccha](mailto:siccha@mathematik.uni-kl.de).

## License
The action `coverage-for-codecov` is free software; you can redistribute
and/or modify it under the terms of the GNU General Public License as published
by the Free Software Foundation; either version 2 of the License, or (at your
opinion) any later version. For details, see the file `LICENSE` distributed
with this action or the FSF's own site.
