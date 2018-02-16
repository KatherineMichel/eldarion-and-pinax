# Eldarion and Pinax

<!--
Eldarion website, conferences

https://github.com/deep-reader/DeepReader | deep-reader/DeepReader: a highly modular, Vue.js-based framework designed for building online reading environments for deep reading of texts with rich annotations and integrated learning tools

https://twitter.com/jtauber/status/910149159470149632 | James Tauber on Twitter: "Thrilled to announce that I'll be leading the development of the next version of @PerseusDigLib with the @eldarion team and others"
https://github.com/PerseusDL | PerseusDL
https://twitter.com/PerseusDigLib
https://sourceforge.net/p/epidoc/wiki/Home/ | EpiDoc: Epigraphic Documents in TEI XML / Home / Home
https://github.com/diyclassics/perseus-experiments/blob/master/Perseus%20Plaintext%20Poetry.ipynb | perseus-experiments/Perseus Plaintext Poetry.ipynb at master · diyclassics/perseus-experiments

http://capitains.org/ | CapiTainS
https://github.com/Capitains/MyCapytain | Capitains/MyCapytain: CTS And Textual Resources Utility Library for Python 3

Stripe
https://www.reddit.com/r/django/comments/7do0uc/pinaxstripe_400_released_stripe_connect_support/ | pinax-stripe 4.0.0 Released - Stripe Connect support lands : django
https://github.com/pinax/pinax-stripe/milestone/11 | Rosie Milestone

Sites built with Pinax: https://github.com/pinax/pinax-theme-pinaxproject/blob/master/pinax_theme_pinaxproject/templates/example_sites/home.html

http://eldarion.com/blog/post/KijaLQaw/ | Getting Started With a Site: Your Waitinglist — Eldarion Blog

http://www.scrumguides.org/scrum-guide.html | Scrum Guide | Scrum Guides

Business Model Canvas
https://cdn.strategyzer.com/assets/marketing/canvases-business-model-canvas-a8509296e3cd543ee7c6881cada7082376d4dfdf4eac40e849490c0dba2d178b.svg | Artboard 101

http://theleanstartup.com/principles | The Lean Startup | Methodology

http://paltman.com/october-2018-review/ | October 2018 Review | Patrick Altman

http://blog.pinaxproject.com/section/community/ | The Pinax Project Blog | The Pinax Project Blog

https://www.youtube.com/channel/UCAPpNG85GLzUBwzYCjd4raQ | Pinax Project - YouTube - YouTube
https://github.com/orgs/eldarion/teams/developers | Developers · Eldarion, Inc. Discussion

https://thoughtstreams.io/ | ThoughtStreams — a micro-blog for every idea
https://github.com/eldarion/thought-streams | thought-streams/tests.py at master · eldarion/thought-streams

https://dashboard.heroku.com/apps/pinax-account-app | pinax-account-app | Heroku
https://pinax-account-app.herokuapp.com/ | example.com [localhost] | pinax-project-account

https://github.com/search?utf8=%E2%9C%93&q=org%3Apinax+label%3A%22up-for-grabs%22&type= | Search · org:pinax label:"up-for-grabs"
https://help.github.com/articles/searching-issues-and-pull-requests/ | Searching issues and pull requests - User Documentation

https://github.com/pinax/pinax-teams/tree/fixing-render-to-string-issue | pinax/pinax-teams at fixing-render-to-string-issue

https://unsplash.com/search/photos/road | 20+ Best Free Road Pictures on Unsplash

Location of site-packages
pipenv --venv

Then browse to:
lib/python3.6/site-packages

https://eldarion.com/blog/2018/02/06/countdown-perseus-50-scaife-launch/ | Countdown to the Perseus 5.0 “Scaife” Launch — Eldarion Blog
https://sites.tufts.edu/perseusupdates/2017/07/22/design-sprint-for-perseus-5-0open-greek-and-latin/ | Design Sprint for Perseus 5.0/Open Greek and Latin » Perseus Digital Library Updates
https://twitter.com/jtauber/status/951742629955371009 | James Tauber on Twitter: "If everyone who uses Perseus 4.0 moves over to Perseus 5.0, it may well be one of the largest (by user count) sites built with @vuejs. There… https://t.co/ENPwiSdRIq"

Style Guide

the way you know if `account` should be added to `known_third_party` is by setup.py “install_requires”. If DUA is in there then “account” should be in 3rd party. Same for other required apps. Check settings.py for the actual app name that needs to be in 3rd party… i.e. “django-user-accounts” app name is “account”.

```[testenv:checkqa]
commands =
    flake8 pinax
    isort --recursive --check-only --diff pinax -sp tox.ini
```
Run these separately on command line before invoking `detox` in order to catch issues.
 `flake8 pinax` looks good
`isort --recursive --check-only --diff pinax -sp tox.ini` isn’t so happy
but the solution is simple 
`isort --recursive pinax -sp tox.ini`
-->

About Pinax and State of Pinax

<!--
https://www.slideshare.net/jtauber/state-of-pinax/19-reusable_appquisition_potterpredictions | State of Pinax
https://www.slideshare.net/jtauber/state-of-pinax/33-Sites_Using_Pinax | reusable app quisition potterpredictions

https://www.slideshare.net/pydanny/pinax-long-tutorial-slides | Pinax Long Tutorial Slides
http://pydanny.blogspot.com/2010/ | pydanny: 2010

https://2016.djangocon.us/schedule/presentation/45/ | Presentation: Building JSON APIs with Django / Pinax
https://speakerdeck.com/brosner/pinax | Building JSON APIs with Django / Pinax // Speaker Deck
https://github.com/pinax/pinax-api | pinax/pinax-api: RESTful API adhering to the JSON:API specification
http://eldarion.com/blog/2016/08/18/eldarions-brian-rosner-speaks-djangocon-us-2016/ | Eldarion's Brian Rosner Speaks At DjangoCon US 2016 — Eldarion Blog
-->

Work in Progress
* [Pinax Groupware Starter Project GitHub](https://github.com/pinax/pinax-starter-projects/wiki/Groupware-Starter-Project)
* [PyCon Israel GitHub](https://github.com/eldarion/pycon-israel)
* [Patch Game GitHub](https://github.com/pinax/patch-game)
* [Conference Starter Project GitHub](https://github.com/pinax/pinax-starter-projects/wiki/Conference-Starter-Project)
* [Pinax Contributors Portal GitHub](https://github.com/pinax/pinax/wiki/Contributors-Portal)
* [Cloudspotting 2 GitHub](https://github.com/pinax/cloudspotting2)
* ["Continuously Deploying Python Packages to PyPI with CircleCI"](https://circleci.com/blog/continuously-deploying-python-packages-to-pypi-with-circleci)

<!--
Runtests
Link to explemplary demos (that use each app) in READMEs
Docs, documenting features
Tools used by Eldarion

https://www.youtube.com/watch?v=VlwfpzMVpRA | Cloudspotting Demo - YouTube
ttps://github.com/pinax/cloudspotting | pinax/cloudspotting: a starter project allowing you to create collections of cloud images, view other people’s collections, “like” a collection, etc.

https://www.npmjs.com/package/pinax-images-panel

http://pinaxproject.com/pinax/faq/ | FAQs - Pinax Documentation
https://github.com/pinax/pinax/wiki/Proposed-Docs-Outline

https://lincolnloop.com/blog/using-setuppy-your-django-project/ | Using setup.py in Your (Django) Project | Lincoln Loop

Inspired by Lincoln Loop "Using setup.py in Your (Django) Project" 
https://github.com/pinax/pinax-starter-projects/pull/56/commits/262c712da313e4ba4ee743654ddad5752d4a0268 | Create setup.py by grahamu · Pull Request #56 · pinax/pinax-starter-projects

Update contributor files
https://docs.python.org/3/library/glob.html#glob.glob | 11.7. glob — Unix style pathname pattern expansion — Python 3.6.4 documentation
-->

Eldarion
* [Eldarion](http://eldarion.com) and [Eldarion GitHub](https://github.com/eldarion)
* [Clients](http://eldarion.com/what-we-do)
* [Eldarion Clients GitHub](https://github.com/eldarion-client)
* [Eldarion YouTube](https://www.youtube.com/channel/UCnop70xOY_4dAr4YB9jjlOg)
* [Eldarion LinkedIn](https://www.linkedin.com/company/eldarion)

Pinax
* [Pinax](http://pinaxproject.com) and [Pinax Docs GitHub](https://github.com/pinax/pinax/tree/master/docs)
* [Pinax Wikipedia](https://en.wikipedia.org/wiki/Pinax)
* [Pinax Twitter](https://twitter.com/pinaxproject)
* [Pinax Blog](http://blog.pinaxproject.com) and [Pinax Medium](https://medium.com/pinax)
* [Pinax GitHub](https://github.com/pinax)
* [Pinax Slack Signup](http://slack.pinaxproject.com)
* [Pinax Slack](https://pinax.slack.com)
* [Pinax Hangouts](https://www.youtube.com/channel/UCAPpNG85GLzUBwzYCjd4raQ)

People
* [James Tauber](http://jtauber.com) and [J.K. Tauber](https://jktauber.com)
* [James Tauber GitHub](https://github.com/jtauber)
* [Patrick Altman](http://paltman.com), [Patrick Altman Twitter](https://twitter.com/paltman), and [Patrick Altman CodePen](https://codepen.io/paltman)

Site Care
* [Eldarion Site Care and Maintenance](http://eldarion.com/consulting/django-site-care)

Dedicated Python Hosting
* [Eldarion Cloud: A New DevOps PaaS Powered by Kubernetes (Formerly Gondor)](http://eldarion.cloud)
* [Kel](http://www.kelproject.com), [Kel GitHub](https://github.com/kelproject), and [Kel Docs GitHub](https://github.com/kelproject/kel-docs)

<!--
Eldarion Cloud,  Blog and Docs (formerly Gondor)
https://github.com/eldarion-gondor | Gondor
https://blog.eldarion.cloud/ 
http://eldarion-gondor.github.io/docs/#how-tos | Eldarion Cloud Documentation
-->

Pinax Packages
* [Warehouse Pinax Search](https://pypi.org/search/?q=pinax)
* [PyPi Pinax Search](https://pypi.python.org/pypi?%3Aaction=search&term=pinax&submit=search)

Warehouse Profiles
* [Patrick Altman](https://pypi.org/user/paltman)
* [Brian Rosner](https://pypi.org/user/brosner)

<!--
https://github.com/pinax/pinax-cli | pinax/pinax-cli: a tool for easily instantiating Pinax starter projects (django templates)

Packages
https://pypi.org/project/pinax-likes | pinax-likes · Warehouse (PyPI)
https://pypi.python.org/pypi/pinax-likes/#downloads | pinax-likes 3.0.0 : Python Package Index
https://pypi.python.org/pypi/pinax-documents | pinax-documents 1.0.0 : Python Package Index
-->

Current Release
* [Pinax Wiki](https://github.com/pinax/pinax/wiki)
* ["Upgrading app for Django v2.0"](https://github.com/pinax/pinax/wiki/Upgrading-app-for-Django-v2.0)
* ["Converting to CircleCi and Codecov"](https://github.com/pinax/pinax/wiki/Converting-to-CircleCi-and-Codecov)
* [Standardizing READMEs](https://github.com/pinax/pinax/wiki/Standardizing-READMEs)

Release Process
* [Pinax App Release Process](https://github.com/pinax/pinax/wiki/App-Release-Process)
* [Pinax Release Process](http://pinaxproject.com/pinax/release_process)
* [Pinax How-To Release a Starter Project](http://pinaxproject.com/pinax/how-tos/release-starter-project)

<!--
http://blog.pinaxproject.com/2017/09/08/simplifying-static-build-process-django-projects/ | Simplifying the Static Build Process in Django Starter Projects | The Pinax Project Blog
http://blog.pinaxproject.com/2017/09/18/remarking-pinax-theme-bootstrap-be-semantic/ | Remarking pinax-theme-bootstrap To Be Semantic | The Pinax Project Blog

http://blog.pinaxproject.com/2016/03/15/writing-better-documentation-and-why-documentation
-->

Tags and Releases
* [GitHub About Releases](https://help.github.com/articles/about-releases) and [GitHub Creating Releases](https://help.github.com/articles/creating-releases)
* [GitHub Working with Tags](https://help.github.com/articles/working-with-tags)

<!--
https://developer.github.com/v3/repos/releases/#create-a-release | Releases | GitHub Developer Guide
-->

Past Releases
* [Pinax 18.01 Plan](https://github.com/pinax/pinax/wiki/Pinax-18.01)
* [Pinax 16.10 Plan](https://github.com/pinax/pinax/wiki/Pinax-16.10-Plan)
* [Pinax 16.07](https://github.com/pinax/pinax/wiki/Pinax-16.07)
* [Checklist for 16.04 candidate apps](https://github.com/pinax/pinax/issues/113)
* [Pinax 16.04 Update Blog Post](http://blog.pinaxproject.com/2016/03/10/update-pinax-1604)
* [Pinax 16.04 Blog Post](http://blog.pinaxproject.com/2016/02/01/pinax-1604) and [Proposal for Pinax Distribution Versioning GitHub](https://github.com/pinax/pinax/issues/84)

<!--
http://blog.pinaxproject.com/2016/08/15/release-pinax-1607/ | Release of Pinax 16.07 | The Pinax Project Blog

https://github.com/pinax/pinax/issues/84#issuecomment-189625770 | Proposal for Pinax Distribution Versioning · Issue #84 · pinax/pinax
-->

Distribution Scripts

<!--
Pinax Release Script
https://github.com/pinax/pinax/blob/master/check.py | pinax/check.py at master · pinax/pinax
https://github.com/pinax/pinax/blob/master/projects.json
https://github.com/pinax/pinax/blob/master/distributions.json | pinax/distributions.json at master · pinax/pinax

https://github.com/cndn/intelligent-code-completion/blob/edb80a083f481aa30897d5cb91c2bc53708b9ec5/raw_data/45600_check.py | intelligent-code-completion/45600_check.py at edb80a083f481aa30897d5cb91c2bc53708b9ec5 · cndn/intelligent-code-completion
-->

Django, Kubernetes, React
* [Django](https://www.djangoproject.com)
* [Kubernetes](https://kubernetes.io)
* [React](https://facebook.github.io/react)

<!--
http://fontawesome.io/ | Font Awesome, the iconic font and CSS toolkit
https://fontawesome.com | Font Awesome 5 | Font Awesome
-->

Testing and CI
* [CircleCI](https://circleci.com)
* [Codecov](https://codecov.io)
* [Tox Read the Docs](https://tox.readthedocs.org)
* [Detox GitHub](https://github.com/tox-dev/detox) and [Detox PyPi](https://pypi.python.org/pypi/detox)
* [Coverage Read the Docs](https://coverage.readthedocs.io) and [Coverage Bitbucket](https://bitbucket.org/ned/coveragepy)
* [Django Test Plus](http://django-test-plus.readthedocs.io) and [Django Test Plus GitHub](https://github.com/revsys/django-test-plus)
* [isort GitHub](https://github.com/timothycrosley/isort)
* [Flake8 GitHub](https://gitlab.com/pycqa/flake8) and [Flake8 Docs](http://flake8.pycqa.org)
* [Flake8 Quotes GitHub](https://github.com/zheller/flake8-quotes)
* [Factory Boy GitHub](https://github.com/FactoryBoy/factory_boy) and [Factory Boy PyPi](https://pypi.python.org/pypi/factory_boy)

<!--
https://docs.python.org/3.7/distutils/sourcedist.html | 4. Creating a Source Distribution — Python 3.7.0b1 documentation
https://pypi.python.org/pypi/flake8 | flake8 3.5.0 : Python Package Index
https://tox.readthedocs.io/en/latest/examples.html | tox configuration and usage examples — tox 3.0.0rc2.dev5 documentation
https://codecov.io/#features | Codecov
https://pypi.org/project/flake8-confusables/ | flake8-confusables · Warehouse (PyPI)

https://docs.pipenv.org/ | Pipenv: Python Dev Workflow for Humans — pipenv 9.0.3 documentation
https://pipenv.readthedocs.io/en/latest/advanced.html#managing-system-dependencies | Advanced Usage of Pipenv — pipenv 8.0.8 documentation
https://www.kennethreitz.org/essays/pipenv-one-year-later-a-call-for-help | Pipenv: One Year Later & a Call for Help — Kenneth Reitz
https://github.com/pypa/pipfile | pypa/pipfile
https://speakerdeck.com/kennethreitz/the-future-of-python-dependency-management | The Future of Python Dependency Management // Speaker Deck


https://pypi.python.org/pypi/flake8

https://en.wikipedia.org/wiki/Manifest_file | Manifest file - Wikipedia

https://en.wikipedia.org/wiki/Smoke_testing_(software) | Smoke testing (software) - Wikipedia
https://en.wikipedia.org/wiki/Traceability_matrix | Traceability matrix - Wikipedia
https://en.wikipedia.org/wiki/Code_coverage
https://martinfowler.com/bliki/TestCoverage.html

https://www.reddit.com/r/Python/comments/7brkpn/how_we_maintain_high_levels_of_code_quality/ | How We Maintain High Levels of Code Quality : Python

http://eldarion.com/blog/2017/10/17/how-we-maintain-high-levels-code-quality | How We Maintain High Levels of Code Quality — Eldarion Blog
http://eldarion.com/blog/2017/07/13/5-reasons-you-should-care-about-code-coverage/ | 5 Reasons You Should Care about Code Coverage — Eldarion Blog
http://blog.pinaxproject.com/2015/12/08/how-test-against-multiple-python-versions-parallel/ | How to Test Against Multiple Python Versions in Parallel | The Pinax Project Blog
-->

How to Contribute
* [How to Contribute](http://pinaxproject.com/pinax/how_to_contribute)
* [How to Contribute Google Doc](https://docs.google.com/document/d/1f9hPTw3nelWy7nxaDawWP7EUl4QyeGeC4BNYeb4iWhU/edit)

<!--
https://github.com/pinax/pinax/blob/master/docs/how_to_contribute.md | pinax/how_to_contribute.md at master · pinax/pinax
-->

Example First-Timers Info
* [Pinax First-Timer Opportunity via Twitter](https://twitter.com/pinaxproject/status/687318459072446466) and [First-Timer](https://twitter.com/pinaxproject/status/694213861327659008)
* [How to Contribute to Pinax Blog Post](http://pinaxproject.com/pinax/ways_to_contribute) and [How to Contribute to Pinax Blog Post](http://blog.pinaxproject.com/2015/11/10/guide-how-contribute-pinax)
* [Pinax First Timers Only](http://blog.pinaxproject.com/2016/01/11/first-timers-only-and-new-labels), and [Pinax Issues GitHub](https://github.com/pinax/pinax/issues)

Triaging Labels
* difficulty: easy
* difficulty: medium
* difficulty: hard
* bug
* docs
* enhancement
* question
* for discussion
* backward incompatible change
* new starter project
* community
* up-for-grabs
* first-timers-only
* DjangoCon Sprint

Clients and Orgs
* [Companies Working with Pinax](http://pinaxproject.com/pinax/companies_working_with_pinax)
* [Pinax In the Wild](http://pinaxproject.com/pinax/in_the_wild)

Pinax Developer Profiles
* [Pinax Developer Profiles](https://docs.google.com/forms/d/1CdiEtvVyWLtdVZUXHLXoZI64K1qbslkOqSR0W5xz6_0/viewform)
