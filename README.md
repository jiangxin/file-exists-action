[![file-exists-action](https://github.com/jiangxin/file-exists-action/actions/workflows/main.yml/badge.svg)](https://github.com/jiangxin/file-exists-action/actions/workflows/main.yml)

# File exists action

This action checks file existence in a branch using GitHub API without cloning the repository.

# Usage

```yaml
- uses: jiangxin/file-exists-action@v1
  with:
    # Repository name with owner. For example, jiangxin/file-exists-action.
    # Default: ${{ github.repository }}
    repository: ''

    # The branch, tag or SHA to search the file path in.
    # Default: the default branch.
    ref: ''

    # File path to find in the repository.
    # No default value, and must provide.
    path: ''

    # Expected type of file in the repository.
    # Default: "file"
    type: ''
 
    # Personal access token (PAT) used to fetch the repository.
    # [Learn more about creating and using encrypted secrets](https://help.github.com/en/actions/automating-your-workflow-with-github-actions/creating-and-using-encrypted-secrets)
    #
    # Default: ${{ github.token }}
    token: ''
```

# Scenarios

## Check file existence in default branch

```yaml
- uses: jiangxin/file-exists-action@v1
  with:
    path: 'path/of/file'
```

## Check file existence in a specific branch

```yaml
- uses: jiangxin/file-exists-action@v1
  with:
    path: 'path/of/file'
    ref: 'my-branch'
```

# License

The scripts and documentation in this project are released under the [MIT License](LICENSE)
