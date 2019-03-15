# pre-commit Config

Configuration files leveraging pre-commit for Python code linting and formatting.

[pre-commit](https://pre-commit.com/) is used to install four Python code linting and
formatting tools:
* [flake8](http://flake8.pycqa.org/en/latest/) a Python style guide linter
* [bandit](https://github.com/PyCQA/bandit) a Python security vulnerability linter
* [black](https://black.readthedocs.io/en/stable/) a Python automatic code formatter
* [isort](https://github.com/timothycrosley/isort) a Python automatic import formatter
* [seed-isort-config](https://github.com/asottile/seed-isort-config) a tool to statically
populate the "known_third_party" part of the `.isort.cfg`

## Getting started
**Requires `python >=3.6`, `pre-commit>=1.14` and a `git` repository**

1. Copy the following files to the root of your Python project:
    * .pre-commit-config.yaml
    * .flake8
    * .isort.cfg
    * pyproject.toml
2. `git add` the previous files to your git repository
3. Run `pip install pre-commit`
4. Run `pre-commit install`

Now on every commit, `pre-commit` will use a git hook to run the tools.

**Warning: the first commit will take some time because the tools are being installed by
`pre-commit`**

## Resolving failed commits

* If `black` or `isort` fail, they have reformatted your code. `git add` and `git commit`
the changes.
* If `flake8` or `bandit`, they will output a complaint and where that complaint exists.
Fix the code that they complain about and `git add` and `git commit` the changes.
* If `seed-isort-config` fails, the `.isort.cfg` file has been modified. `git add` and
`git commit` the changes.
