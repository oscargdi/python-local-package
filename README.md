# Python project with common library

This project demonstrate how to configure a project to import local libraries without having to make them live in the same environment.

## Structure

- `py-common`: contains code that is considered as common across the mulitple projects.
- `service`: constains a demo project that makes use of the `py-common` library.

## How to develop

### py-common

This can be mantained as regular project since it is independent from other projects.

### service

This requires the `py-common` library for development. For convenience, installation process has been simplified with a make target:

```bash
make dev
```

This install `py-common` library in editable mode so that any change in `py-common` is reflected in `service` project instantly.

## Benefits

- `service` and `py-common` projects can evolve separately.
- No complex imports in `service` code.
