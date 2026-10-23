# prebuilt
prebuilt kernels, initramfs, and other binary artifacts. They are built when we cut a release.

Linux configuration fragments live in `configs/linux/`. On each published
release, `.github/workflows/release.yml` builds Linux 7.3 and u-root v0.16.0
initramfs for x86_64, arm64, and riscv64, then attaches the kernel and initramfs
artifacts to the release. The fragments are merged with each architecture's
Linux `defconfig` before building.
