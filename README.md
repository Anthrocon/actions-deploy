# actions-deploy

Action generates Hugo site, then deploys to GitHub Pages.

## Scope

Intended for Anthrocon internal use, however may be useful elsewhere.

## Usage

Create a workflow in `.github/workflows` with:

```yaml
name: Deploy

on:
  push:
    branches:
      - main

jobs:
  call:
    name: Call
    runs-on: ubuntu-latest
    steps:
      - name: Build and deploy
        uses: Anthrocon/actions-deploy/.github/workflows/deploy.yaml
```

## Licence

No licence implied. All rights reserved copyright Anthrocon, Inc., 2022.
