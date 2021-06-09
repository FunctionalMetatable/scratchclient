---
title: Getting Started
---
# Getting Started
To use scratchclient, you need to use Python (of course) and pip.
```bash
# install scratchclient
pip install scratchclient
```

## Basic Usage
```python
from scratchclient import ScratchSession # import the module

session = ScratchSession("ceebee", "--uwu--") # creates a session

# post comments
session.get_user("Paddle2See").post_comment("OwO")

# lots of other stuff
print(session.get_project(450216269).get_comments()[0].content) # first comment in project 450216269
print(session.get_studio(29251822).description) # description of studio 29251822
```

## Interfacing with cloud variables
```python
from scratchclient import ScratchSession

session = ScratchSession("griffpatch", "SecurePassword7")

connection = session.create_cloud_connection(450216269)

connection.set_cloud_variable("variable name", 5000) #

@connection.on("set")
def on_set(variable):
    print(variable.name, variable.value)

print(connection.get_cloud_variable("other variable"))
```
