# actions-deploy

Action generates Hugo site, then deploys to GitHub Pages.

## Scope

Intended for Anthrocon internal use, however may be useful elsewhere.

## Usage

Create a workflow in `.github/workflows` with:

```yaml
name: Deploy Hugo site

on:
  push:
    branches:
      - main

jobs:
  call:
    permissions:
      contents: read
      id-token: write
      pages: write
    uses: Anthrocon/actions-deploy/.github/workflows/deploy.yaml@main
    secrets: inherit
```

## Licence

No licence implied. All rights reserved copyright Anthrocon, Inc., 2022.
