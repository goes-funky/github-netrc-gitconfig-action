# github-netrc-gitconfig-action
Sets up a `.netrc` and `.gitconfig` files, which force GitHub SSH URLs into
HTTPS URLs, with authentication set to a Personal Access Token.

## Usage
```yaml
name: Build

jobs:
  build:
    runs-on: ubuntu-latest
    name: Build

    steps:
      # ...

      - name: Setup .gitconfig and netrc
        uses: goes-funky/github-netrc-gitconfig-action@v1
        with:
          github-token: "${{ secrets.GH_REPO_READ_TOKEN }}"

      # happy cloning!
```

