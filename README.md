# Eldarion and Pinax

<!--
Mine
https://dashboard.heroku.com/apps/pinax-account-app | pinax-account-app | Heroku
https://pinax-account-app.herokuapp.com/ | example.com [localhost] | pinax-project-account

https://github.com/pinax/pinax-teams/tree/fixing-render-to-string-issue | pinax/pinax-teams at fixing-render-to-string-issue

http://www.scrumguides.org/scrum-guide.html | Scrum Guide | Scrum Guides

Business Model Canvas
https://cdn.strategyzer.com/assets/marketing/canvases-business-model-canvas-a8509296e3cd543ee7c6881cada7082376d4dfdf4eac40e849490c0dba2d178b.svg | Artboard 101

http://theleanstartup.com/principles | The Lean Startup | Methodology

https://www.python.org/dev/peps/pep-0496/ | PEP 496 -- Environment Markers | Python.org
https://www.python.org/dev/peps/pep-0508/#id23 | PEP 508 -- Dependency specification for Python Software Packages | Python.org
https://www.python.org/dev/peps/pep-0394/ | PEP 394 -- The "python" Command on Unix-Like Systems | Python.org
https://code.djangoproject.com/ticket/29250 | #29250 (Add 'django_version' context variable reference documentation for startapp and startproject) – Django

http://initd.org/psycopg/articles/2018/02/08/psycopg-274-released/ | Psycopg 2.7.4 released | Psycopg



Eldarion website, conferences

http://eldarion.com/blog/post/KijaLQaw/ | Getting Started With a Site: Your Waitinglist — Eldarion Blog

https://thoughtstreams.io/ | ThoughtStreams — a micro-blog for every idea
https://github.com/eldarion/thought-streams | thought-streams/tests.py at master · eldarion/thought-streams


Style Guide


Location of site-packages
pipenv --venv

Then browse to:
lib/python3.6/site-packages

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
* [State of Pinax: DjangoCon 2009](https://www.slideshare.net/jtauber/state-of-pinax)

<!--
Eldarion Year in Review blog posts

http://paltman.com/october-2018-review/ | October 2018 Review | Patrick Altman

https://www.slideshare.net/search/slideshow?searchfrom=header&q=pinax&ud=any&ft=all&lang=en&sort=

https://www.slideshare.net/jtauber/how-to-contribute-to-pinax
https://www.slideshare.net/jtauber/state-of-pinax/19-reusable_appquisition_potterpredictions | State of Pinax
https://www.slideshare.net/jtauber/state-of-pinax/33-Sites_Using_Pinax | reusable app quisition potterpredictions

https://www.slideshare.net/pydanny/pinax-introduction
https://www.slideshare.net/pydanny/pinax-tutorial-090909
https://www.slideshare.net/pydanny/pinax-long-tutorial-slides | Pinax Long Tutorial Slides
http://pydanny.blogspot.com/2010/ | pydanny: 2010

https://2016.djangocon.us/schedule/presentation/45/ | Presentation: Building JSON APIs with Django / Pinax
https://speakerdeck.com/brosner/pinax | Building JSON APIs with Django / Pinax // Speaker Deck
https://github.com/pinax/pinax-api | pinax/pinax-api: RESTful API adhering to the JSON:API specification
http://eldarion.com/blog/2016/08/18/eldarions-brian-rosner-speaks-djangocon-us-2016/ | Eldarion's Brian Rosner Speaks At DjangoCon US 2016 — Eldarion Blog

https://groups.google.com/forum/#!forum/pinax-core-dev
https://groups.google.com/forum/#!topic/pinax-users/rtBvRdjd2ZI
https://groups.google.com/forum/#!topic/pinax-business/OOhLDYEYv9c

https://groups.google.com/forum/#!topic/pinax-users/rtBvRdjd2ZI | list of sites using pinax - Google Groups
Sites built with Pinax: https://github.com/pinax/pinax-theme-pinaxproject/blob/master/pinax_theme_pinaxproject/templates/example_sites/home.html
-->

Work in Progress- Symposium
* [Conference Starter Project GitHub](https://github.com/pinax/pinax-starter-projects/wiki/Conference-Starter-Project)
* [PyCon Israel GitHub](https://il.pycon.org/2018) and [PyCon Israel GitHub](https://github.com/eldarion/pycon-israel)

<!--
https://github.com/pinax/symposion/wiki/Apps-Phase-Grid
-->

Work in Progress- Contributors
* [Pinax Contributors Portal GitHub](https://github.com/pinax/pinax/wiki/Contributors-Portal)

Work in Progress- Documentation
* [Pinax Project Proposed Document Outline](https://github.com/pinax/pinax/wiki/Proposed-Docs-Outline)
* [Pinax Project FAQs](http://pinaxproject.com/pinax/faq)

Work in Progress- Improve Docs
* [Django User Accounts Read the Docs](http://django-user-accounts.readthedocs.io) and [Django User Accounts GitHub](https://github.com/pinax/django-user-accounts)
* [Pinax Stripe Read the Docs](https://pinax-stripe.readthedocs.io) and [Pinax Stripe GitHub](https://github.com/pinax/pinax-stripe)

Work in Progress- Pinax Releases
* ["Continuously Deploying Python Packages to PyPI with CircleCI"](https://circleci.com/blog/continuously-deploying-python-packages-to-pypi-with-circleci)
* [Glob](https://docs.python.org/3/library/glob.html#glob.glob)
* [Lincoln Loop: "Using setup.py in Your (Django) Project"](https://lincolnloop.com/blog/using-setuppy-your-django-project)
* [Graham: setup.py](https://github.com/pinax/pinax-starter-projects/pull/56/commits/262c712da313e4ba4ee743654ddad5752d4a0268)

Work in Progress- Pinax Demo Projects
* [Pinax Groupware Starter Project GitHub](https://github.com/pinax/pinax-starter-projects/wiki/Groupware-Starter-Project)
* [Cloudspotting 2 GitHub](https://github.com/pinax/cloudspotting2)
* [Patch Game](http://patchgame.pinaxproject.com) and [Patch Game GitHub](https://github.com/pinax/patch-game)

Work in Progress- Screencasts
* [Screencasts GitHub](https://github.com/pinax/screencasts)

<!--
https://www.youtube.com/watch?v=VlwfpzMVpRA | Cloudspotting Demo - YouTube
-->

Work in Progress- Decouple DUA
* [Django User Accounts Read the Docs](http://django-user-accounts.readthedocs.io) and [Django User Accounts GitHub](https://github.com/pinax/django-user-accounts)

<!--
Onboarding
https://github.com/pinax/pinax/blob/master/docs/how_to_contribute.md | pinax/how_to_contribute.md at master · pinax/pinax

Runtests
Link to explemplary demos (that use each app) in READMEs
Docs, documenting features
Update contributor files
Tools used by Eldarion

https://www.npmjs.com/package/pinax-images-panel
-->

Eldarion
* [Eldarion](http://eldarion.com) and [Eldarion GitHub](https://github.com/eldarion)
* [Clients](http://eldarion.com/what-we-do)
* [Eldarion Clients GitHub](https://github.com/eldarion-client)
* [Eldarion YouTube](https://www.youtube.com/channel/UCnop70xOY_4dAr4YB9jjlOg)
* [Eldarion LinkedIn](https://www.linkedin.com/company/eldarion)

<!--
https://github.com/orgs/eldarion/teams/developers | Developers · Eldarion, Inc. Discussion
-->

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

<!--
https://www.youtube.com/watch?v=q6-zh2ZT9HE | How Eldarion Cloud Boosts Productivity of Development Teams - YouTube
-->

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

Tags and Releases
* [GitHub About Releases](https://help.github.com/articles/about-releases) and [GitHub Creating Releases](https://help.github.com/articles/creating-releases)
* [GitHub Working with Tags](https://help.github.com/articles/working-with-tags)

<!--
https://developer.github.com/v3/repos/releases/#create-a-release | Releases | GitHub Developer Guide
-->

Release Blog Posts
* [Release of Pinax 16.07 Blog Post](http://blog.pinaxproject.com/2016/08/15/release-pinax-1607)
* [Pinax 16.04 Update Blog Post](http://blog.pinaxproject.com/2016/03/10/update-pinax-1604)
* [Pinax 16.04 Blog Post](http://blog.pinaxproject.com/2016/02/01/pinax-1604)

Past Release Plans
* [Pinax 18.01 Plan](https://github.com/pinax/pinax/wiki/Pinax-18.01)
* [Pinax 16.10 Plan](https://github.com/pinax/pinax/wiki/Pinax-16.10-Plan)
* [Pinax 16.07](https://github.com/pinax/pinax/wiki/Pinax-16.07)
* [Checklist for 16.04 candidate apps](https://github.com/pinax/pinax/issues/113)

Proposal for Pinax Distribution Versioning
* [Proposal for Pinax Distribution Versioning](https://github.com/pinax/pinax/issues/84)

Distribution
* [Pinax CLI GitHub](https://github.com/pinax/pinax-cli)

Distribution Scripts

<!--
Pinax Release Script
https://github.com/pinax/pinax/blob/master/check.py | pinax/check.py at master · pinax/pinax
https://github.com/pinax/pinax/blob/master/projects.json
https://github.com/pinax/pinax/blob/master/distributions.json | pinax/distributions.json at master · pinax/pinax

https://github.com/cndn/intelligent-code-completion/blob/edb80a083f481aa30897d5cb91c2bc53708b9ec5/raw_data/45600_check.py | intelligent-code-completion/45600_check.py at edb80a083f481aa30897d5cb91c2bc53708b9ec5 · cndn/intelligent-code-completion
-->

Static Build Process
* ["Simplifying the Static Build Process in Django Starter Projects" Blog Post](http://blog.pinaxproject.com/2017/09/08/simplifying-static-build-process-django-projects)

Pinax Templates and Semantic Markup
* [Pinax Templates Site](https://templates.pinaxproject.com)
* [Pinax Templates GitHub](https://github.com/pinax/pinax-templates)
* [Remarking pinax-theme-bootstrap To Be Semantic Blog Post](http://blog.pinaxproject.com/2017/09/18/remarking-pinax-theme-bootstrap-be-semantic)
* [Roadmap to Semantic Markup](https://github.com/pinax/pinax-theme-bootstrap/wiki/Roadmap-to-Semantic-Markup)

<!--
https://github.com/pinax/pinax-theme-bootstrap/pull/133/ | WIP: Convert to Semantic Markup by paltman · Pull Request #133 · pinax/pinax-theme-bootstrap

Stripe
https://www.reddit.com/r/django/comments/7do0uc/pinaxstripe_400_released_stripe_connect_support/ | pinax-stripe 4.0.0 Released - Stripe Connect support lands : django
https://github.com/pinax/pinax-stripe/milestone/11 | Rosie Milestone
-->

Django, Kubernetes, React
* [Django](https://www.djangoproject.com)
* [Kubernetes](https://kubernetes.io)
* [React](https://facebook.github.io/react)

<!--
http://fontawesome.io/ | Font Awesome, the iconic font and CSS toolkit
https://fontawesome.com | Font Awesome 5 | Font Awesome
-->

Webpack Versus Browserify
* [Webpack](https://webpack.js.org)
* [Copy Webpack Plugin GitHub](https://github.com/webpack-contrib/copy-webpack-plugin)
* [Browserify](http://browserify.org)

<!--
https://github.com/paltman/trying-webpack | paltman/trying-webpack
-->

CI
* [CircleCI](https://circleci.com)
* [Codecov](https://codecov.io)

Testing
* See Python and Django Notes

Testing- Blog Posts
* ["How We Maintain High Levels of Code Quality" Blog Post](http://eldarion.com/blog/2017/10/17/how-we-maintain-high-levels-code-quality)
* ["5 Reasons You Should Care about Code Coverage" Blog Post](http://eldarion.com/blog/2017/07/13/5-reasons-you-should-care-about-code-coverage)
* ["How to Test Against Multiple Python Versions in Parallel" Blog Post](http://blog.pinaxproject.com/2015/12/08/how-test-against-multiple-python-versions-parallel)

Blog Photos
* [Unsplash](https://unsplash.com)

Typical Eldarion Blog Post Subjects
* Eldarion Project Management
* Eldarion DevOps
* Eldarion services and product offerings, sales
* Case studies
* Eldarion donations to Pinax
* Project and app upgrades
* Project and app functionality tutorials and demos
* Cloudspotting
* React 
* Year in Review
* Conferences
* Eldarion accolades
* Sprints and other open-source initiatives
* New hires

Typical Pinax Blog Post Subjects
* About Pinax starter projects and apps
* Pinax starter project and app functionality tutorials and demos
* Cloudspotting
* Release announcements
* Release management
* Why and how to contribute to Pinax
* Documentation
* Why and how to use Slack
* Other helpful info for contributors
* Pinax developers
* My first pull request series
* Hangouts and Recaps
* Conferences

How to Contribute
* [How to Contribute](http://pinaxproject.com/pinax/how_to_contribute)
* [How to Contribute Google Doc](https://docs.google.com/document/d/1f9hPTw3nelWy7nxaDawWP7EUl4QyeGeC4BNYeb4iWhU/edit)

<!--
http://blog.pinaxproject.com/2016/03/15/writing-better-documentation-and-why-documentation

http://blog.pinaxproject.com/section/community/ | The Pinax Project Blog | The Pinax Project Blog

https://github.com/search?utf8=%E2%9C%93&q=org%3Apinax+label%3A%22up-for-grabs%22&type= | Search · org:pinax label:"up-for-grabs"
https://help.github.com/articles/searching-issues-and-pull-requests/ | Searching issues and pull requests - User Documentation
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

<!--
https://github.com/deep-philology/DeepVocabulary
https://github.com/deep-philology/DeepVocabulary/wiki/Overview
https://github.com/deep-philology/DeepReader | deep-reader/DeepReader: a highly modular, Vue.js-based framework designed for building online reading environments for deep reading of texts with rich annotations and integrated learning tools

https://sites.tufts.edu/perseusupdates/2018/03/19/its-alive-perseus-and-the-scaife-digital-library-viewer/
https://sites.tufts.edu/perseusupdates/2018/03/15/first-version-of-the-scaife-digital-library-viewer-goes-live-building-the-future-while-remembering-a-friend/
https://eldarion.com/blog/2018/02/06/countdown-perseus-50-scaife-launch/ | Countdown to the Perseus 5.0 “Scaife” Launch — Eldarion Blog
https://sites.tufts.edu/perseusupdates/2017/07/22/design-sprint-for-perseus-5-0open-greek-and-latin/ | Design Sprint for Perseus 5.0/Open Greek and Latin » Perseus Digital Library Updates

https://twitter.com/jtauber/status/951742629955371009 | James Tauber on Twitter: "If everyone who uses Perseus 4.0 moves over to Perseus 5.0, it may well be one of the largest (by user count) sites built with @vuejs. There… https://t.co/ENPwiSdRIq"

https://twitter.com/jtauber/status/910149159470149632 | James Tauber on Twitter: "Thrilled to announce that I'll be leading the development of the next version of @PerseusDigLib with the @eldarion team and others"
https://github.com/scaife-viewer
https://github.com/PerseusDL | PerseusDL
https://twitter.com/PerseusDigLib
https://sourceforge.net/p/epidoc/wiki/Home/ | EpiDoc: Epigraphic Documents in TEI XML / Home / Home
https://github.com/diyclassics/perseus-experiments/blob/master/Perseus%20Plaintext%20Poetry.ipynb | perseus-experiments/Perseus Plaintext Poetry.ipynb at master · diyclassics/perseus-experiments

http://capitains.org/ | CapiTainS
https://github.com/Capitains/MyCapytain | Capitains/MyCapytain: CTS And Textual Resources Utility Library for Python 3

https://github.com/ETCBC | Eep Talstra Centre for Bible and Computing
-->

Pinax Developer Profiles
* [Pinax Developer Profiles](https://docs.google.com/forms/d/1CdiEtvVyWLtdVZUXHLXoZI64K1qbslkOqSR0W5xz6_0/viewform)
