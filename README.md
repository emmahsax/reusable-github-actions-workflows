# GitHub Actions

A place for me to store GitHub Actions reusable workflows and composite steps for use in personal repos.

To call one of these reusable workflows, create a `.github/workflows/WORKFLOW_NAME.yml` file and put this in it (example):

```yaml
name: Workflow Name

on:
  pull_request:
  workflow_dispatch:

jobs:
  workflow-name:
    uses: emmahsax/github-actions/.github/workflows/workflow-name.yml@main
    with:
      arg_1: arg 1
      arg_2: arg 2
    secrets:
      private_arg: ${{ secrets.private_arg }}
```

To call a composite step, add the following in the `steps` section of the workflow:

```yaml
- name: Step Name
  uses: emmahsax/github-actions/step-name@main
  with:
    arg_1: arg 1
    arg_2: arg 2
```

---

### Contributing

To submit a feature request, bug ticket, etc, please submit an official [GitHub issue](https://github.com/emmahsax/github-actions/issues/new). To copy or make changes, please [fork this repository](https://github.com/emmahsax/github-actions/fork). When/if you'd like to contribute back to this upstream, please create a pull request on this repository.

Please follow included Issue Template(s) and Pull Request Template(s) when creating issues or pull requests.

### Security Policy

To report any security vulnerabilities, please view this repository's [Security Policy](https://github.com/emmahsax/github-actions/security/policy).

### Licensing

For information on licensing, please see [LICENSE.md](https://github.com/emmahsax/github-actions/blob/main/LICENSE.md).

### Code of Conduct

When interacting with this repository, please follow [Contributor Covenant's Code of Conduct](https://contributor-covenant.org).
