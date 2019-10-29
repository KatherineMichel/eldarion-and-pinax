# Pinax Improvements

Fix Windows problem
Checklists

Positive things:

Less positive things:

https://github.com/chaoss/metrics

The number one idea I took from Hynek's talk was to remove the friction from the process for the contributor.
Provide very easy to find guidance to the contributor.

Pinax organization-level community health file repo
https://help.github.com/en/articles/creating-a-default-community-health-file-for-your-organization
Use .github repo for community docs to make repos more DRY #151
https://github.com/pinax/pinax/issues/151
https://github.com/psf/.github

Supported file types
You can create organization-wide defaults for the following community health files:

Community health file	Description
CODE_OF_CONDUCT.md	A CODE_OF_CONDUCT file defines standards for how to engage in a community. For more information, see "Adding a code of conduct to your project."
CONTRIBUTING.md	A CONTRIBUTING file communicates how people should contribute to your project. For more information, see "Setting guidelines for repository contributors."
FUNDING.yml	A FUNDING file displays a sponsor button in your repository to increase the visibility of funding options for your open source project. For more information, see "Displaying a sponsor button in your repository."
Issue and pull request templates	Issue and pull request templates customize and standardize the information you'd like contributors to include when they open issues and pull requests in your repository. For more information, see "About issue and pull request templates."
SECURITY.md	A SECURITY file gives instructions for how to responsibly report a security vulnerability in your project. For more information, see "Adding a security policy to your repository."
SUPPORT.md	A SUPPORT file lets people know about ways to get help with your project. For more information, see "Adding support resources to your project."

Work Completed

## Pinax 18.01 Release Overview

The Pinax 18.01 release was completed in the spring of 2018. Around 28 Pinax apps were included. Most updates are explained in [Converting to CircleCi and Codecov](https://github.com/pinax/pinax/wiki/Converting-to-CircleCi-and-Codecov) and [Upgrading app for Django v2.0](https://github.com/pinax/pinax/wiki/Upgrading-app-for-Django-v2.0)

Updates completed in the 18.01 release:
* Dropped support for Django 1.8, 1.9, 1.10 and Python 3.3
* Added support for Django 2.0 (See: [Upgrading app for Django v2.0](https://github.com/pinax/pinax/wiki/Upgrading-app-for-Django-v2.0))
* Converted from Travis CI to CircleCI and CodeCov (See: [Converting to CircleCi and Codecov](https://github.com/pinax/pinax/wiki/Converting-to-CircleCi-and-Codecov))
* Changed app README.md layouts
* Moved docs to README.mds
* Updated setup.py format
* Updated .gitignore (possible additions: VSCode/PyCharm)

## Pinax 19.xx Release Overview

High level-updates proposed for the 19.xx release:
* Drop support for Django 1.11 and Python 2.7 [(Official support ends in 2020)](https://docs.djangoproject.com/en/dev/faq/install/#what-python-version-should-i-use-with-django)
* Drop support for Django 2.0 and Python 3.4 (Django 2.0 end-of-life was April 2019, Python 3.4 end-of-life was March 2019: https://docs.djangoproject.com/en/2.2/releases/2.0/#python-compatibility)
* Add support for Django 2.1, 2.2 and Python 3.7
* Add support for [Black](https://github.com/python/black) pending stable release [(Django Technical Board has adopted Black as Django's official formatter)](https://twitter.com/andrewgodwin/status/1127027840296177666)
* Improve README.mds and community docs (possibly including auto-deploy)
* Add auto-package publish using CircleCI (Michael has offered to assist with this)

The 19.xx release will focus on apps that were included in the 18.01 release. If possible, we will included apps in the 19.xx release that were not included in the 18.01 release.

See also: https://github.com/pinax/pinax/issues/146

## A Few Important Notes About the Release Process

### Standardization and Consistency

We strive for standardization and consistency anytime possible. This makes it easier to maintain Pinax, and easier for newcomers to understand individual projects and apps and the ecosystem as a whole.

### Version

* Version follows the convention yy.mm for limited timeframe
* Otherwise yy.xx

### Oversight

* We use a wiki to store current and historical release info: https://github.com/pinax/pinax/wiki
* We use a spreadsheet to track updates to individual apps
* At times, GitHub milestones have been used within repos

### Triaging

Anytime possible:

* Triage PRs
* Merge PRs
* Close issues

### Pinax Starter App

[Pinax Starter App](https://github.com/pinax/pinax-starter-app) should be updated to reflect the latest best practices included in the new release (See: https://github.com/pinax/pinax-starter-app/issues/24). Pinax Starter App can be used to generate a new Pinax app.

### Nice to Have

* Automation improvements
* CI improvements
* Packaging improvements

## High Level Release Instructions

### If You Are Submitting a Release PR

* Make the relevant updates to the app repo based on the info in this file
* After making the CircleCI and tox updates in particular, run Makefile by using the command ```Make``` or run ```tox --parallel``` directly to test the new matrix; fix the errors you see in the terminal until you see green at the end of the process
* Update the changelog and app version number in setup.py (see [SemVer](https://semver.org/) for more info about how version number works)
* Create a PR

### If You Are Accepting a Release PR

* Before merging PR, check that all of the necessary updates have been made, including update to changelog and app version number
* Tag the release and publish to PyPi (see the official publishing/PyPi docs and GitHub docs for more info about packaging, releases, and publishing to PyPi)
* After publishing to PyPi, check that the app PyPi page renders properly (Note: if you need to re-publish, PyPi will not let you use the existing version number)

## App Repo Files

### Files to Include in App Repos

All apps should include:

```
.circleci/config.yml
.gitignore
AUTHORS
CONTRIBUTING.md
LICENSE
Makefile
MANIFEST.in
README.md
runtests.py
setup.cfg
setup.py
tox.ini
```

### makemigrations.py

All apps that have models should include `makemigrations.py`. Double check that they exist and are accurate.


### Update .gitignore


### Update .coveragerc

### Update Makefile

In Makefile and elsewhere, change references of `detox` to `tox` and `tox --parallel`. detox has been merged into tox (tox [parallel mode](https://tox.readthedocs.io/en/latest/example/basic.html#parallel-mode) has replaced detox) (See also: https://github.com/pinax/pinax/issues/143)

In the apps included in the most recent release, references to docs, documentation, and Sphinx should be gone, due to docs having been moved to READMEs. Docs no longer need to be generated via Makefile. This update might not have been made yet in deprecated apps.

## Continuous Integration, Coverage, and Test Matrix

### Update CircleCi Configuration

Note: Patrick has requested that Pinax be added to the [GitHub Actions](https://github.com/features/actions) beta. GitHub Actions now includes CI/CD and might render CircleCi unnecessary for Pinax.

Update `.circleci/config.yml` files with current test matrix info

Note the additional `- v2-deps` is not a typo. It's for caching and should be added to all app `config.yml` files. Also, all apps should show the same Docker image version numbers.


### Add CodeCov Support

The coverage.py configs can be consolidated into the `tox.ini` file. The `.coveragerc` file can then be removed, because coverage.py can read from the `tox.ini` file (See: https://coverage.readthedocs.io/en/coverage-4.4.2/config.html). Otherwise, we have some duplicate info within `.coveragerc` and `tox.ini` files.

We would need to ensure that the tox.ini includes any relevant info that is only in the .coveragerc files, specifically, all of the omitted paths. This will primarily involve the `admin.py` path (See `.coveragerc` example below). Note: `branch = true` and `branch = 1` are both Boolean values (See: https://coverage.readthedocs.io/en/v4.5.x/config.html#syntax)

`app` refers to the name of the app

### Convert tox.ini
  
Update `tox.ini` files with current test matrix info

This configuration performs testing on Python 3.5, 3.6, and 3.7 alongside Django 2.1, and 2.2. It requires `isort` for automated import sorting and `flake8-quotes` for enforcing double quote standard.

`flake8`, `flake8-quotes`, and `isort` have been updated to most recent versions.

Note the `[isort]` - `known_third_party` section should contain appropriate app names for every application listed in setup.py `install_requires` section. The `tox.ini` example below is appropriate for this snippet from `setup.py`:

```python
# setup.py

setup(
    # other settings
    install_requires=[
        "django-appconf>=1.0.2",
        "django-user-accounts>=2.1.0",
    ],
)
```

```ini
deps =
    coverage
    codecov
    
commands =
    coverage run setup.py test
    coverage report -m --skip-covered
```

## Packaging

### Possible Packaging Improvements

We need to review our packaging process and incorporate any applicable new best practices

* Consider using [Twine](https://github.com/pypa/twine), including updating docs (See: https://github.com/pinax/pinax/issues/144)
* Consider adding `check-manifest` and `python setup.py` check tox.ini (See: https://github.com/pypa/sampleproject/blob/master/tox.ini)
* Add auto-package publish using CircleCI (not sure how credentials would be dealt with; See .gitignore)

### Things to Watch For

* Update Pinax team email in setup.py (team@pinaxproject.com not team@pinaxprojects.com) (See: https://github.com/pinax/pinax/issues/139)
* Make setup.py content order consistent across all apps
* Make sure we are consistent with SemVer

### Update setup.cfg

If we drop Python 2 support, apparently we can remove the universal wheel syntax from the set.cfg and use a pure Python wheel instead (See the [PyPi Sample Project](https://github.com/pypa/sampleproject/blob/master/setup.cfg) or [Packaging Tutorial Wheels](https://packaging.python.org/guides/distributing-packages-using-setuptools/#wheels) section for more info). That is, if a set.cfg is needed at all.

With universal wheel syntax:

```python
[bdist_wheel]
universal=1
```

Without universal wheel syntax:

```python
[bdist_wheel]
```

### Update setup.py

This version of `setup.py` shows common configuration. App-specific data includes:

```python
from setuptools import find_packages, setup

VERSION = "0.0"
LONG_DESCRIPTION = """
.. image:: http://pinaxproject.com/pinax-design/patches/pinax-app.svg
    :target: https://pypi.python.org/pypi/pinax-app/

=========
Pinax App
=========

.. image:: https://img.shields.io/pypi/v/pinax-app.svg
    :target: https://pypi.python.org/pypi/pinax-app/

\ 

.. image:: https://img.shields.io/circleci/project/github/pinax/pinax-app.svg
    :target: https://circleci.com/gh/pinax/pinax-app
.. image:: https://img.shields.io/codecov/c/github/pinax/pinax-app.svg
    :target: https://codecov.io/gh/pinax/pinax-app
.. image:: https://img.shields.io/github/contributors/pinax/pinax-app.svg
    :target: https://github.com/pinax/pinax-app/graphs/contributors
.. image:: https://img.shields.io/github/issues-pr/pinax/pinax-app.svg
    :target: https://github.com/pinax/pinax-app/pulls
.. image:: https://img.shields.io/github/issues-pr-closed/pinax/pinax-app.svg
    :target: https://github.com/pinax/pinax-app/pulls?q=is%3Apr+is%3Aclosed

\ 

.. image:: http://slack.pinaxproject.com/badge.svg
    :target: http://slack.pinaxproject.com/
.. image:: https://img.shields.io/badge/license-MIT-blue.svg
    :target: https://opensource.org/licenses/MIT/

\ 

``pinax-app`` is a useful app for the Django web framework.
 
``pinax-app`` does this and that.

Supported Django and Python Versions
------------------------------------

+-----------------+-----+-----+-----+
| Django / Python | 3.5 | 3.6 | 3.7 |
+=================+=====+=====+=====+
|  2.1            |  *  |  *  |  *  |
+-----------------+-----+-----+-----+
|  2.2            |  *  |  *  |  *  |
+-----------------+-----+-----+-----+
"""

setup(
    author="Pinax Team",
    author_email="team@pinaxproject.com",
    description="<project description> for the Django web framework",
    name="pinax-app",
    long_description=LONG_DESCRIPTION,
    version=VERSION,
    url="http://github.com/pinax/pinax-app/",
    license="MIT",
    packages=find_packages(),
    package_data={
        "app_name": []
    },
    install_requires=[
        "django>=2.1",
    ],
    tests_require=[
    ],
    test_suite="runtests.runtests",
    classifiers=[
        "Development Status :: 5 - Production/Stable",
        "Environment :: Web Environment",
        "Framework :: Django",
        "Framework :: Django :: 2.1",
        "Framework :: Django :: 2.2",
        "Intended Audience :: Developers",
        "License :: OSI Approved :: MIT License",
        "Operating System :: OS Independent",
        "Programming Language :: Python",
        "Programming Language :: Python :: 3.5",
        "Programming Language :: Python :: 3.6",
        "Programming Language :: Python :: 3.7",
        "Topic :: Software Development :: Libraries :: Python Modules",
    ],
    zip_safe=False
)
```

### MANIFEST.in

The MANIFEST.in should include:

```python
include AUTHORS
include LICENSE
include README.md
```

The MANIFEST.in could include any of the following lines, depending upon if that folder is included in the app:

```python
recursive-include pinax/<app>/static *
recursive-include pinax/<app>/locale *
recursive-include pinax/<app>/templates *
```

## Unit Tests

### Add Tests

A few apps are still missing test coverage.

TODO

### Test URLs

Apps that do not include URLs need not have a test directory ```urls.py``` file or a ```ROOT_URLCONF="pinax.<app>.tests.urls",``` setting in the ```runtests.py``` file.

### Run Tests

* Fix inconsistencies across code bases (such as ```MIDDLEWARE_CLASSES=[]``` versus ```MIDDLEWARE=[]```)

## Templates

Some apps should have templates and are missing them. Some templates that should be in pinax-templates are still in individual apps. Add or move templates when possible.

If templates are added to pinax-templates, add the standard pinax-templates blurb to the README of the app the templates belong to.

## README.md

* Convert docs from README.rst to README.md (with the MANIFEST.in reflecting the new file name ending)


Docs should have been moved to the READMEs and the READMEs organized into sections as seen in [pinax-announcements README](https://github.com/pinax/pinax-announcements/blob/master/README.md).

### Standard README.md Table of Contents

Table of Contents
* About Pinax
* Overview
  * Features
  * Dependencies (if applicable)
  * Supported Django and Python Versions
* Documentation
  * Installation
  * Usage
  * Templates (if applicable)
* Change Log
* History (if applicable)
* Contribute
* Code of Conduct
* Connect with Pinax
* License

### README.md Accuracy and Updates

* Check for README ToC deadlinks, README typos, README layout inconsistency
* Verify app name is correct throughout README.md (usually pinax-app)
* Add README.md patches, where needed (Patrick has created these in the past)
* Verify README.md badges are correct (including CircleCi and CodeCov badges), in correct order, and rendering properly (also in setup.py)
* Add/improve features descriptions, if possible (also in setup.py)
* Make any necessary updates to dependencies, support Django/Python versions, and installation/usage
* Update the test support matrix in README.md  (and setup.py; See Supported Versions Matrix Example section)
* If templates have been added to pinax-templates, a standard pinax-templates blurb should have been added to README of the app the templates belong to.


* Add a section to the README with a link to an exemplary demo the app is included in
* Update supported versions matrix
* Ensure that code-fencing is accurate
* Ensure that change logs are accurate

## Community

* Update and standardize LICENSEs across repos
* Update and standardize CONTRIBUTING.md across all projects/apps (See: https://github.com/pinax/pinax/issues/149). 
* Update and standardize AUTHORS files across all projects/apps; Could this be automated? (See: https://github.com/pinax/pinax/issues/148)

### Deprecation

* Mark deprecated repos as deprecated, especially in the repo description line.

### Tags

Although not a necessity, tags are nice to have, and already included in some Pinax repos.

Possible tags:

* django-project-template
* python
* django
* pinax

## Documentation, Pinax Starter Projects, and Demos

### Improving Documentation

* Ensure basic installation instructions exist
* Improve usage docs
* Tutorials

### Improving Pinax Starter Projects and Demos

* Create or improve a Pinax Starter Project
* Create a demo that showcases a Pinax Starter project or app(s)
