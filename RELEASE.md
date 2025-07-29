# Release Process

This document explains how to create a new release for Dumproid.

## Automated Releases

This project uses GitHub Actions and GoReleaser to automate the release process:

1. When a new tag following the pattern `vX.Y.Z` is pushed to the repository, the [Release workflow](.github/workflows/release.yml) will automatically create a new release.

2. The release includes pre-built binaries for Android ARM64 targets.

## Manual Release Process

To manually create a new release:

1. Update the version in the code if needed
2. Create and push a new tag:
   ```bash
   git tag -a v1.2.3 -m "Release version 1.2.3"
   git push origin v1.2.3
   ```

3. Wait for the GitHub Action workflow to complete and generate the release

## Release Contents

Each release includes:
- Pre-built binary for Android ARM64
- Checksums for verification
- Release metadata

The binaries are built with the proper target architecture (ARM64) for Android devices.