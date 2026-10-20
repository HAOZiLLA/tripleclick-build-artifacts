# tripleclick-build-artifacts

Pinned third-party binaries that Tripleclick's render workers install at image
build time. Nothing here is Tripleclick code: each release holds an unmodified
upstream build, mirrored so a pin stays downloadable after the upstream
autobuild is pruned. The pin itself (file name, SHA-256, install step) lives in
the private application repo and is verified on every build; the weekly check
there confirms this mirror and the upstream still serve the exact bytes.

| Tool | Release | File | SHA-256 | Upstream |
|---|---|---|---|---|
| FFmpeg 8.0.1 line (static GPL, linux64) | `ffmpeg-n8.0.1-66-g27b8d1a017` | `ffmpeg-n8.0.1-66-g27b8d1a017-linux64-gpl-8.0.tar.xz` | `26d2ecd0cefba99f9d1ea92252a3a4f743a58df4c1c3cf9f8bbaaa40b1fca5b0` | [BtbN/FFmpeg-Builds autobuild-2026-02-28-12-59](https://github.com/BtbN/FFmpeg-Builds/releases/tag/autobuild-2026-02-28-12-59) |

## Licensing

FFmpeg is licensed under the GPL when built with GPL components, as these
builds are. The binaries are redistributed unmodified; the corresponding
source is the [FFmpeg source tree](https://git.ffmpeg.org/ffmpeg.git) at the
tag named in each release and the
[BtbN/FFmpeg-Builds](https://github.com/BtbN/FFmpeg-Builds) build scripts,
which also list every bundled library and its licence
(`ffmpeg-*/LICENSE.txt` inside the tarball).
