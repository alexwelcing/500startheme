# 500 Stars is a Ghost theme

Built to share great experiences, this flexible theme can be adapted for by anyone to highlight their content and empower readers to explore.

## Features

Using the Ghost API, we have created custom pages and components to create a flexible user experience.

1. Tag Page with adaptable 'Featured', 'Recommended', and 'New' Post blocks
2. Membership Page explaining accounts and pricing

The documentation includes steps for creating a GitHub Action to connect your theme repository to the production site.

[Ghost GitHub Actions](https://ghost.org/integrations/github/)

```yml
name: Deploy 500Star Theme
on:
  push:
    branches:
      - main
jobs:
  deploy:
    runs-on: ubuntu-18.04
    steps:
      - uses: actions/checkout@main
      - uses: TryGhost/action-deploy-theme@v1.4.1
        with:
          api-url: ${{ secrets.GHOST_ADMIN_API_URL }}
          api-key: ${{ secrets.GHOST_ADMIN_API_KEY }}
```
