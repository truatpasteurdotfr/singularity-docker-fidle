# building container for fidle (https://gricad-gitlab.univ-grenoble-alpes.fr/talks/fidle)

Tru <tru@pasteur.fr>

## Why ?
- toy system for github actions
- build docker image from dockerhub registry and push to ghcr.io with proper tags
- build singularity container from dockerhub registry and push to oras://ghcr.io with proper tags 
- build docker image, push to ghcr.io and re-use that docker image to create a singularity container pushed ghcr.io oras://
- 
## Caveat
- playground, use at your own risk!
- `:main` tagged docker image
- `:latest` tagged singularity image
- Only cover the software installation for cpu (https://gricad-gitlab.univ-grenoble-alpes.fr/talks/fidle/-/wikis/Using%20Fidle/Linux%20installation%20using%20conda)

## Usage
- Docker [![Docker build](https://github.com/truatpasteurdotfr/singularity-docker-fidle/actions/workflows/docker-publish.yml/badge.svg)](https://github.com/truatpasteurdotfr/singularity-docker-fidle/actions/workflows/docker-publish.yml)
```
docker pull ghcr.io/truatpasteurdotfr/singularity-docker-fidle:main
```

- Singularity [![Singularity build](https://github.com/truatpasteurdotfr/singularity-docker-fidle/actions/workflows/singularity-publish.yml/badge.svg)](https://github.com/truatpasteurdotfr/singularity-docker-fidle/actions/workflows/singularity-publish.yml)
```
singularity run oras://ghcr.io/truatpasteurdotfr/singularity-docker-fidle:latest
```
