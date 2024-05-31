# Check Broken Symlinks
This GitHub Action checks for broken symlinks within a Git repository. If any broken symlinks are found, it prints an error message and exits with a non-zero status; otherwise, it prints a success message and exits normally.

## Usage
Include the action in your workflow.

```yaml
- uses: feather-actions/check-broken-symlinks@0.0.1
```
Full example:

```yaml
on: [push]

jobs:
  check-broken-symlinks:
    runs-on: macos-latest

    steps:
      - name: Checkout
        uses: actions/checkout@v4
        with:
          fetch-depth: 1
  
      - name: Check Broken Symlinks
        uses: feather-actions/check-broken-symlinks@0.0.1
```
