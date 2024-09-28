# Chapter 1: Coding Style

- The ordering of import should be following
  1. Standard library import
  1. Related third party import
  1. Local application or library specific import

```py
# Stdlib imports
from math import sqrt
from os.path import abspath


# Core Django imports
from django.db import models
from django.utils.translation import ugettext_lazy as _


# Third-party app imports
from django_extensions.db.models import TimeStampedModel


# Imports from your apps
from splits.models import BananaSplit
```

- Avoid Using Import \*

```py
# ANTI-PATTERN: Don't do this!
from django.forms import *
from django.db.models import *
```

The reason for this is to avoid implicitly loading all of another Python module’s locals into and over
our current module’s namespace, this can produce unpredictable and sometimes catastrophic results.

Do this

```py
from django import forms
from django.db import models
```

- Other Python Naming Collisions

```py
# ANTI-PATTERN: Don't do this!
from django.db.models import CharField
from django.forms import CharField
```

Use alias

```py
from django.db.models import CharField as ModelCharField
from django.forms import CharField as FormCharField
```
