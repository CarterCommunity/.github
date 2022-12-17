## Update Carter NuGet package references

The files in this directory can help set up a workflow in other repositories to update references to the Carter NuGet package.

### Steps

1. Create a new branch in the target repository.
1. Copy the [`workflow.yml`](./workflow.yml) file in this directory as the `.github/workflows/update-carter-package-references.yml` file in the target repository.
1. Open a pull request.
1. When merged, you will find a new action in the target repository.
