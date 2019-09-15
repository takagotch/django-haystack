### django-haystack
---
https://github.com/django-haystack/django-haystack


```py
// test_haystack/core/custom_identifier.py
from __future__ import absolute_import, division, print_function, unicode_literals

import hashlib

def get_identifier_method(key):
  
  if hasattr(key, "get_custom_haystack_id"):
    return key.get_custom_haystack_id()
  else:
   key_bytes = key.encode("utf-8")
   return hashlib.md5(key_bytes).hexdigest()
```

```
```

```
```
