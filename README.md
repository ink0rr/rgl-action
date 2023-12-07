# rgl-action

GitHub Action for rgl.

## Usage

### Pre-requisites

Create a workflow `.yml` file in your `.github/workflows` directory.

### Inputs

| Input          | Description                         | Default   |
| -------------- | ----------------------------------- | --------- |
| `version`      | rgl version to use                  | `latest`  |
| `profile`      | Profile to run                      | `default` |
| `github_token` | GitHub token to get private filters | None      |

### Example workflow

```yml
name: Example workflow
on: push
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: ink0rr/rgl-action@v1
        with:
          profile: build
```
