# action-luacheck

> A github action that uses luacheck to lint full codebases or specific files

![](/docs/github_luacheck_action.png)

# How to use

#### Basic usage

```yaml
on: [push]

jobs:
  lint-luacheck:
    runs-on: ubuntu-latest
    name: Luacheck linting
    steps:
      - name: Checkout Repository
        uses: actions/checkout@v2
      - name: Run Luacheck
        uses: RagedUnicorn/action-luacheck@[version]
```

#### Custom Path and Arguments

```yaml
on: [push]

jobs:
  lint-luacheck:
    runs-on: ubuntu-latest
    name: Luacheck linting
    steps:
      - name: Checkout Repository
        uses: actions/checkout@v2
      - name: Run Luacheck
        uses: RagedUnicorn/action-luacheck@[version]
        with:
            files: code/
            args: -q
```

# License

MIT License

Copyright (c) 2021 Michael Wiesendanger

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
