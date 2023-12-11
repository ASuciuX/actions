# Update cache action

Logs the mutants to cache, appending to the old output, and saving an artifact for easier data access and backup.

## Documentation

### Inputs

| Input | Description | Required | Default |
| ------------------------------- | ----------------------------------------------------- | ------------------------- | ------------------------- |
| `gh-token` | The github token from the main workflow for cache deletion | true | `""` |

## Usage

```yaml
name: Action
on: push
jobs:
  build:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Update Cache
        id: update-cache
        uses: stacks-network/actions/mutation-testing/update-cache@main
        with:
          gh-token: ${{ secrets.GITHUB_TOKEN }}
```
