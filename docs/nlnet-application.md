# KGPE-D16 Open Source Firmware

### Thematic call

ASUS KGPE-D16 Open Source Firmware

### Contact information

* Piotr Król

  3mdeb Founder and Embedded Systems Consultant

  Email: piotr.król@3mdeb.com

* Michał Żygowski

  3mdeb Firmware Engineer and Team Leader

  Email: michal.zygowski@3mdeb.com

* 3mdeb Embedded Systems Consulting - Office

  Phone: +48 58 718 91 79

  Email: contact@3mdeb.com

### General project information

This project mainly focuses on coreboot, which is integrated in other projects,
like Heads, Trenchboot and libreboot. The work described here implies other
projects like vboot (Verified Boot for integrity attestation) and the Linux
kernel.

Project page: https://coreboot.org/
Project wiki: https://doc.coreboot.org/index.html

This is the project we will mainly contribute to and where the wiki will be placed
for other project integrations. Any other project may also have additional
documentation about the KGPE-D16.

### Abstract

In recent years, processor manufacturers have been attempting to strengthen
security by adding new components to processors whose architecture and firmware
are kept secret (Intel ME [1], Intel MRC [2], Intel FSP [3], AMD AGESA [4], AMD
PSP [5], microcode [6]). Yet, to make matters worse, the hardware will not run
if these components are not present, furthering the push for open-source
firmware.

To be clear, we can not trust our hardware if the most basic building block is
an unknown. This means that a person looking for trust-worthy hardware, is
forced to search for what is called "binary blob-free" architectures. The ASUS
KGPE-D16 mainboard is one of the last "binary blob-free" x86-architecture based
platforms. As luck would have it, there was an open-firmware project that
supported that mainboard, but sadly that project is going to drop that support.

Trusting the integrity of our systems to commercial interests rather than an
open-source project that we can audit seems ludicrous. Our project aims to
create a secure open-source firmware for all users, respecting and protecting
their security, privacy, and foremost, their freedom.

[1]: https://en.wikipedia.org/wiki/Intel_Management_Engine
[2]: https://en.wikipedia.org/wiki/Memory_Reference_Code
[3]: https://www.intel.pl/content/www/pl/pl/intelligent-systems/intel-firmware-support-package/intel-fsp-overview.html
[4]: https://en.wikipedia.org/wiki/AGESA
[5]: https://en.wikipedia.org/wiki/AMD_Platform_Security_Processor
[6]: https://en.wikipedia.org/wiki/Microcode

### Compare your own project with existing or historical efforts

3mdeb is a licensed coreboot consultant. coreboot is the project where
Raptor Engineering implemented the support for ASUS KGPE-D16. This project aims
to continue the support by keeping the code maintained and tested on the
hardware. Without it there will be currently no option for secure hardware based
on x86 architecture. 3mdeb always strives to promote open and secure solutions
and ASUS KGPE-D16 is an ideal hardware to achieve it, because it is one of the
last blob-free machines that can be owner controlled. We also develop BIOS and
firmware for other companies (like PC Engines) and have much experience in
firmware development on machines like the ASUS KGPE-D16. We also would like to push
further the support of the Baseboard Management Controller (BMC) for this platform
in order to increase the availability of the solution. We are also Yocto
Participants and have experts to develop the OpneBMC support. Our wide range
of experts make us a perfect fit to complete the project.

### What are significant technical challenges you expect to solve during the project, if any?

One of the main challenges is to revive the code base for the machine which
hasn't been touched and tested for a long time. Locating old and unresolved
bugs will also be a huge effort. The state of support in other projects also is
not in the best shape (see the related projects in attachment number one). The
scope of projects that needs fixes and contributions is wide.

The second biggest challenge is the validation infrastructure. Hardware testing is
much more complex and different on the firmware level, thus requires special
approach. Validation standards in firmware related projects are not yet well
established. We aim to be the pioneers of the validation standard in the
projects like coreboot. Testing is a very crucial part in such a dynamically
evolving environment, where code patches that touch every hardware board, are
being applied on a daily basis and each change may bring unexpected results.

### Requested support

22000 Euro.

About half of the budget will focus on getting needed features and fixes added
to the coreboot project in order to keep the platform alive in the main tree.
The main focus is put on coreboot since it is the base for integrating and
testing related projects (Linux kernel, Heads). The other half will be spent on
contribution and developing other projects (Linux kernel, Yocto, U-Boot,
OpenBMC, u-bmc, libreboot). The last third part of the fund will be spent on
designing a validation infrastructure and standards for firmware related
projects (Linux kernel, U-Boot, coreboot, libreboot). The detailed description
of tasks is available in attachment no. 2.

1. Setting up the hardware validation [1500 Euro]
2. The specific tasks to be performed for coreboot project:
2.1 The processor and chipsets code should be separated from board specific
    code. [2000 Euro]
2.2 KGPE-D16 firmware should support RELOCATABLE_RAMSTAGE and cache the
    ramstage in TSEG. [2000 Euro]
2.3. KGPE-D16 firmware support for POSTCAR_STAGE and NO_CAR_GLOBAL_MIGRATION [1500 Euro]
2.4  KGPE-D16 firmware shall support C_ENVIRONMENT_BOOTBLOCK [1500 Euro]
2.5 KGPE-D16 firmware save memory training parameters [1500 Euro]
2.6 KGPE-D16 should initialize CPUs in parallel [1500 Euro]
2.7 Improve the coreboot documentation and resolve existing and newly found
    issues. [2000 Euro]
3. Contribution to other projects:
3.1 Test and develop support in Heads project [1500 Euro]
3.2 Develop, test and contribute support to OpenBMC and u-bmc projects. [4000 Euro]
3.3 Develop and test Secure Launch implementation in Trenchboot. [1500 Euro]
3.4 Contribution to libreboot [1500 Euro]

### Projects or organisations relevant to this project before?

Detailed description and role of the related projects organizations can be
found in the attachment no. 1.

- [coreboot](https://github.com/coreboot/coreboot)
- [libreboot](https://notabug.org/libreboot/libreboot)
- [Heads](https://github.com/osresearch/heads/)
- [OpenBMC](https://github.com/openbmc/openbmc)
- [u-bmc](https://github.com/u-root/u-bmc)
- [U-Boot](https://gitlab.denx.de/u-boot/u-boot/)
- [Linux kernel](https://github.com/torvalds/linux)
- [Poky Yocto](https://git.yoctoproject.org/cgit/cgit.cgi/poky/)
- [Trenchboot](https://github.com/TrenchBoot/documentation)
- [vboot](https://chromium.googlesource.com/chromiumos/platform/vboot_reference/)
- [Vikings GmbH](https://www.vikings.net/)
- [Raptor Engineering LLC](https://www.raptorengineering.com/)  

### Compare your own project with existing or historical efforts

3mdeb is a licensed coreboot consultant. coreboot is also the project where
Raptor Engineering implemented the support for ASUS KGPE-D16. This project aims
to continue the support by keeping the code maintained and tested on the
hardware. 3mdeb always strive to promote open and secure solutions and ASUS
KGPE-D16 is an ideal hardware to achieve it, because it is one of the last
binary blob-free x86 architecture based platforms that can be owner controlled
(https://ryf.fsf.org/products/VikingsD16). We also develop BIOS and firmware
for other companies (like PC Engines) and have much experience in the
development on machines like ASUS KGPE-D16. We also would like to push further
the support of the Baseboard Management Controller (BMC) for this platform in order
to increase the availability of the solution. The BMC is required to have the
automatic thermal control and remote management of the ASUS KGPE-D16 platform.
We are also Yocto Participants and have experts to develop the OpenBMC support.
Our wide range of engineers make us a perfect fit to complete the project.

### What are significant technical challenges you expect to solve during the project, if any?

One of the main challenges is to revive the code base for the machine which
haven't been touched and tested for a long time. Locating the old and
unresolved bugs will also be a huge effort. The state of support in other
projects also is not in the best shape. The scope of projects that need fixes
and contributions is wide.

The second biggest challenge is the validation infrastructure. Hardware testing is
much more complex and different from software testing, thus requires special a
approach. Validation standards in firmware related projects are not yet well
established. We aim to be the pioneers of the validation standard in the
projects like coreboot. Testing is a very crucial part in such a dynamically
evolving environment, where code patches that touch every hardware board, are
being applied on a daily basis and each change may bring unexpected results.

### The ecosystem of the project

There are several developers and people already interested in this outcome,
however, any of the current contributors to the projects mentioned above
(coreboot, Heads, Trenchboot, OpenBMC) are welcome to join us in this open
source development. Our thread on the coreboot mailing list got many positive
responses:

https://mail.coreboot.org/hyperkitty/list/coreboot@coreboot.org/thread/KVXTVFEINCCM7OZOWRERFI2CL3BMGC6L/#AGOCLQURLB7BAJDB7VVFVDV7KBOQWWS7

Although 3mdeb will be responsible for the whole implementation and testing, anyone
is also welcome to test, develop code and report issues. The implemented code
will be additionally reviewed by the experts and core developers of the related
projects we are going to contribute to:

* Patrick Rudolph: firmware developer (coreboot), https://9elements.com,
https://github.com/PatrickRudolph

* Kyösti Mälkki: firmware developer (coreboot), https://github.com/kmalkki

* Arthur Heymans: firmware developer (coreboot), https://github.com/ArthurHeymans

* Trammel Hudson, Heads project initiator, security researcher. https://github.com/osresearch,
https://trmm.net/

* Francis Lam, Heads collaborator and code reviewer: https://github.com/flammit

* Thierry Laurion, Heads collaborator and code reviewer: https://github.com/tlaurion

* Andrew Jeffery and Joel Stanley, Linux kernel ASPEED support maintainers and
  code reviewers

* Armin Kuster, maintainer of the Yocto project

* Brad Bishop, maintainer and reviewer of OpenBMC project

* Tom Rini, maintainer of the ARM architecture (the ASPEED chipset
  architecture) in the U-Boot project

* Daniel P. Smith, maintainer of Trenchboot project