# Canvas API

* Beta Environment:
https://unl.beta.instructure.com/

* Live API:
https://unl.instructure.com/doc/api/live

* `canvasapi` a Python API wrapper for Canvas:
https://github.com/ucfopen/canvasapi

```python
from canvasapi import Canvas

# user access token
token = 'your_token'
base_url = 'https://canvas.unl.edu'

canvas = Canvas(base_url, token)

user = canvas.get_current_user()
print(user)

for course in canvas.get_courses()
  print(course)
```

* Getting Started:
[community docs](https://community.canvaslms.com/docs/DOC-14390-canvas-apis-getting-started-the-practical-ins-and-outs-gotchas-tips-and-tricks#jive_content_id_Can_anyone_use_the_APIs)

* Canvas Developers:
https://community.canvaslms.com/groups/canvas-developers
