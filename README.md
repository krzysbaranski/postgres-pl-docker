# PostgreSQL with Polish Locale

This is a PostgreSQL Docker image with Polish locale (pl_PL.UTF-8) support and English messages.

## Docker Hub

The Docker image is automatically built and pushed to Docker Hub via GitHub Actions.

### Configuration Required

To enable automatic building and pushing to Docker Hub, configure the following secrets in your GitHub repository settings:

1. `DOCKER_USERNAME` - Your Docker Hub username
2. `DOCKER_PASSWORD` - Your Docker Hub password or access token (recommended)

### Workflow Triggers

The workflow is triggered on:
- Push to `main`, `master`, or `latest` branches
- Push of version tags (e.g., `v1.0.0`)
- Pull requests to `main`, `master`, or `latest` branches (build only, no push)
- Manual workflow dispatch

### Image Tags

The following tags are automatically generated:
- `latest` - Latest build from the default branch
- `<branch-name>` - Builds from specific branches
- `<version>` - Semantic version tags (e.g., `1.0.0`, `1.0`, `1`)

## Usage

```bash
docker pull krzysbaranski/postgres-pl-docker:latest
docker run -d krzysbaranski/postgres-pl-docker:latest
```

## Build Locally

```bash
docker build -t postgres-pl .
docker run -d postgres-pl
```
