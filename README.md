# Smart Checkout Action

This GitHub Action calculates and fetches the minimum commits for head and base branches to ensure the merge base commit is included. It supports both regular and LFS (Large File Storage) caching.

## Inputs

- `checkout-type` (required): The type of the checkout. Either "branch" or "sha". Defaults to `branch`.
- `base-branch` (required): The base branch name. Required if `checkout-type=branch`. Defaults to `main`.
- `head-branch` (required): The head branch name. Required if `checkout-type=branch`. Defaults to the current head reference.
- `commit` (optional): The commit SHA to checkout. Required if `checkout-type=commit`. Defaults to the current commit SHA.
- `main-branch` (optional): The main branch name. Required if `checkout-type=commit`. Defaults to `main`.
- `lfs` (required): Whether to use LFS caching. Defaults to `false`.
- `lfs-token` (optional): The GitHub token to use for LFS. Required if pushing in other steps. Defaults to the GitHub token.

## Outputs

This action does not produce any direct outputs.

## Example Usage

```yaml
- uses: pasqualesalza/smart-checkout-action@v1