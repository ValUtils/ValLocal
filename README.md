# ValLocal

![GitHub](https://img.shields.io/github/license/ValUtils/ValLib)

A Python module for interacting with the RiotClient local api.

## Features

- Automated lockfile grabbing
- Request method

## Installation

The preferred method of installation is through `pip` but if you know better use the package manager that you want.

```sh
pip install git+https://github.com/ValUtils/ValLocal.git
```

## Reference

### Basic structure

ValLib contains this basic building blocks:

- `LockFile` a dataclass containing the lockfile data

And the following methods:

- `get_lockfile` to get the lockfile as a `LockFile` instance
- `local_api` to make requests to the RiotClient, using `LockFile`

### Ussage

```python
import ValLocal

lock = ValLocal.get_lockfile()
api_help = ValLocal.local_api(lock, "GET", "/help").text
print(api_help)
```

## Roadmap

- [ ] Async
- [ ] WebSockets
- [ ] Better documentation

## Acknowledgements

- Thanks to [Techdoodle](https://github.com/techchrism) for his API docs
- Thanks to the Valorant App Developers discord
