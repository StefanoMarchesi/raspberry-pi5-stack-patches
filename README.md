# Raspberry Pi 5 stack patches

Recovery archive for measured and experimental Raspberry Pi 5 graphics and
emulation changes. Patch series are kept here when the original upstream uses a
different forge, or when a change still needs to be split and validated before
an upstream submission.

This repository is a backup and review staging area. A patch being present does
not imply that it is upstream-ready.

## Mesa

`mesa/26.1.4` contains the five commits from the Raspberry Pi checkout based on
Mesa 26.1.4 (`e462dccf`) through `driver-patches-test` (`faecaa0a`). The series
includes the V3D GL 3.3 capability change and later experimental V3DV work.

Apply in numeric order with `git am`. The later V3DV commits must be separated
and validated with the relevant Vulkan CTS coverage before proposing them to
Mesa upstream.
