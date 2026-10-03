# Kernel configuration

The `kernel-github` branch does not keep an external Channel kernel fragment in this build repository.

Kernel configuration is sourced directly from the kernel tree:

- `arch/arm64/configs/defconfig`
- `arch/arm64/configs/msm8953.config`
- `arch/arm64/configs/motorola-channel.config`

This keeps the Channel hardware and bring-up requirements in `SaaSD3v/linux` instead of injecting them from the postmarketOS/build repository.
