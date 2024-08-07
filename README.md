# actions-deploy

[![Deploy Hugo site](https://github.com/Anthrocon/actions-deploy/actions/workflows/test.yaml/badge.svg)](https://github.com/Anthrocon/actions-deploy/actions/workflows/test.yaml)

Action generates a Hugo site from `main` branch, then deploys it to GitHub Pages.

## Scope

Intended for Anthrocon internal use, however may be useful elsewhere.

## Usage

Create a workflow in `.github/workflows` with:

```yaml
on:
  push:

jobs:
  call:
    uses: Anthrocon/actions-deploy/.github/workflows/deploy.yaml@main
```

### Specify Hugo version

Recommended. Overrides action default, and prevents unexpected changes.

```yaml
uses: Anthrocon/actions-deploy/.github/workflows/deploy.yaml@main
with:
  hugo-version: '0.131.0'
```

### Disable cache

By default, action caches Hugo package, build cache, and resources. Cache can be disabled for testing.

```yaml
uses: Anthrocon/actions-deploy/.github/workflows/deploy.yaml@main
with:
  cache: false
```

## License

No license implied. All rights reserved copyright Anthrocon, Inc., 2023.
