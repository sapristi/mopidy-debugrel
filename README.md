# mopidy-debugrel

![PyPI - Version](https://img.shields.io/pypi/v/mopidy-debugrel?link=https://pypi.org/p/mopidy-debugrel)
![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/sapristi/mopidy-debugrel/ci.yml?link=https://github.com/sapristi/mopidy-debugrel/actions/workflows/ci.yml)
![Codecov](https://img.shields.io/codecov/c/gh/sapristi/mopidy-debugrel?link=https://codecov.io/gh/sapristi/mopidy-debugrel)

Mopidy extension that provides a debugging Read-Eval loop over http


## Installation

Install by running:

```sh
python3 -m pip install mopidy-debugrel
```

See https://mopidy.com/ext/debugrel/ for alternative installation methods.


## Configuration

Before starting Mopidy, you must add configuration for
mopidy-debugrel to your Mopidy configuration file:

```ini
[debugrel]
# TODO: Add example of extension config
```


## Project resources

- [Source code](https://github.com/sapristi/mopidy-debugrel)
- [Issues](https://github.com/sapristi/mopidy-debugrel/issues)
- [Releases](https://github.com/sapristi/mopidy-debugrel/releases)


## Development

### Set up development environment

Clone the repo using, e.g. using [gh](https://cli.github.com/):

```sh
gh repo clone sapristi/mopidy-debugrel
```

Enter the directory, and install dependencies using [uv](https://docs.astral.sh/uv/):

```sh
cd mopidy-debugrel/
uv sync
```

### Running tests

To run all tests and linters in isolated environments, use
[tox](https://tox.wiki/):

```sh
tox
```

To only run tests, use [pytest](https://pytest.org/):

```sh
pytest
```

To format the code, use [ruff](https://docs.astral.sh/ruff/):

```sh
ruff format .
```

To check for lints with ruff, run:

```sh
ruff check .
```

To check for type errors, use [pyright](https://microsoft.github.io/pyright/):

```sh
pyright .
```

### Setup before first release

Before the first release, you must [enable trusted publishing on
PyPI](https://docs.pypi.org/trusted-publishers/creating-a-project-through-oidc/)
so that the `release.yml` GitHub Action can create the PyPI project and publish
releases to PyPI.

When following the instructions linked above, use the following values in the
form at PyPI:

- Publisher: GitHub
- PyPI project name: `mopidy-debugrel`
- Owner: `sapristi`
- Repository name: `mopidy-debugrel`
- Workflow name: `release.yml`
- Environment name: `pypi` (must match environment name in `release.yml`)

### Making a release

To make a release to PyPI, go to the project's [GitHub releases
page](https://github.com/sapristi/mopidy-debugrel/releases)
and click the "Draft a new release" button.

In the "choose a tag" dropdown, select the tag you want to release or create a
new tag, e.g. `v0.1.0`. Add a title, e.g. `v0.1.0`, and a description of the changes.

Decide if the release is a pre-release (alpha, beta, or release candidate) or
should be marked as the latest release, and click "Publish release".

Once the releease is created, the `release.yml` GitHub Action will automatically
build and publish the release to
[PyPI](https://pypi.org/project/mopidy-debugrel/).


## Credits

- Original author: [Mathias Millet](https://github.com/sapristi)
- Current maintainer: [Mathias Millet](https://github.com/sapristi)
- [Contributors](https://github.com/sapristi/mopidy-debugrel/graphs/contributors)
