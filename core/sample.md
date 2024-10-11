## Sample Github Actions Yaml

```yaml
# create this is .github/workflow directory of your project

name: Sample Workflow

on: [push]

jobs:
  sample_job:
    runs-on: ubuntu-latest
    steps:
    - name: Welcome Message
      run: echo "Welcome Folks"
```

Description of the `sample.yaml`:
- `on`: defines when to run the CI (e.g. on push, on commit, etc).
- `jobs`: what are the jobs to run sequentially.