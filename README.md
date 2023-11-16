# Pull Request Requester

This repository contains a simple example of how to ensure that PRs are created
and merged based on the following rules:

- Feature branches can have any name
- Release branches start with `release-*`
- The default branch is `main`
- Feature branches are merged into release branches via PRs

Once a PR is merged into a release branch, the release branch must be merged
into `main`. This example action will do the following:

- Check if there is an existing PR from a release branch into `main`
- If not, create a new PR to merge a release branch into `main`

Check it out [here](.github/workflows/pull-request-requester.yml)!

## Permissions

In order to use this workflow, you must ensure that the **Allow GitHub Actions
to create and approve pull requests** option is enabled for your repository!
