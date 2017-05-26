# Nflex Connector Utils

This python package provides a suite of tools to produce data structures when implementing resources connector nflex modules.

# Installation
```sh
pip install nflex-connector-utils
```

# Example

This example returns two servers.
```python
from nflex_connector_utils import Server, serialize_list


def get(event, context):
    return serialize_list([
        Server(id='server-1', name='Server 1'),
        Server(id='server-2', name='Server 2'),
    ])
```

# Development
A Makefile has been included to do most common development things.
```sh
make clean
make setup
make doc
make test
make package
```

# Package Release procedure
Versioneer is used for releasing the package. To release one, just create a tag and run:
```sh
git push origin
git tag vx.y.z
git push origin vx.y.z
make upload
```
