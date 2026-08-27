+++
title = 'About DICE-nx'
menu = { main = { name = "About", weight = 20 } }
layout = 'content'
+++

{{< leader >}}
This is DICE-nx - a C&nbsp;compiler for Commodore&nbsp;Amiga computers and embedded 68k systems.
DICE-nx includes all the tools needed to build Amiga executables - the C&nbsp;compiler itself, as
well as an assembler, linker and numerous other support tools. It also has several Amiga-specific
features, such as automatic opening of the common Amiga OS libraries, easy support for ARexx, and
more.
{{< /leader >}}

DICE can also target embedded systems using 68000 processors.

DICE-nx is a fork of DICE, which was originally a commercial product written by Matt Dillon in the
1990s. In the late 1990s, commercial development of DICE ceased and its source code was released
under a "non-commercial use only" license. In 2023, Matt re-licensed it under the standard 3-clause
BSD license, meaning for the first time ever DICE was available under a true open-source license.

DICE-nx aims to re-start development of DICE, and focusing on its original aim of providing a
fully-featured C&nbsp;compiler for Amiga computers. At this time, the original 68000-based Amiga
series is seeing increased support from retro-computing enthusiasts, including the restarting of
AmigaOS development with the release of AmigaOS 3.2. DICE-nx aims to provide for this audience,
fully supporting AmigaOS 3.2 and native development on real Amiga hardware.


## What's new in DICE-nx

Although DICE-nx is in the early stages of its life, it has already made these changes from the
original DICE:

* Compatibility with AmigaOS 3.2, the latest release of the 68000-based AmigaOS from Hyperion
  Entertainment
* A new Installer-based hard drive installation process
* A reworked build system that can bootstrap DICE-nx from either an earlier version of DICE on an
  Amiga, or using GCC on a Linux PC
* Strips back on duplicated, unused and optional 3rd-party files
* A number of bug fixes and small improvements

Many bigger changes are planned to happen in future releases!


## Built exclusively for the Commodore&nbsp;Amiga

DICE-nx is a fully self-hosted C compiler system that runs natively on the Commodore&nbsp;Amiga
series of computers. As the Amiga system is its first-class target, it offers a number of features
specially suited to the Amiga:

* Fully-integrated support for AmigaOS functionality. Call into AmigaOS as easily as calling a
  regular C function. The AmigaOS NDK provides full function prototypes, macros, structure
  definitions and more to make using AmigaOS from C as simple as possible. Inline library calls make
  OS calls fast and efficient.
* Integrated ARexx support, allowing you to add ARexx ports to your applications with ease and
  support cross-process scripting Amiga-style.
* Create *pure* executables that can be loaded `Resident` with a simple compiler option.
* Supporting 3rd-party "library" as easily as AmigaOS itself - write code that uses
  bsdsocket.library, MUI, ReqTools and many more with little effort. The support for libraries is
  generic, supported by tools provided by DICE-nx, meaning that **any** Amiga library that comes
  with C headers and an `FD` file can be integrated into DICE-nx.


## Get Started

To get started with DICE-nx, head over to the [Get Started]({{< relref "get-started" >}}) page and download
the latest binary distribution!
