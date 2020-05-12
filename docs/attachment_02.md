# Attachment no. 2

## Task description

1. Setting up the hardware validation [1500 Euro]

  Validation standards in firmware related projects are not yet well established.
  Testing is very a crucial part when software directly touches hardware. Even the
  slightest change may cause huge negative impacts on the machine's operation.
  That is why we need to have automated tests that will constantly check for
  issues and regression due to the code change.

---

2. The specific tasks to be performed for coreboot project:

  2.1 The processor and chipsets code should be separated from board specific
    code. [2000 Euro]

  Separating the code allows for better maintenance and development of code by
  the whole community. Reduces the board specific code significantly and allows
  easier integration of existing and new boards.

  2.2 KGPE-D16 firmware should support RELOCATABLE_RAMSTAGE and cache the
    ramstage in TSEG. [2000 Euro]

  One of the coreboot requirements to keep the platform supported in the
  project. Implementing those mechanisms will allow us to use suspend to RAM
  (sleep mode).

  2.3. KGPE-D16 firmware support for POSTCAR_STAGE and NO_CAR_GLOBAL_MIGRATION [1500 Euro]

  One of the coreboot requirements to keep the platform supported in the
  project. Allows clean separation of the boot firmware stages and makes
  the code far simpler.

  2.4  KGPE-D16 firmware shall support C_ENVIRONMENT_BOOTBLOCK [1500 Euro]

  One of the coreboot requirements to keep the platform supported in the
  project. Allows to enable temporary memory early and setup a Root of
  Trust in the very early stage of machine startup.

  2.5 KGPE-D16 firmware save memory training parameters [1500 Euro]

  This feature will decrease the startup time by avoiding time-consuming memory
  training in subsequent machine launches.

  2.6 KGPE-D16 should initialize CPUs in parallel [1500 Euro]

  As KGPE-D16 is a server/desktop platform with up to 2 processing units with
  multiple cores, their initialization may take a while. This feature will
  reduce the startup time further.

  2.7 Improve the coreboot documentation and resolve existing and newly found
    issues. [2000 Euro]

  There were reports from the community that the board is no longer able to launch
  modern Linux distribution without custom modifications. There are also lots of
  unfixed items in the code base.

---

3. Contribution to other projects:

  3.1 Test and develop support in Heads project [1500 Euro]

  The Heads project focuses on security and privacy of the hardware it runs on.
  It is one of the very important use-cases of the KGPE-D16. The initial
  support has been done by Thierry Laurion on top the older version of
  coreboot. Required fixes and adjustments have not been propagated back.

  3.2 Develop, test and contribute support to OpenBMC and u-bmc projects. [4000 Euro]

  There is a huge amount of code developed by Raptor Engineering, but it's not
  contributed back to the upstream repositories. The support was developed over
  2 years ago and nothing has been done since that time. There is also a serial
  over IPMI feature to be developed in order to provide better remote
  accessibility to the board from network. This task requires contribution to
  projects like OpenBMC, Linux kernel, U-Boot, Poky and coreboot.

  3.3 Develop and test Secure Launch implementation in Trenchboot. [1500 Euro]

  Performing Secure Launch allows to establish the Root of Trust at any time of
  machine startup. It is a very important security feature offered by hardware.
  Moreover it was never done in an open source way for AMD processors (except
  Trenchboot for apu2 co-developed by 3mdeb) which are present on the KGPE-D16.

  3.4 Contribution to libreboot [1500 Euro]

  libreboot is based on the coreboot, however it implements the build system in
  its own way and modifies the coreboot source to its needs. The task will
  focus on adjusting the libreboot project in order to build the firmware image
  successfully and contribute the changes back.
