# npm-test


feature/1 -> develop -> release/*-M.m.p -> next -> main

To give your git-flow runner merge access to protected branches.
1. [create a PAT](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/creating-a-personal-access-token) and copy to your clipboard
2. [create a secret](https://docs.github.com/en/actions/reference/encrypted-secrets#creating-encrypted-secrets-for-a-repository) label it as `ADMIN_TOKEN` and paste the previously stored token

This allows the `git-flow.yml` to bypass the protection rules and merges into the branch(es). If there is a merge conflict, an MR is raised where you will have to fix the conflicts manually.
