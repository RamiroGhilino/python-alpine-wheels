# python-alpine-wheels

This repository works as a wheel database/cache for precompiled Python packages built for Alpine Linux.

The goal is to avoid compiling dependencies from source every time we build Alpine-based Docker images. Instead of rebuilding native modules in each pipeline run, our images can install ready-made `.whl` files from here, which:

- reduces build time
- reduces CI resource usage
- makes builds more predictable and reproducible

In short: this repo stores precompiled wheels so Alpine Docker builds are faster and more stable.
