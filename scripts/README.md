# Build scripts

This directory contains userspace/rootfs build helpers.

## `build-rootfs.sh`

Creates the Debian Trixie ARM64 rootfs, copies the `rootfs/` overlay, installs matching kernel modules when supplied by the corresponding flow, validates the target sshd configuration, and produces the compressed ext4 image.

The `kernel-github` branch intentionally has no project-owned kernel build script and no boot-image packing script. Its kernel workflow invokes the Linux kernel build system directly and uses only configuration stored in `SaaSD3v/linux`.
