## Update Carter NuGet package references

The files in this directory can help set up a workflow in other repositories to update references to the Carter NuGet package.

### Steps

1. Create a new branch in the target repository.
1. Copy the [`workflow.yml`](./workflow.yml) file in this directory to the `.github/workflows` directory in the target repository.
1. Open a pull request.
1. When merged, you will find a new action in the target repository.

### How it works

This process takes advantage of [reusable workflows in GitHub Actions](https://docs.github.com/en/actions/using-workflows/reusing-workflows), which avoids having to duplicate logic across several repositories.

The workflow defined in the `workflow.yml` file calls the workflow located in the [`.github/workflows/update-carter-nuget-package-references.yml`](../.github/workflows/update-carter-nuget-package-references.yml) file in this repository, which contains all the logic.
If in the future, we need to make adjustments to the logic, we'll only have to update a single file, instead of having to go through all the repositories where we might have copied that logic.
