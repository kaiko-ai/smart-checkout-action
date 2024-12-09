# Smart Checkout Action

This GitHub Action calculates and fetches the minimum commits for head and base branches to ensure the merge base commit is included. It supports both regular and LFS (Large File Storage) caching.

## Inputs

- `base-branch` (required): The base branch name.
- `head-branch` (required): The head branch name. Defaults to the current head reference.
- `lfs` (required): Whether to use LFS caching. Defaults to `false`.

## Outputs

This action does not produce any direct outputs.

## Example Usage

```yaml
- uses: pasqualesalza/smart-checkout-action@v1
  with:
    base-branch: 'main'
    head-branch: 'feature-branch'
    lfs: false
```
