# setup-actionlint action

easy way to install [actionlint](https://github.com/rhysd/actionlint) in your GitHub
Actions workflows.

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@9c091bb21b7c1c1d1991bb908d89e4e9dddfe3e0  # v7.0.0
      - uses: pcrockett/setup-actionlint@LATEST_RELEASE_TAG
```

if you don't want to use the default version of actionlint that comes with this action, you
can specify your own version and checksum:

```yaml
- uses: pcrockett/setup-actionlint@LATEST_RELEASE_TAG
  with:
    version: '1.7.12'
    checksum: '8aca8db96f1b94770f1b0d72b6dddcb1ebb8123cb3712530b08cc387b349a3d8'
```

**recommended:** run [pinact](https://github.com/suzuki-shunsuke/pinact) to pin your
actions to a specific release. don't worry, if you're using Dependabot, Renovate, etc.,
they will update your pins correctly for you.

```bash
pinact run --update
```
