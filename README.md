# valheim-server-docker-shim

This repository exists to keep publishing the legacy container image at `ghcr.io/lloesche/valheim-server`.

The actual source code lives in `community-valheim-tools/valheim-server-docker`:

- Repository: `https://github.com/community-valheim-tools/valheim-server-docker`
- Image: `ghcr.io/community-valheim-tools/valheim-server`

## Why This Exists

GitHub Container Registry permissions are tied to repository access in a way that makes publishing the legacy image path awkward from the upstream repository. This shim repository is the workaround:

- GitHub Actions in this repo check out the upstream repository
- The upstream code is built and tested here
- The resulting image is pushed to the legacy GHCR location

## What Belongs Here

This repository is intentionally minimal.

It should only contain:

- Workflow and publishing configuration
- Small documentation like this file
- Other shim-specific automation if needed

Application source changes should be made in `community-valheim-tools/valheim-server-docker`, not here.
