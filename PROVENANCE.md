# Source and provenance

The eZeus game executable is the existing, unmodified MacThings ARM64 0.8.1-Beta.8 binary.
Binary SHA-256: `f8b273a8c6395fde6d7bc69d8a61612d30e54b82a32ba3a502beb0cf08cd3ad0`.

Release: https://github.com/MacThings/eZeus/releases/tag/Zeus-Binaries
Published source tag: `Zeus-Binaries`, commit `b9e1678ffdd4d7f95b4ec743ba6f55c3d612183b`.
The code-only source snapshot from that tag is included. Original resource maps and fonts
from the upstream repository have been omitted to keep this program distribution free
of game assets. The publisher provides no reproducible-build proof, and the source tag
has not been rebuilt here. The tested executable is preserved byte for byte.

`Launcher.swift` is this package's new importer/launcher. Build it on an Apple Silicon Mac:

```sh
xcrun swiftc -O -target arm64-apple-macosx15.0 Launcher.swift -o eZeusLauncher
```

No engine compilation is required to use these packages. The ENG parser follows the MIT
licensed Citybuilding tools format reader: https://github.com/bvschaik/citybuilding-tools
Full notices are in `Licenses/`. Dependency source projects and notices are listed there.
The launcher and packaging scripts are GPL-3.0-or-later; text translations are provided
only as this eZeus localization patch. Original game rights remain with their owners.
