+++
draft = true
title = 'FAQ'
menus = 'main'
weight = 30
layout = 'content'
+++

## General

{{< faq-section >}}

{{< faq "Who is maintaining DICE-NX?">}}
DICE-NX is currently maintained by [Richard Downer](https://github.com/rdowner). I hope that others
will join in the effort to improve DICE-NX for the modern retrocomputing community.
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
Your Amiga should have a hard drive, at least 2MiB of RAM, and AmigaOS 3.2. You must also have the
AmigaOS 3.2 NDK to hand, either from the AmigaOS 3.2 CD-ROM or - preferably - the latest version
downloaded from the Hyperion Entertainment website (but note that you must be a registered owner
of AmigaOS 3.2 to access the download section of that website).
{{< /faq >}}

{{< faq "Do I need to buy AmigaOS 3.2?" >}}
Yes. DICE-NX requires AmigaOS 3.2 NDK, which currently can only be legally obtained by purchasing
AmigaOS 3.2 from Hyperion Entertainment.

I realise that this is a barrier for many people, and I intend to allow DICE-NX to once again use
the NDKs from earlier AmigaOS releases, when development time permits me.
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
DICE-NX currently only supports NDK 3.2. This is somewhat of a backwards step as DICE supported
multiple simultaneous NDK versions, but it was faster to support AmigaOS 3.2 by dropping
compatibility for the earlier NDKs.

I hope to be able to restore support for NDK versions 1.3, 2.0, 3.0 and 3.1 in the future.
{{< /faq >}}

{{< /faq-section >}}
