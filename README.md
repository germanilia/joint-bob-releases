# Joint Bob releases

Public installation packages and checksums for Joint Bob. No GitHub account or update token is required.

[Download the latest release](https://github.com/germanilia/joint-bob-releases/releases/latest)

## Install or migrate

Run on macOS or Ubuntu as the user who runs Joint Bob:

```bash
installer="$(mktemp)"
curl -fsSL https://raw.githubusercontent.com/germanilia/joint-bob-releases/main/install.sh -o "$installer" && bash "$installer"
rm -f "$installer"
```

The installer verifies the release archive's SHA-256 checksum before installation and uses Joint Bob's transactional installer.

## Existing installations

Version `2.249.0` is the public-feed migration release. The identical package is also published on [the previous public feed](https://github.com/iliagerman/joint-bob/releases/tag/v2.249.0), so older installations can update normally and then use this repository.

An interim installation that already uses the private GitHub feed but has no token can use the installer above to migrate. Remove any explicit `JOINT_BOB_RELEASE_API` override to use the new public default.

## Repository contents

This repository contains release packages, checksums, this README, and the standalone installer. Development source and Git history are maintained separately in a private repository. Published packages include the application code required to run Joint Bob.

Release tags refer to this repository's independent history. The `.joint-bob-release` marker inside each package identifies its actual build commit.
