---
layout: post
title: "URGENT: ContentDB security incident: 22–26 October 2026"
authors: [Luanti team]
description: >-
  An attacker gained unauthorized access to ContentDB's servers, including emails,
  hashed passwords, and uploads. All users are advised to take action.
image: /static/blog/2026_cdb_incident/cover.webp
image_credit: Zenon Seth
---

An attacker gained unauthorized access to ContentDB's servers and data, including emails,
hashed passwords, and uploads. All users are advised to take action.

<!-- more -->

## What happened? (All times in UTC)

An attacker broke into ContentDB by exploiting two vulnerabilities. One of these
vulnerabilities was in a third-party component that we have reported to the
maintainer. We will share more once they have been fixed and made public.

From 22nd October 13:00, the attacker had access to ContentDB's internal
configuration. We have confirmed that they used this to sign into a staff
account. This configuration also allowed modifying uploads and sending emails,
but we do not have any evidence that this took place.

On 22nd October at 17:35, coincidentally, we deployed a patch for one of the
vulnerabilities. At this point, we did not know that it had been exploited
already.

From 24th October 23:00, the attacker began to probe the system for remote code
execution vulnerabilities.

From 26th October 00:15, we have confirmed that the attacker had full access to
run commands on our server inside a docker container. This means that they
will have had full access to the database and may have modified code that ran
inside this container.

On 26th October at 09:00, we discovered the break-in and took ContentDB offline.
We revoked all secrets, including sessions, API tokens, and GitHub OAuth tokens.

## What may have been accessed?

The attacker had full access to the secrets, database, redis, and uploads:

- Account information: usernames, emails, and hashed passwords. Passwords are
  stored as salted hashes (bcrypt) and never in plain text. Strong, unique
  passwords are hard to recover from these hashes, but weak or common ones can
  be guessed. However, you should still assume the password you used is no
  longer safe to use.
- IP addresses, not linked to any account, of people who downloaded packages
  from ContentDB or viewed them in-game in the two weeks before 26th October.
- Uploaded packages and release files.

With the secret key, they could act on behalf of any account.

We've checked every upload against our backups and have found no changes.
However, we haven't ruled out the possibility that the attacker caused ContentDB
to serve malicious uploads during the vulnerable period.

## What should you do?

- If you use your ContentDB password on any other sites, or a similar password,
  you need to change it immediately.
- Watch out for phishing emails, especially ones that pretend to be from Luanti.
- If you downloaded from ContentDB between 22nd October and 26th October, you
  may wish to check your downloads. We have seen no evidence of malicious
  uploads but have not ruled it out. You may wish to:
    - Redownload anything you downloaded during this time
    - Compare content against the upstream source
    - Compare content against the unofficial mirror:
      [contentdb.milcho.org](https://contentdb.milcho.org)
- When ContentDB comes back online, you will be asked to reset your password and
  any API tokens you have.

## What's next?

We are replacing the vulnerable components, continuing the security audit, and
are actively looking into preventing other incidents like this in the future.

ContentDB will remain offline whilst we make security updates. This is likely to
take a week or more.

We are continuing with the investigation and will share more information when we
can.

If you have any questions or concerns, or notice anything suspicious, please
contact us at security@luanti.org.
