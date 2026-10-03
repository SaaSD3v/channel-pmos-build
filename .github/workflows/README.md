# GitHub Actions workflows

The `kernel-github` branch contains a kernel-only GitHub Actions build.

## `kernel-github.yml`

Builds Motorola Moto G7 Play (`channel`) directly from:

- repository: `SaaSD3v/linux`
- branch: `msm8953/latest`
- in-tree configs: `arch/arm64/configs/msm8953.config` and `arch/arm64/configs/motorola-channel.config`

The workflow does not apply an external device-tree patch, does not merge a configuration fragment from this build repository, and does not call project-owned kernel or boot-image shell scripts.

It publishes the raw kernel image, Channel DTB, matching modules, final kernel config, release metadata, `System.map`, and SHA-256 hashes. It intentionally does not create a `boot.img`, embed a rootfs/initramfs, or choose a root partition.

The other component launcher workflows are retained from `main` for their respective branches.
