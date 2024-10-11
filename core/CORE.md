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

## Core Components
The YAML file consists of 3 core components:
1. `Workflow`: It is an automated process capable executing one or more jobs. It is used in SLDC for building and pushing images, applications, etc.
2. `Jobs`: They are the building blocks of Workflows. They run sequentially.
3. `Steps`: As the name suggest, they define the steps to run a job. usually consists of `actions`, `run` and `name`

#### What are Actions?
They are reusable predefined components for specific task, they facilitate automation, integration with third party tools, etc. Example: build and push docker images, creating AKS clusters, etc.

Using Actions:
```yaml
name: Sample Workflow

on: [push]

jobs:
  sample_job:
    runs-on: ubuntu-latest
    steps:
    - name: Welcome Message
      run: echo "Welcome Folks"
	
	- name: Checkout Repository
	  uses: actions/checkout@v4

	- name: List Files
	  run: ls

	- name: Read README.md
	  run: cat README.md
```
