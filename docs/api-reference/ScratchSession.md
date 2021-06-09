# ScratchSession
The base class for the module:

```python
from scratchclient import ScratchSession

session = ScratchSession("aVeryRandomUsername", "OwO")
```

## Properties

### username
The username of the logged in user.

```python
print(session.username) # aVeryRandomUsername
```

### session_id
The session id of the logged in user. This is the `scratchsessionsid` entry found in your cookie.

```python
print(session.session_id)
```
### csrf_token
The csrf token of the logged in user. This is the `scratchcsrftoken` entry found in your cookie.

```python
print(session.csrf_token) # a random string
```

### token
The xToken of the logged in user.

```python
print(session.token)
```
### user
The [User](user) object of the currently logged in user

## Methods

### get_user(username)
Gets the [User](user) object of the given username.

```python
print(session.get_user("griffpatch").scratchteam) # false
```

### get_project(id)
Gets the [Project](project) object of the given project id.

```python
print(session.get_project(60917032).title) # Appel v1.4
```

### get_studio(id)
Gets the [Studio](studio) object of the given studio id.

```python
print(session.get_studio(26135902).owner) # Za-Chary
```

### get_news()
Gets Scratch's [news](https://scratch.mit.edu/discuss/5/) and translates them into an array of [News](news) objects.

```python
print(session.get_news()[0].title)
```

### get_messages(all=false, limit=20, offset=0)
Gets the messages of the logged in user as an array of [Message](message) objects. If the all parameter is specified as True, all the messages are fetched. Otherwise, they are fetched with a limit of limit messages and and offset of offset.

### create_cloud_connection(id)
Creates a cloud connection for the specified project ID. Returns a [CloudConnection](cloudconnection) object.

```python
connection = session.create_cloud_connection(104)

print(connection.get_cloud_variable('foo'))
```

### explore_projects(mode="trending", query)
Explores Scratch projects with the specified `mode` and `query`. Returns an array of [Project](project) objects.
```python
print(session.explore_projects()[0].title)
```

### explore_studios(mode="trending", query)
Explores Scratch studios with the specified `mode` and `query`. Returns an array of [Studio](studio) objects.

### search_projects(mode="popular", query)
Searches Scratch projects with the specified `mode` and `query`. Returns an array of [Project](project) objects.

### search_studios(mode="popular", query)
Searches Scratch studios with the specified `mode` and `query`. Returns an array of [Studio](studio) objects.
