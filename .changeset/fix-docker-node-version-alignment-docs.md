---
'@backstage/create-app': patch
---

Added a comment to the example backend Dockerfiles clarifying that the host build steps (`yarn install`, `yarn build:backend`) must use the same Node version as the Docker base image (Node 24). Using a mismatched version — especially combined with a shared BuildKit Yarn cache — can cause native modules to fail silently at runtime.
