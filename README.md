# Generate GitHub App Token Action

This Github Action generates a Github App Token for a given Github App ID, Github App Private Key, and Github Repository.

## Inputs

### `app_id`

**Required** The ID of the Github App.

### `app_private_key`

**Required** The private key of the Github App.

### `github_repo`

**Optional** The full name of the Github repository (e.g. `owner/repo`). If not provided, the repository name is obtained from the Github Actions context.

## Outputs

### `token`

The generated Github App Token.

### `unscoped_token`

The generated Github App Unscoped Token.

## Example usage

```yaml
 - name: Generate Github App Token
  uses: khajavi/generate-github-app-token@v0.1
  with:
    app_id: ${{ secrets.APP_ID }}
    app_private_key: ${{ secrets.APP_PRIVATE_KEY }}
    github_repo: ${{ github.repository }} // optional
```
