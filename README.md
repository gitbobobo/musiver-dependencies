# Musiver public dependencies

This repository publishes the public native archives used by [Musiver](https://github.com/gitbobobo/musiver). The main repository downloads release assets by immutable tag and verifies SHA-256 before installation.

The repository contains build recipes, source revisions, configure flags, license files, and release metadata. Large binaries are stored only as GitHub Release assets. They are never committed to git history.

## Release rules

- A release may be created only from a protected `v*` tag or a maintainer-triggered workflow dispatch.
- The workflow dispatch accepts a public, already verified archive URL and SHA-256, downloads it on GitHub-hosted infrastructure, verifies it, and uploads it to the immutable release.
- Every asset needs a source commit, toolchain version, build log, license directory, and SHA-256 entry in `recipes/`.
- No workflow uses private registries, long-lived credentials, or unpublished artifacts.
- An asset is immutable after publication. Publish a new release when the build changes.
