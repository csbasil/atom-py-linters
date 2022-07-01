[Atom-Py-Linters](https://atom.io/packages/py-linters)
===================

**Customizable Python Lintor for Atom**

[![repo status Active](https://www.repostatus.org/badges/latest/active.svg "repo status Active")](https://www.repostatus.org/#active)
[![last commit](https://img.shields.io/github/last-commit/csbasil/atom-py-linters)](https://github.com/csbasil/atom-py-linters/commits/master)

[![py-linters_BugTracker](https://img.shields.io/github/issues/csbasil/atom-py-linters.svg)][py-linters_BugTracker]
[![Build Status](https://travis-ci.org/csbasil/atom-py-linters.svg?branch=master)](https://travis-ci.org/cs/atom-py-linters)

This [atom][atom homepage] package is a modified version of atom [python-linters][python-linters homepage] package. It is an all-in-one linter for [python][python homepage] code which internally use multiple linting tools:

- [flake8][flake8 homepage]
- [mypy][mypy homepage]
- [pydocstyle][pydocstyle homepage]
- [pylint][pylint homepage]

The lint triggers of all of those linting tools can individually be configure to
* `Lint as you type`
* `Lint on file save`
* `Never`

If any of the above lint tool is not installed, it will be detected and a user friendly message will guide you to either install it or change its lint trigger to 'Never'.

To provide specific lint options, `py-linters` supports `setup.cfg` configuration file format <a href="http://renesd.blogspot.com/2017/02/setupcfg-solution-to-python-config-file.html">which is supported by all of the above lint tool</a>.

Having lint options in a file external to the IDE settings allows to share the configuration with other process like manual run or CI and therefore obtain consistent lint results.

To provide project specific package configurations, `py-linters` support an external toml file.  When toml file is provided, all the global settings for `py-linters` package is ignored and settings from toml file is used. This feature allows to override the global `py-linters` settings and keeps project specific `py-linters` configurations. 

## Toml File Options
Following variables can be set from toml for project specific configurations:
```
PythonPath="%PROJECT_PATH/env/bin"
PythonExecutable="%PROJECT_PATH/env/bin/python3"
LintConfig=""
```
All empty varibles in the toml must be provided with empty strings like `LintConfig`

## Prerequisites

- [atom](https://atom.io/) must be installed which will provide the apm command aka *Atom Package Manager*.

## Installation Steps

	apm install py-linters

## ⎇ Alternatives

Use the following atom linting packages:
- https://atom.io/packages/python-linters
- https://atom.io/packages/linter-flake8
- https://atom.io/packages/linter-mypy
- https://atom.io/packages/linter-pydocstyle
- https://atom.io/packages/linter-pylint


## ⚖️ License

This project is licensed under the MIT License - see the [LICENSE.txt](LICENSE.txt) file for details

## 👩👨
* [You want to contribute?](CONTRIBUTING.md)
* [You need support?](SUPPORT.md)

[atom homepage]: https://atom.io/
[python homepage]: https://www.python.org
[flake8 homepage]: http://flake8.pycqa.org/
[mypy homepage]: http://www.mypy-lang.org/
[pydocstyle homepage]: https://pypi.org/project/pydocstyle/
[pylint homepage]: https://www.pylint.org/
[python-linters homepage]: https://github.com/elarivie/atom-python-linters
[py-linters_BugTracker]: https://github.com/csbasil/atom-py-linters/issues
