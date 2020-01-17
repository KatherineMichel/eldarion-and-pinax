# Pinax- Porting from Python 2 to 3

f-strings
type checking
from __future__ import
https://docs.djangoproject.com/en/2.2/_modules/django/utils/six/
https://stackoverflow.com/questions/59193514/importerror-cannot-import-name-six-from-django-utils
https://docs.djangoproject.com/en/3.0/releases/3.0/#removed-private-python-2-compatibility-apis

https://docs.djangoproject.com/en/3.0/releases/2.0/
While Python 2 support was removed in Django 2.0, some private APIs weren’t removed from Django so that third party apps could continue using them until the Python 2 end-of-life.

Since we expect apps to drop Python 2 compatibility when adding support for Django 3.0, we’re removing these APIs at this time.

django.utils.six - Remove usage of this vendored library or switch to six.
Many

from django.utils.decorators import available_attrs
https://github.com/pinax/pinax-teams/blob/master/pinax/teams/decorators.py
https://github.com/pinax/django-user-accounts/blob/master/account/decorators.py

from django.utils.encoding import python_2_unicode_compatible
Many

from django.utils.functional import curry
Several

https://github.com/pinax/symposion/commit/a95825ede8d4039cb406c7a7acd2d94abde1f29a

## Essential syntax differences

### print

Possibly many

### Raising exceptions

Not sure

### Catching exceptions

Not sure

### Division

Not sure

### Long integers

Not sure

### Octal constants

Not sure

### Backtick repre

Not sure

### Metaclasses

Not sure


## Strings and bytes

### Unicode (text) string literals

Not sure

### Byte-string literals

Not sure

### basestring :checkmark:

None

### unicode

Not sure

### StringIO

https://github.com/pinax/django-user-accounts/blob/master/account/tests/test_commands.py
https://github.com/pinax/symposion/blob/master/symposion/sponsorship/views.py
https://github.com/pinax/symposion/blob/master/symposion/sponsorship/tests.py


## Imports relative to package

Not sure


## Dictionaries

### Iterating through dict keys/values/items :checkmark:

Iterable dict keys: iterkeys()
None

Iterable dict values: itervalues()
None

Iterable dict items: iteritems()
https://github.com/pinax/pinaxproject.com/blob/master/pinaxsite_project/apps/packages/views.py

### dict keys/values/items as a list :checklist:

dict keys as a list: keys()
Many!

dict values as a list: values()
Many!

dict items as a list: 
Many, probably


## Custom class behaviour

### Custom iterators

Not sure

### Custom __str__ methods

Not sure... possibly  many

### Custom __nonzero__ vs __bool__ method :checkmark:

https://github.com/pinax/pinax-points/commit/d5b90fd90a6a5a90a848c7699132781d289c364f


## Lists versus iterators

### xrange :checkmark:

None

### range

Not sure

### map

Not sure

### imap :checkmark:

None

### zip, izip

zip
Not sure

izip
None

### filter, ifilter

filter
Not sure

ifilter
None


## Other builtins

### File IO with open()

Not sure

### reduce() :checkmark:

https://github.com/pinax/django-user-accounts/blob/master/account/models.py

### raw_input() :checkmark:

None

### input() :checkmark:

I don't think so

### file()

Possibly a number of them

### exec :checkmark:

None

Don't think so
https://github.com/pinax/pinax-api/blob/master/docs/utilities.md

### execfile() :checkmark:

https://github.com/pinax/symposion/blob/master/docs/conf.py
https://github.com/pinax/django-waitinglist/blob/master/docs/conf.py

### unichr() :checkmark:

None

### intern() :checkmark:

None

### apply()

Not sure- look again

### chr() :checkmark:

None

### cmp() :checkmark:

https://github.com/pinax/pinax/blob/master/check.py

### reload() :checkmark:

I don't think so


## Standard library

### dbm modules :checkmark:

I don't think so

### commands / subprocess modules :checkmark:

None

### subprocess.check_output() :checkmark:

None

### collections: Counter and OrderedDict :checkmark:

from collections import OrderedDict
https://github.com/pinax/django-user-accounts/blob/master/account/forms.py

### StringIO module :checkmark:

https://github.com/pinax/django-user-accounts/blob/master/account/tests/test_commands.py
https://github.com/pinax/symposion/blob/master/symposion/sponsorship/views.py
https://github.com/pinax/symposion/blob/master/symposion/sponsorship/tests.py

### http module :checkmark:

None

### xmlrpc module :checkmark:

None

### html escaping and entities :checkmark:

from html import escape
Not sure

htmlentitydefs
None

### html parsing :checkmark:

HTMLParser
https://github.com/pinax/symposion/blob/master/symposion/markdown_parser.py

### urllib module :checkmark:

urlparse
https://github.com/pinax/django-user-accounts/blob/master/account/utils.py
https://github.com/pinax/django-user-accounts/blob/master/account/middleware.py
https://github.com/pinax/django-user-accounts/blob/master/account/tests/test_views.py
https://github.com/pinax/pinax-api/blob/master/pinax/api/jsonapi.py
https://github.com/pinax/pinaxproject.com/blob/master/pinaxsite_project/apps/downloads/utils.py
https://github.com/pinax/atom-format/blob/master/atomformat.py

urlencode- check these
https://github.com/pinax/django-user-accounts/blob/master/account/templatetags/account_tags.py
https://github.com/pinax/django-user-accounts/blob/master/account/models.py
https://github.com/pinax/django-user-accounts/blob/master/account/middleware.py
https://github.com/pinax/pinax-api/blob/master/pinax/api/jsonapi.py
https://github.com/pinax/code.pinaxproject.com/blob/master/cpc_project/apps/tasks/views.py
https://github.com/pinax/django-user-accounts/blob/master/account/utils.py

urllib2
https://github.com/pinax/pinaxproject.com/blob/master/pinaxsite_project/apps/downloads/utils.py

### Tkinter :checkmark:

I don't think so

### socketserver :checkmark:

None

### copy_reg, copyreg :checkmark:

None

### configparser :checkmark:

None

### queue :checkmark:

I don't think so

### repr, reprlib :checkmark:

repr- look through these; some don't qualify
https://github.com/pinax/pinax-stripe/blob/master/pinax/stripe/tests/test_models.py
https://github.com/pinax/pinax-stripe/blob/master/pinax/stripe/models.py
https://github.com/pinax/django-mailer/blob/master/src/mailer/models.py
https://github.com/pinax/django-mailer/blob/master/src/mailer/__init__.py
https://github.com/pinax/django-mailer/blob/master/tests/__init__.py
https://github.com/pinax/pinaxproject.com/blob/master/pinaxsite_project/apps/downloads/verlib.py
https://github.com/pinax/code.pinaxproject.com/blob/master/cpc_project/migrations/001_initial.sql

reprlib
None

### UserDict, UserList, UserString :checkmark:

UserDict
None

UserList
None

UserString
None

### itertools: filterfalse, zip_longest :checkmark:

izip_longest
https://github.com/pinax/pinax-documents/blob/master/pinax/documents/compat.py
https://github.com/pinax/pinax-documents/blob/master/pinax/documents/models.py
https://github.com/pinax/symposion/blob/master/symposion/schedule/timetable.py
https://github.com/pinax/symposion/blob/master/symposion/sponsorship/views.py

zip_longest
https://github.com/pinax/pinax-documents/blob/master/pinax/documents/compat.py
