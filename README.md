## OpenMemory images

Pre-built Docker images for the OpenMemory subproject from mem0ai/mem0, published to GHCR.

- API: ghcr.io/benrski/openmemory-api
- UI: ghcr.io/benrski/openmemory-ui

## How it works

- This repo contains a minimal GitHub Actions workflow that runs on every tag push.
- The workflow builds from mem0ai/mem0 at the same tag and publishes images tagged with that tag.

## Trigger a build

1. Create and push a tag in this repo that matches an upstream tag, for example: v0.1.116.

## Pull images

```bash
docker pull ghcr.io/benrski/openmemory-api:latest
docker pull ghcr.io/benrski/openmemory-ui:latest
```

## Notes

- Images are built from the upstream Dockerfiles at openmemory/api and openmemory/ui.
- If the upstream layout changes, update the build contexts in .github/workflows/build.yml.

Upstream: https://github.com/mem0ai/mem0
