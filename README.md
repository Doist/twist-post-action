# GitHub Action - Twist Post
GitHub action that posts a message to Twist thread through a thread integration.

## Example

```yml
on:
  push:
    branches: [ dev ]

jobs:
  notify:
    runs-on: ubuntu-latest
    steps:
      uses: Doist/twist-post-action@master
      with:
        message: "Dev branch has been updated"
        install_id: ${{ secrets.TWIST_INTEGRATION_INSTALL_ID }}
        install_token: ${{ secrets.TWIST_INTEGRATION_INSTALL_TOKEN }}
```
