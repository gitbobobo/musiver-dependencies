# Recipes

Each JSON recipe records the public source URL and SHA-256, exact configure flags, artifact name and digest, license files, and the command used to build the archive. Build logs live under `build-logs/`; copied upstream license texts live under `licenses/`. A release asset is immutable: publish a new `v*` release when any field or build input changes.

The Apple FFmpeg recipe is currently published as `apple-ffmpeg-lgpl-8.1.1-4.zip`. Its archive contains only LGPL FFmpeg libraries and the corresponding license/build metadata.
