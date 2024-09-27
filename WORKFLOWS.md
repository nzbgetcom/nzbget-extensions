# Reusable workflows for NZBGet Extensions:

- [Prospector](#prospector)
- [Manifest](#manifest)
- [Tests](#tests)
- [Release](#release)

## Prospector

Runs [Prospector](https://prospector.landscape.io) static analysis check (strictness - medium, bundled libs ignored).

Recommended use: branch and tags push

Example:

```
jobs:
  prospector:
    uses: nzbgetcom/nzbget-extensions/.github/workflows/prospector.yml@main
```

## Manifest

Runs extension manifest check with check-jsonschema.

Recommended use: branch and tags push

Example:

```
jobs:
  manifest:
    uses: nzbgetcom/nzbget-extensions/.github/workflows/manifest.yml@main
```

## Tests

Can be used with extensions written in python. Runs tests check with specified python versions.

Recommended use: branch and tags push

Parameters:

- `python-versions`

  Python versions for running tests, space separated

- `supported-python-versions`

  Python versions for which tests must be passed without error

- `test-script`

  Name of test script in repository

- `debug`

  Enable debug output, recommended

Example:

```
jobs:
  tests:
    uses: nzbgetcom/nzbget-extensions/.github/workflows/python-tests.yml@main
    with:
      python-versions: "3.6 3.7 3.8 3.9 3.10 3.11 3.12"
      supported-python-versions: "3.8 3.9 3.10 3.11 3.12"
      test-script: tests.py
      debug: true
```

## Release

Create extension release from tag.

Recommended use: `v*` tags push

Parameters:

- `release-file-list`

  Space separated list of files to include in release archive. Wildcards can be used. To include directory with contents, end its name with '/'

- `release-file-name`

  Base file name for release archive. For an example: `videosort` will create release archives like `videosort-10.9-dist.zip`

- `release-dir`

  Top level directory in release archive to put all files in

Example:

```
name: release

on:
  push:
    tags:
    - "v*"

jobs:
  release:
    uses: nzbgetcom/nzbget-extensions/.github/workflows/extension-release.yml@main
    with:
      release-file-list: lib/ ChangeLog.txt README.* main.py manifest.json
      release-file-name: videosort
      release-dir: VideoSort
```
