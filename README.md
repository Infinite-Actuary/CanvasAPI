# Canvas API

* Beta Environment:
https://unl.beta.instructure.com/

* Live API:
https://unl.instructure.com/doc/api/live

* `canvasapi` a Python API wrapper for Canvas:
https://github.com/ucfopen/canvasapi

### Example: List Courses

```python
from canvasapi import Canvas

# user access token
token = 'your_token'
base_url = 'https://canvas.unl.edu'

canvas = Canvas(base_url, token)

user = canvas.get_current_user()
print(user)

for course in canvas.get_courses():
  print(course)
```

### Example: Get Profiles

```python
from canvasapi import Canvas

# user access token
token = 'your_token'
base_url = 'https://canvas.unl.edu'

canvas = Canvas(base_url, token)

# https://canvas.unl.edu/courses/{course_id}
course_id = 'course_id'
course = canvas.get_course(course_id)
users = course.get_users(enrollment_type=['student'])

for user in users:
    profile = user.get_profile()
    name = profile.get('name')
    login_id = profile.get('login_id')
    print(f'name: {name} | id: {login_id}')
```

* Getting Started:
[community docs](https://community.canvaslms.com/docs/DOC-14390-canvas-apis-getting-started-the-practical-ins-and-outs-gotchas-tips-and-tricks#jive_content_id_Can_anyone_use_the_APIs)

* Canvas Developers:
https://community.canvaslms.com/groups/canvas-developers
