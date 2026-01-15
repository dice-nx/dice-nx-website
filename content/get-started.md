+++
draft = true
title = 'Get Started'
menu = 'main'
weight = 30
layout = 'content'
+++

{{< big-button caption="Download Latest DICE-nx Release" url="https://get.dice-nx.dev/latest.lha" >}}


## What you'll need

{{< callout "info" >}}
To use DICE-nx you will need good knowledge of AmigaOS, its Shell, how to program for the Amiga, and the C programming language itself. DICE-nx is not intended for beginners, unfortunately.
{{< /callout >}}

To install and run DICE-nx, you will need:

{{< grid >}}

{{< grid-row >}}

{{< grid-card "keyboard" "an Amiga computer" >}}
Either a real Amiga or an emulator such as WinUAE or Amiberry.
{{< /grid-card >}}

{{< grid-card "memory" "4 MiB of RAM" >}}
More memory beyond this can boost the performance of DICE-nx.
{{< /grid-card >}}

{{< grid-card "device-hdd" "10 MiB of free hard disk space" />}}

{{< /grid-row >}}

{{< grid-row >}}

{{< grid-card "floppy2-fill" "AmigaOS 2.0 or later" >}}
AmigaOS 3.2 is recommended. AmigaOS 1.3 may be possible for expert users...
{{< /grid-card >}}

{{< grid-card "boxes" "Native Developer Kit" >}}
An AmigaOS NDK that matches your OS version, and optionally for other OS versions too.
{{< /grid-card >}}

{{< grid-card "box-seam" "Dependent packages" >}}
If you don't already have them, grab
[LhA](http://main.aminet.net/util/arc/lha.run) and
[Installer](http://main.aminet.net/util/misc/Installer-43_3.lha).
{{< /grid-card >}}

{{< /grid-row >}}

{{< /grid >}}


## Install

Unpack the DICE-nx package to a temporary location. For example:

```
lha x DICE-nx-dist-3.20.0.lha RAM:
```

Using Workbench, open up the location where you unpacked the DICE-nx package. Double-click on the DICE-nx drawer, and then double-click on **Install DICE-nx**. Follow the on-screen instructions to install DICE-nx.


## Installing an NDK

If you have the AmigaOS NDK 3.2, then the installer script will offer to install the NDK for you - choose this option and follow the on-screen instructions.
