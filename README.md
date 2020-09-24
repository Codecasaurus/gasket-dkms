The Gasket driver framework and Apex driver are kmods required to support Coral (Google) [Edge TPUs](https://coral.ai/). These drivers landed in [the 4.19 kernel](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=9a69f5087ccc20bb411025decab455836df04168). Google also publishes [dkms packages](https://coral.googlesource.com/gasket-dkms-debian/) for Debian-ish distros. Unfortunately that doesn't help non-Debian-ish users running kernels older 4.19.

This is an RPM/DKMS package for EL7 (and maybe EL8) distros based on the in-tree gasket driver (from kernel 5.4.67). Newer kernel versions (>=5.5) have breaking changes that require more work to backport to EL7 / 3.10. "PRs welcome."

Warning: I am not a kernel developer, I rarely build RPMs and I generally don't know what I'm doing. Use this package at your own risk.
