# Pinax- Porting from Python 2 to 3


## Essential syntax differences

### print

### Raising exceptions

### Catching exceptions

### Division

### Long integers

### Octal constants

### Backtick repre

### Metaclasses


## Strings and bytes

### Unicode (text) string literals

### Byte-string literals

### basestring

### unicode

### StringIO

https://github.com/pinax/django-user-accounts/blob/master/account/tests/test_commands.py
https://github.com/pinax/symposion/blob/master/symposion/sponsorship/views.py
https://github.com/pinax/symposion/blob/master/symposion/sponsorship/tests.py


## Imports relative to package

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

### Custom __str__ methods

### Custom __nonzero__ vs __bool__ method:


## Lists versus iterators

### xrange :checkmark:

None

### range

### map

### imap

### zip, izip

### filter, ifilter


## Other builtins

### File IO with open()

### reduce()

### raw_input()

### input()

### file()

### exec

### execfile()

### unichr()

### intern()

### apply()

### chr()

### cmp()

### reload()


## Standard library

### dbm modules

### commands / subprocess modules

### subprocess.check_output()

### collections: Counter and OrderedDict

### StringIO module

### http module

### xmlrpc module

### html escaping and entities

### html parsing

### urllib module

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
