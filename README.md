# Smart Checkout Action

This GitHub Action calculates and fetches the minimum commits for head and base branches to ensure the merge base commit is included. It supports both regular and LFS (Large File Storage) caching.

## Inputs

- `base-branch` (required): The base branch name.
- `head-branch` (required): The head branch name. Defaults to the current head reference.
- `head-only` (required): Whether to only checkout the head branch. Defaults to `false`.
- `head-only-fetch-depth` (optional): The fetch depth for the head branch when only checking out the head branch. Defaults to `1`.
- `lfs` (required): Whether to use LFS caching. Defaults to `false`.
- `lfs-token` (optional): The GitHub token to use for LFS. Required if pushing in other steps. Defaults to the GitHub token.

## Outputs

This action does not produce any direct outputs.

## Example Usage

```yaml
- uses: pasqualesalza/smart-checkout-action@v1
```
