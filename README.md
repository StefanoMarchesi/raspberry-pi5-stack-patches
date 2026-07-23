# Raspberry Pi 5 stack patches

Recovery archive for measured and experimental Raspberry Pi 5 graphics and
emulation changes. Patch series are kept here when the original upstream uses a
different forge, or when a change still needs to be split and validated before
an upstream submission.

This repository is a backup and review staging area. A patch being present does
not imply that it is upstream-ready.

## Mesa

`mesa/26.1.4` contains the seven commits from the Raspberry Pi checkout based on
Mesa 26.1.4 (`e462dccf`) through the ROAA fixes (`ef9f037`). The series includes
the V3D GL 3.3 capability change, the custom V3DV work, and the two independently
submitted fixes for channel-count/MSAA TLB reads and multisample input-attachment
lowering.

Apply in numeric order with `git am`. The later V3DV commits must be separated
and validated with the relevant Vulkan CTS coverage before proposing them to
Mesa upstream. Patches 6 and 7 are the reviewed ROAA correctness follow-ups and
are kept separate from the larger experimental driver patch.
