## Attachment no. 1

## Projects or organisations relevant to the project before

- [coreboot](https://github.com/coreboot/coreboot)

Open source firmware framework supporting the hardware of the aforenamed project
relates to. In general coreboot allows to build the firmware (also called BIOS)
from source code. By firmware (or BIOS) one should understand the lowest level
software executed on the processor right after machine launch. It is
responsible for hardware initialization and preparation for operating system
launch. The BIOS implementation for KGPE-D16 is fully open and auditable in
contrast to closed source proprietary solutions of current hardware vendors.

- [libreboot](https://notabug.org/libreboot/libreboot)

This project is based on coreboot, but operates with different rules and
restrictions. First and foremost the libreboot project does not allow any
source code for platform firmware which requires closed source components to
operate. coreboot on the other hand supports platforms that require closed
source and proprietary components used for hardware initialization (Intel FSP,
AMD AGESA, Intel ME, AMD PSP).

- [Heads](https://github.com/osresearch/heads/)

A coreboot's Linux based payload focusing on security of the firmware and
operating systems booting. Uses sophisticated methods for privacy preserving,
security measures, hardware ownership and Root of Trust attestation. The
ultimate goal is to ensure that the computer is in a trusted state and that the
operating system may be launched securely without fear of leaking sensitive and
private data or the presence of malware. Has initial support for the board:
https://github.com/osresearch/heads/pull/335

- [OpenBMC](https://github.com/openbmc/openbmc)

Open implementation of the Baseboard Management Controller (BMC) present on
server/desktop platforms, based on Linux. The BMC is responsible for
out-of-band management of the server/desktop platform, it has privileged access
to the resources of the machine thus is very important piece of hardware and
software that should be protected. Open implementation assures auditability and
security of the BMC solution typically delivered by hardware vendors as a
closed source component. Has support for the board (unmaintained) done by
Raptor Engineering:
https://www.raptorengineering.com/coreboot/kgpe-d16-bmc-port-status.php

- [u-bmc](https://github.com/u-root/u-bmc)

The BMC Linux distribution similar to OpenBMC but written in Go language.
Currently does not support KGPE-D16's AST2050 chipset:
https://github.com/u-root/u-bmc/issues/133
The main advantages of u-bmc are minimalism and compactness comparing to
OpenBMC.

- [U-boot](https://github.com/u-boot/u-boot)

U-Boot is a boot loader for Embedded boards based on PowerPC, ARM, MIPS and
several other processors, which can be installed in a boot ROM and used to
initialize and test the hardware. It is one of subcomponents of the OpenBMC
implementation. Initial implementation:
https://www.raptorengineering.com/coreboot/kgpe-d16-bmc-port-files/ast2050-uboot-tree.tar.bz2

- [Linux kernel](https://github.com/torvalds/linux)

Linux is an open source implementation of the GNU operating system's kernel. It
is a subcomponent of the OpenBMC implementation and subcomponents of operating
systems launched by the KGPE-D16. Initial implementation:
https://www.raptorengineering.com/coreboot/kgpe-d16-bmc-port-files/ast2050-linux-kernel-tree.tar.bz2

- [Poky Yocto](https://git.yoctoproject.org/cgit/cgit.cgi/poky/)

Poky is a reference distribution of the Yocto Project. It contains the
OpenEmbedded Build System (BitBake and OpenEmbedded Core) used to build a Linux
distribution. A subcomponent of the OpenBMC implementation. Initial
implementation for the KGPE-D16:
https://git.raptorengineering.com/git/ast2050-yocto-poky

All the source code lack maintainership since the platform has been orphaned by
the initial maintainer. The number of bugs is growing and soon the code will be
deprecated and dropped from the projects like coreboot and others.

- [Trenchboot](https://github.com/TrenchBoot/documentation)

Trenchboot is a framework that allows individuals and projects to build
security engines to perform launch integrity actions for their systems. The
framework builds upon Boot Integrity Technologies (BITs) that establish one or
more Roots of Trust (RoT) from which a degree of confidence that integrity
actions were not subverted. 3mdeb already contributed to this project by
enabling the Secure Launch feature offered by the hardware security engines
on the PC Engines apu2 board.

- [vboot](https://chromium.googlesource.com/chromiumos/platform/vboot_reference/)

Google's Verified Boot reference implementation, an alternative to UEFI's
SecureBoot. Provides mechanisms for cryptographical signing and verification of
boot firmware components.

- [Vikings GmbH](https://www.vikings.net/)

Company that sells the ASUS KGPE-D16 with libre firmware based on an old
version of coreboot. Big kudos to Vikings for sending 2 boards for testing and
development of the project.

- [Raptor Engineering LLC](https://www.raptorengineering.com/)

The company that did the initial implementation of the coreboot firmware and
OpenBMC for the ASUS KGPE-D16. The board has been neglected by this company and is
no longer maintained in those projects.
