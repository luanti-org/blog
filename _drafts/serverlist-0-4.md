---
layout: post
title: "We'll remove 0.4.x from the serverlist soon"
authors: [the Luanti team]
# description: >-
#   Luanti has been removed from Google Play due to a DMCA notice from Tracer.AI.
#   We have filed a counter-notice, but this isn't the first time.
# image: /static/blog/2026_dmca/cover.webp
# forum_topic: https://forum.luanti.org/viewtopic.php?t=32663
# tags:
#   - last_month
---

In the last 8 years, we've made a massive effort to find and fix security
vulnerabilities and harden our code. Our most recent release fixed multiple
serious security vulnerabilities. By this point, we know that 0.4.x has multiple
critical vulnerabilities. To keep players safe, we will be removing 0.4.x
servers from the Luanti server list in 4 weeks.

<!-- more -->

## 0.4.x is not secure

We are aware of multiple critical security vulnerabilities affecting 0.4.x. More
worryingly, as 0.4.x is unsupported it likely has many unknown security
vulnerabilities.

Since 0.4.x, we have reworked and modernized our dependencies, reducing risk.
Irrlicht was effectively unmaintained and riddled with bugs. We merged it into
our code base, stripped it down, and replaced many of its functions with
well-maintained libraries like SDL and modern C++ code. As an example, we
recently discovered serious vulnerabilities in Irrlicht's mesh and image loading
code. These vulnerabilities put players at risk and the fixes will never make it
to the 0.4.x series.

0.4.x binaries also ship with dependencies from 8 years ago. Our dependencies
have released many security fixes in this time, including in zlib, libpng,
libjpeg, and curl - all of which have a remote attack surface.

## Removing 0.4.x servers reduces risk

By removing 0.4.x from the serverlist, we reduce the risk of 0.4 clients being
exploited remotely in the wild. Players can still connect to servers they trust
by using favorites or entering the address and port.

This action will remove 13 servers from the serverlist and impact an average of
20 concurrent online players. For comparison, there are 427 5.x servers with 450
online players.

We encourage those who stay on 0.4.x for preference reasons to start a
maintained fork of 0.4.x with the security fixes applied. This is especially
important for server owners to protect players and their data.
