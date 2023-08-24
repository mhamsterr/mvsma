# mvsma

mvsma, aka mhamster's very simple modrinth api (wrapper), is a super simple modrinth api wrapper for python.

It provides plain and simple access to [modrinth's api](https://api.modrinth.com) endpoints and returns their plain responses. Very easy to use!

For information about api models see [modrinth api documentation](https://docs.modrinth.com/api-spec/#tag/project_model).

# Examples

Search for a projects:
```py
from mvsma import Modrinth

m = Modrinth()
# Search for mod called 'cesium' and print first result
m.ua = 'Package example from https://github.com/mhamsterr/mvsma' # Edit User-Agent of request so everyone will know who we are and what we are doing

response = m.search(query="cesium")
print(response["hits"][0])

```

Get versions of a project:
```py
from mvsma import Modrinth

m = Modrinth()
# Get versions of mod with slug "supercoolmod"
m.ua = 'Package example from https://github.com/mhamsterr/mvsma' # Edit User-Agent of request so everyone will know who we are and what we are doing

response = m.project_versions(slug="supercoolmod")
print(response)

```

Get list of random projects
```py
from mvsma import Modrinth

m = Modrinth()
# Get list of random projects
m.ua = 'Package example from https://github.com/mhamsterr/mvsma' # Edit User-Agent of request so everyone will know who we are and what we are doing

response = m.random_projects(count=11)
print(response)
```

# Documentation:
TODO

# Installation
```
pip install mvsma
```

# License:
MIT License, find more in 'LICENSE' file