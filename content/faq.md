+++
draft = true
title = 'FAQ'
menus = 'main'
weight = 40
layout = 'content'
+++

## General

{{< faq-section >}}

{{< faq "Who is maintaining DICE-NX?">}}
DICE-NX is currently maintained by [Richard Downer](https://github.com/rdowner). I hope that others
will join in the effort to improve DICE-NX for the modern retrocomputing community.
{{< /faq >}}

{{< faq "What is the current version of DICE-nx?" >}}
DICE-nx is currently at version 3.20.0.

So far this is the only release of DICE-nx.
{{< /faq >}}

{{< faq "Why did DICE-nx start version numbering at 3.20.0?" >}}
Ideally, DICE-nx would have continued from the next version number after the last DICE release.
Unfortunately, it's not clear what last DICE version number *was*.

The last release of the commercial DICE product was 3.15. After this, there was the first
open-source (but not BSD-licensed) release of the DICE source code around 1997. This contained some
updates that had not previously been part of a binary release, so a developer named Richard Drummond
took that source code release and made a binary release he called 3.16, in 1998.

On Matt Dillon's own website, his releases of DICE were labelled 1.14 and 1.15 (1.15 being the
relicense to BSD License, in 2023). Both contain new updates since the 3.15/3.16 time frame. The
reason for the version number reset is unknown, and as the source code history is largely lost, we
don't have a clear idea what happened between 1997 and 2023.

There is also a slight unknown in that semantic versioning wouldn't become a thing until around
2009. Prior to this, there were a few conventions but no single established best practice. In the
Amiga world in the 1990s, a version like "3.15" would typically be interpreted as either:

* Semantic versioning style - the 15th minor release after the 3rd major release
* As a decimal number - where 3.15 is sometime after 3.1 but before 3.2

I took the decision to make the first DICE-nx version 3.20, and to commit to semantic versioning
from this point on. I chose this for these reasons:

* I chose to ignore the "reset" versions and continue the version numbering from the releases
  available on Aminet. To continue with 1.x-series releases would cause confusion, as people would
  assume that 3.16 from Aminet is newer.
* No matter if you are using semantic or decimal style versions, 3.20 is later than any known DICE
  release.
{{< /faq >}}


{{< faq "What is the origins of DICE-NX?">}}
DICE-NX is a continuation of DICE, a commercial C compiler written by Matt Dillon in the 1990s.
In the late 90s, Matt ceased development of DICE and made it available under a "source available"
style license - one where the source code is available but some restrictions are applied so it does
not fall under OSI's open source definition - in DICE's case, the license prohibited commercial
use.

Matt did a small amount of development on DICE between then and 2023, mostly focussed on changing
it to be hosted on BSD instead of Amiga, supporting 64-bit host OSes, for the purpose of generating
ROMable code for 68000 embedded systems.

Then, in October 2023, Matt relicensed DICE to BSD, and I forked it to create DICE-NX.
{{< /faq >}}

{{< faq "What is the relationship between DICE-NX and DICE?" >}}
DICE-NX is a fork of DICE, as of DICE's relicensing to BSD in October 2023. The original DICE is
unlikely to see further activity as it's author, Matt Dillon, has moved on to other projects.
Meanwhile DICE-NX is re-starting development on DICE. (It's also entirely possible that other
people may fork DICE and take it in a different direction to both the original and DICE-NX.)

There is no ongoing relationship between the two projects.
{{< /faq >}}

{{< faq "Why did DICE-NX change the name from DICE?" >}}
This was done at the request of Matt Dillon, developer and owner of the original version of DICE. I
am happy to comply with his wish that this fork is distinguished from the original.
{{< /faq >}}

{{< /faq-section >}}

## Getting started

{{< faq-section >}}

{{< faq "What do I need before I get started with DICE-NX?" >}}
To use the packaged binary release of DICE-NX, you will need an Amiga (either real or emulated).
Your Amiga should have a hard drive and at least 2MiB of RAM.

AmigaOS 2.04 or later is recommended. DICE-nx is developed using AmigaOS 3.2 and you will likely have an easier time if you are using AmigaOS 3.2. DICE did support AmigaOS 1.3 but DICE-nx has not been tested on this version, so consider that an experts-only option.

You must also have an AmigaOS NDK 3.2. NDK 3.2 can be freely downloaded from Aminet,
making it the easiest NDK to legally obtain at this time, and you can still target earlier AmigaOS
releases even if you are using NDK 3.2.
{{< /faq >}}

{{< faq "Do I need to buy AmigaOS 3.2?" >}}
No. DICE-nx is developed using AmigaOS 3.2 and you will likely have an easier time if you are using AmigaOS 3.2, but it does work on earlier AmigaOS versions too.
{{< /faq >}}

{{< /faq-section >}}

## Developing for AmigaOS

{{< faq-section >}}

{{< faq "Can I build applications for AmigaOS 3.2?">}}
Yes, DICE-NX supports building AmigaOS 3.2 applications. Supporting the newest AmigaOS releases is
a key goal for DICE-NX.
{{< /faq >}}

{{< faq "Can I build applications for earlier AmigaOS releases?" >}}
Yes, the AmigaOS 3.2 NDK (Native Developer Kit) is backwards compatible with AmigaOS 3.1 and
earlier. However you will have to make sure that you do not use any AmigaOS 3.2 specific features,
library calls, structures, etc. Refer carefully to the AmigaOS AutoDocs and other documentation,
and make sure that you degrade gracefully instead of causing a system crash.
{{< /faq >}}

{{< faq "Can I build applications for AmigaOS 3.5 and 3.9?" >}}
AmigaOS 3.5 and 3.9 is not officially supported by DICE-NX. They are backwards compatible with
AmigaOS 3.1, so if you limit to using AmigaOS 3.1 features, that can be reasonably expected to work
on 3.5 and 3.9. However if you wish to develop features that are part of 3.5 and/or 3.9 but not
part of 3.2, this may be tricky and you should be prepared to do some work to make it work.
{{< /faq >}}

{{< faq "Can I build applications for AmigaOS 4?" >}}
No. AmigaOS 4 uses the PowerPC CPU architecture, and DICE-NX only supports the 68000 CPU
architecture.
{{< /faq >}}

{{< faq "Can I use AmigaOS NDKs other than 3.2?">}}
DICE-NX currently only officially supports NDK 3.2. This is somewhat of a backwards step as DICE supported multiple simultaneous NDK versions, but it was faster to support AmigaOS 3.2 by dropping
compatibility for the earlier NDKs.

I hope to be able to restore official support for NDK versions 1.3, 2.0, 3.0 and 3.1 in the future. In the mean time, you may still be able to use the earlier NDKs if you install them manually, but consider that an experts-only option.
{{< /faq >}}

{{< faq "What are inline library calls?" >}}
Inline library calls are one possible implementation of how programs written in C can make calls to
AmigaOS libraries.

In C, we want to be able to call AmigaOS libraries (API calls, in modern terms) in as simple a way
as possible. They are expressed in the OS documentation as something like making a function call:

```c
struct Library = OpenLibrary("mylib.library", 0L);
```

In practice, the AmigaOS interface is not a C function call. The traditional method of calling
AmigaOS relies on a file called `amiga.lib` which is part of the AmigaOS NDK. This linker library
contains a function that can be invoked from C for every AmigaOS API call; each implementation is
a handful of machine code instructions that invokes the equivalent AmigaOS API call, adapting the OS
interface to C language conventions.

This works quite well, but it is inefficient. The AmigaOS interface is designed to be fast - it
can be invoked with just a few machine code instructions - but the C function call conventions are
slower.

Inline library calls solve this problem. When enabled and supported, DICE-nx can directly generate
the machine language instructions to invoke the AmigaOS API. This speeds up OS calls and reduces the
dependency on amiga.lib.
{{< /faq >}}

{{< faq "How do I use inline library calls?" >}}
The are two things you need to do. Firstly, when invoking the `dcc` command, pass the `-mi` and
`-proto` arguments. This instructions DICE-nx to make inline library calls whenever possible, and
to check that all library calls are correct according to the function prototypes.

Secondly, DICE-nx needs additional information about the AmigaOS API. These are supplied in special
header files in the AmigaOS NDK. For each AmigaOS library that you will be using, you must use
an `#include` directive using this naming convention:

```c
/* support inline library calls for "exec.library" */
#include <proto/exec.h>
/* support inline library calls for "graphics.library" */
#include <proto/graphics.h>
/* support inline library calls for "intuition.library" */
#include <proto/intuition.h>
```

These include directives will bring in C-style function prototypes so that library invocations are
checked for type correctness, and brings in the extra information (DICE-nx-specific `#pragma`
directives) that allows DICE-nx to construct the correct machine code instructions to make the
library call.

If you include the header from `proto`, you do not need to include any headers from `clib`,
`pragma`, or `pragmas`. Any AmigaOS includes that begin with those directories can be removed.
{{< /faq >}}

{{< /faq-section >}}
