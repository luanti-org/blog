---
layout: post
title: "Luanti removed from Google Play due to baseless AI copyright notice"
authors: [the Luanti team]
description: >-
  Luanti has been removed from Google Play due to a DMCA notice from Tracer.AI.
  We have filed a counter-notice, but this isn't the first time.
excerpt: >-
  Luanti's Android app is currently not available on the Google Play Store due to
  a baseless DMCA notice filed on behalf of Microsoft by Tracer.AI, alleging that
  Luanti infringes Minecraft copyright. The Luanti app does not contain any
  proprietary code or assets, from Minecraft or otherwise.
image: /static/blog/2026_dmca/cover.webp
forum_topic: https://forum.luanti.org/viewtopic.php?t=32663
# tags:
#   - last_month
games:
  - src: /static/blog/2026_dmca/asuna.webp
    caption: >-
      <a href="https://content.luanti.org/packages/EmptyStar/asuna/">Asuna by EmptyStar</a>, a sandbox game with a focus on biomes and exploration
    alt: Asuna by EmptyStar, a sandbox game with a focus on biomes and exploration
  - src: /static/blog/2026_dmca/extra_ordinance.webp
    caption: >-
      <a href="https://content.luanti.org/packages/Sumianvoice/extra_ordinance/">Extra Ordinance by Sumi</a>, a top-down shooter
    alt: Extra Ordinance by Sumi, a top-down shooter
  - src: /static/blog/2026_dmca/lazarr.webp
    caption: >-
      <a href="https://content.luanti.org/packages/Wuzzy/lazarr/">Lazarr! by Wuzzy</a>, a puzzle game with lasers
    alt: Lazarr! by Wuzzy, a puzzle game with lasers
  - src: /static/blog/2026_dmca/klots.webp
    caption: >-
      <a href="https://content.luanti.org/packages/Warr1024/klots/">Klots by Warr1024</a>, a 3D sliding block puzzle game
    alt: Klots by Warr1024, a 3D sliding block puzzle game
---

Luanti's Android app is currently not available on the
[Google Play Store](https://play.google.com/store/apps/details?id=net.minetest.minetest)
due to a baseless
[DMCA notice](https://lumendatabase.org/notices/93778051) filed on behalf of
Microsoft by Tracer.AI, alleging that Luanti infringes Minecraft copyright. The
Luanti app does not contain any proprietary code or assets, from Minecraft or
otherwise.

We received an identical notice from the same company in 2023 and successfully
appealed against it. This company also filed a similar notice this year against
an indie game with similar voxel artstyle by the name of
[Allumeria](https://allumeria.com/).


<!-- more -->

## Table of Contents <!-- omit in toc -->

- [What is Luanti?](#what-is-luanti)
- [What is the DMCA notice?](#what-is-the-dmca-notice)
- [Which assets?](#which-assets)
- [Cubes are for everyone](#cubes-are-for-everyone)
- [What is Tracer.AI?](#what-is-tracerai)
- [This is not the first time this has happened](#this-is-not-the-first-time-this-has-happened)
- [This can't keep happening](#this-cant-keep-happening)
- [What next?](#what-next)

## What is Luanti?

[Luanti](https://www.luanti.org) is a voxel game-creation platform where anyone
can make, share, discover, and play blocky games. It does not ship with any
games or game assets by default. Instead, players can browse
[a catalog of games](https://content.luanti.org/packages/?type=game) created by
the community, or simply join multiplayer servers.

{% include figure_gallery.html items=page.games %}

We are a non-profit project developed by a community of passionate
individuals expressing their creativity. Luanti is open source, which means
anyone can view the source code, modify it, learn from it, redistribute it, and
even sell games made with it on platforms like Steam.

While Luanti is popular as an open-source alternative to Minecraft (as its roots
are in blocky sandbox games), it also lowers barriers to bringing creative ideas
to life. The freedom and customization Luanti affords has made it an excellent
tool in [education](https://www.luanti.org/education/), finding its way into
many schools across Europe.

## What is the DMCA notice?

The [Digital Millennium Copyright Act (DMCA)](https://en.wikipedia.org/wiki/Digital_Millennium_Copyright_Act)
is United States law which lays out a notice-and-takedown process which
platforms like Google Play follow to avoid liability for damages resulting from
copyright-infringing packages which they distribute. These platforms are not
responsible for the actions of their users, but they are responsible for taking
corrective action when user-generated content is reported.

The DMCA notice we received through Google claims that:

> These products use copyrighted assets as outlined directly from the Minecraft
> game (available at www.minecraft.net) without authorization and should be
> removed. Specifically, US Reg. #TX 8-192-097

"US Reg. #TX 8-192-097" is
[the registration of Minecraft Java Edition 1.9 with the US Copyright Office](https://publicrecords.copyright.gov/detailed-record/voyager_28402120).

It does not provide any information aside from this and does not outline which
assets Luanti allegedly uses.

## Which assets?

### Engine

Luanti is a game-creation platform and does not ship with any games, let alone
game assets. In fact, here are all the textures Luanti comes with:

{% include figure.html src="/static/blog/2026_dmca/builtin.webp" caption="All textures in the Luanti app" %}

Luanti also includes further assets, particularly fonts. These are properly
attributed in the [license file](https://github.com/luanti-org/luanti/blob/master/LICENSE.txt).

The GitHub repository does include the
[Development Test game](https://content.luanti.org/packages/Luanti/devtest/),
which is also available on ContentDB but is not included in Luanti releases
anymore. Being a testing ground for the engine, the textures are largely
utilitarian in nature.

{% include figure.html src="/static/blog/2026_dmca/devtest.webp" caption="Development Test game, for engine development" %}

### Minetest Game

Luanti _previously_ shipped with
[Minetest Game](https://content.luanti.org/packages/Luanti/minetest_game/),
a crafting survival game intentionally kept bare-bones to provide a base for
modding. [As of December 2023](https://blog.luanti.org/2023/12/04/5.8.0-released/),
it is no longer bundled with Luanti, and can be downloaded from within the
Luanti client like any other game. All of Minetest Game's assets are original
and properly licensed[^mtglicense].

{% include figure.html src="/static/blog/2026_dmca/mtg.jpg" caption="Minetest Game" %}

### Third-party content

Players can download content from ContentDB, our in-app game catalog. Except for
Minetest Game and Development Test, all these games, mods, and texture packs are
third-party, just like most apps on Google Play.

{% include figure.html src="/static/blog/2026_dmca/contentdb.webp" caption="ContentDB in the main menu" %}

Packages uploaded on ContentDB are reviewed manually by volunteer staff before
they are approved. We proactively check for copyright issues, including checking
for commercial assets. Independent of this incident, we have been looking into
automated asset flagging using conventional perceptual hashing algorithms. This
would help human moderators detect copyrighted assets, and we will always
require a final human decision without relying on erroneous AI.

It is in everyone's best interests that content on ContentDB is legal and free,
as it allows the community to safely use and build on top of it for their own
projects. If you are a rightsholder who believes your rights are being infringed
by content hosted on ContentDB, then the correct action is to submit a
[DMCA notice](https://content.luanti.org/copyright_dmca/) against the particular
game on ContentDB.

## Cubes are for everyone

The concept of a game featuring 3D cubes or voxels is not something anyone can
own[^copyrightideas]. Minecraft was originally inspired by the 2009 game
[Infiniminer](https://en.wikipedia.org/wiki/Infiniminer) which uses similar
voxel graphics, and later examples like Hytale show that block games make up an
entire genre that Minecraft is simply a part of. Mojang and its parent company
Microsoft have all rights to enforce their copyright for assets such as
Minecraft's textures, but cannot use the DMCA as a means to intimidate and
monopolize an entire genre of games.

Luanti was originally created by celeron55 in 2010 under the name "Minetest",
inspired by the newly-released Minecraft Alpha to make a sandbox in a voxel grid
that ran better on low-end hardware. Work began in 2011 on a modding API using
the [Lua](https://lua.org) programming language, allowing players to create
their own content. Minetest has continued to work to support a larger variety of
user creativity ever since. In 2024,
[the rename from Minetest to Luanti](https://blog.luanti.org/2024/10/13/Introducing-Our-New-Name/)
set this direction in stone.

## What is Tracer.AI?

Quoting their website:

> Tracer is a next-generation brand protection platform that empowers brands to
> take control of their brand presence online. Our AI agents streamline
> workflows and enhance operational efficiency, making it easier to monitor
> digital channels, take down detections, and analyze vast amounts of data to
> provide better business intelligence insights. Bring speed, accuracy, and
> efficiency to your brand protection strategy, without draining your team’s
> resources.
>
> Tracer’s AI brand protection technology detects and removes infringements to
> your brand across thousands of digital platforms, faster and more accurately
> than ever before.

From this, we can gather that Tracer uses AI agents for automated infringement
detection. In a
[2024 blog post](https://www.tracer.ai/tracer-blog/achieving-precision-and-speed-in-brand-protection-with-tracers-human-in-the-loop-ai),
the company boasts "85% faster takedowns", "100% more reviews
month-over-month" along with "review times that are six times faster than
traditional methods". It claims this has resulted in "44% more takedowns
month-over-month".

## This is not the first time this has happened

Luanti's Android app received an identical notice from the same company in
March 2023. As the notice was incorrect, we submitted a counter-notice and the app
was eventually reinstated... after 46 days[^timeline2023].
[Section 512(g)(2)\(c)](https://www.law.cornell.edu/uscode/text/17/512) of the
DMCA requires that providers "[replace] the removed material and [cease]
disabling access to it not less than 10, nor more than 14, business days
following receipt of the counter notice". Google's failure to adhere to the
deadlines specified by the DMCA raises questions regarding its approach toward
handling DMCA counter-notices.

In February of this year, an indie game called
[Allumeria](https://allumeria.com/) also received a DMCA takedown from Tracer.AI
on behalf of Microsoft, resulting in the game's temporary removal from the Steam
store. The notice
[was eventually dropped by Microsoft](https://www.pcgamer.com/games/survival-crafting/i-genuinely-do-not-know-what-to-do-says-developer-of-minecraft-like-allumeria-after-microsoft-issues-a-dmca-takedown-forcing-it-off-steam/) after much public noise.

## This can't keep happening

If a company can repeatedly submit the same DMCA notice with no explanation or
evidence, taking projects down for months at a time, the system is broken. It
prevents users from discovering or updating Luanti, and risks users settling for
shady or ad-ridden forks instead.

If we were a small company relying on income from the app, this would be
especially devastating. We, like most open-source communities, lack the
resources to continually fight unfounded DMCA notices.

## What next?

We have submitted a counter-notice and the app should be restored soon,
hopefully sooner than 46 days. But with counter-notices not being respected in
the set timeframe, a more public approach is required.

We call on Microsoft, Mojang, and Tracer.AI to stop relying on AI tools to send
inaccurate and vague DMCA notices. Detection must be verified by a human and,
more importantly, substantiated with tangible proof.

We call on Google to improve how they verify notices, allow users to respond to
notices without taking apps down for extended periods of time, and properly
comply with copyright law.

While we hope Google reinstates the Luanti app in a timely manner, we would like
to mention that the Luanti Android app is also available on
[F-Droid](https://f-droid.org/en/packages/net.minetest.minetest/), an app store
for Android whose official repository contains only verified free software.
In addition, APK downloads are available
[on our own website](https://www.luanti.org/en/downloads/). Unfortunately,
both distribution mechanisms are [increasingly under threat](https://keepandroidopen.org/).

We ask our community and readers to share this post far and wide, to help raise
awareness and ensure this doesn't happen again, for us or anyone else.

[^mtglicense]: [Minetest Game's LICENSE.txt](https://github.com/luanti-org/minetest_game/blob/master/LICENSE.txt)
[^copyrightideas]: 17 U.S. Code § 102(b) <https://www.law.cornell.edu/uscode/text/17/102>
[^timeline2023]: We submitted the counter notice on 25 March 2023 and the app was reinstated on 10 May 2023.
