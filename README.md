# Pre-commit Config

**This repository is associated with a [blog post](https://www.laac.dev/blog/automating-convention-linting-formatting-python/)
about linting and formatting Python code. For a repo with more up to date configuration files
see [here](https://github.com/laactech/pre-commit-config-latest)**

[pre-commit](https://pre-commit.com/) is used to install four Python code linting and
formatting tools:
* [flake8](http://flake8.pycqa.org/en/latest/) a Python style guide linter
* [bandit](https://github.com/PyCQA/bandit) a Python security vulnerability linter
* [black](https://black.readthedocs.io/en/stable/) a Python automatic code formatter
* [isort](https://github.com/timothycrosley/isort) a Python automatic import formatter
* [seed-isort-config](https://github.com/asottile/seed-isort-config) a tool to statically
populate the "known_third_party" part of the `.isort.cfg`
