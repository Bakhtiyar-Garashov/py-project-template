# Python Project Template

Python project structure based on best practices, focused on security, automation and coding style.

## Prerequisites

Python 3.8+

First install [copier](https://pypi.org/project/copier/) and [copier_templates_extensions](https://pypi.org/project/copier-templates-extensions/)

`pip3 install copier`

`pip3 install copier-templates-extensions`

Then of course you need to have [GNU make](https://www.gnu.org/software/make/) installed on your machine.

## How to create the project?

* Go to the root folder where you are going to create the Python project. For eg, for me it is called `~/REPOS/others/`
`cd ~/REPOS/others/`

* Run copier as:

`copier copy --trust git@github.com:ShahriyarR/py-project-template.git py-remove-me`

or

`python3 -m copier copy --trust git@github.com:ShahriyarR/py-project-template.git py-remove-me`

* Answer the questions.

```
🎤 Project name
   py-remove-me
🎤 Package name
   pyremoveme
🎤 Authors full name
   rzayev sehriyar
🎤 Authors email
   rzayev.sehriyar@gmail.com
🎤 Project description
   awesome project
🎤 Project version
   0.0.1
🎤 Do you want to install virtualenv?
   Yesn)
🎤 Python version.
   3.10
🎤 Enable pre-commit hooks?
   Yesn)
🎤 Enable Docker?
   Yesn)

Copying from template version 0.0.0.post11.dev0+15688cd
    create  .
    create  Makefile
    create  .pylintrc
    create  tests
    create  tests/__init__.py
    create  tests/conftest.py
    create  ci
    create  ci/Dockerfile
    create  pyproject.toml
    create  pytype.cfg
    create  src
    create  src/pyremoveme
    create  src/pyremoveme/__init__.py
    create  src/pyremoveme/service
    create  src/pyremoveme/service/__init__.py
    create  src/pyremoveme/domain
    create  src/pyremoveme/domain/__init__.py
    create  src/pyremoveme/configurator
    create  src/pyremoveme/configurator/__init__.py
    create  src/pyremoveme/configurator/settings
    create  src/pyremoveme/configurator/settings/base.py
    create  src/pyremoveme/configurator/settings/__init__.py
    create  src/pyremoveme/entrypoints
    create  src/pyremoveme/entrypoints/__init__.py
    create  src/pyremoveme/entrypoints/main.py
    create  src/pyremoveme/entrypoints/web
    create  src/pyremoveme/entrypoints/web/__init__.py
    create  src/pyremoveme/entrypoints/cli
    create  src/pyremoveme/entrypoints/cli/__init__.py
    create  src/pyremoveme/utils
    create  src/pyremoveme/utils/__init__.py
    create  src/pyremoveme/utils/common.py
    create  .gitignore
    create  README.md
    create  .pre-commit-config.yaml
```

* You will have ready-to-go project structure with all optional dependencies.

## How to use?

You need to master the Makefile and make command to fully create advance developer experience.

Let's see what we have?

* First go to the new created project directory:

`cd ~/REPOS/others/py-remove-me`

* Install project in production mode:

`make install`

* Install project in development mode, especially useful

`make install-dev`

* Format, sort the imports and also check the style

`make format`

* Run linter for final check

`make lint`

* Run tests all non-slow and non-integrated tests

`make test`

* Run slow tests

`make test-slow`

* Run integration tests

`make test-integration`

* Run test coverage

`make test-cov`

* Run type check

`make type-check`

* Run security check

`make secure`


# TODO:

* Add GitHub workflows/CI runs.
* Update Makefile for adding separate test runs. test-slow, test-integration etc.
* Respectively add pytest marks.
* Issue and PR templates