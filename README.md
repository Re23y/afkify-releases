# AFKify releases

**AFKify your Roblox grind.** AFKify is a Windows app for building macros for Roblox without writing any code: clicks,
key presses, waiting for things to appear on screen, and the logic to handle what a game throws at you. Players share
their macros as **packs**, which anyone can import with a short code like `AFK-7KQ2-XP9F`.

This repository holds AFKify's installers. **Most people should download AFKify from
[afkify.com/download](https://afkify.com/download).** It's the same installer, and the site explains what to do next.

- Website: [afkify.com](https://afkify.com)
- Guide: [afkify.com/guide](https://afkify.com/guide)
- Discord: [afkify.com/discord](https://afkify.com/discord)
- Support: [support@afkify.com](mailto:support@afkify.com)

## What's here

| Kind | Tags | Who it's for |
|---|---|---|
| **Stable** | `v<version>` | Everyone, marked as the latest release. (None yet.) |
| **Beta** | `v<version>-beta.<number>` | Testers, staff and affiliates: new features first. Marked as pre-releases. |
| **Open-source sources** | `lgpl-sources-…` | The exact source of the open-source parts AFKify uses (see below). Not app releases. |

Each app release has:

- `AFKify-Setup-<version>.exe`: the installer;
- `SHA256SUMS.txt`: the SHA-256 checksum of each file;
- `SHA256SUMS.txt.sig`: an Ed25519 signature of those checksums (key `afkify-release-1`).

AFKify needs **Windows 10 or 11** and Roblox.

## How updates work

You install AFKify once. After that it keeps itself up to date:

1. **It checks for a new version** when it starts and every 6 hours while it's open (unless you turn that off in
   Settings), or whenever you choose **Help › Check for updates…**. It only looks at the releases here, and only at
   your update channel (Stable, or Beta if you can use it: **Settings › Updates**).
2. **It asks first.** Nothing is installed until you say yes.
3. **It checks the download before running it.** The installer's SHA-256 must match `SHA256SUMS.txt`, and that file's
   signature must match AFKify's release key. A download that doesn't match is never run.
4. **It updates in place.** The installer replaces the app, keeps your settings and packs, and opens AFKify again.

## Installing by hand

1. Download `AFKify-Setup-<version>.exe` from the release you want (or from
   [afkify.com/download](https://afkify.com/download)).
2. If you like, check it in PowerShell: `Get-FileHash .\AFKify-Setup-<version>.exe`, and compare the result with that
   file's line in `SHA256SUMS.txt`.
3. Run it. AFKify installs for your Windows account and needs no administrator rights.

**Not code-signed yet.** Until AFKify's installers are code-signed, Windows may say "Windows protected your PC". Click
**More info**, then **Run anyway**. Only ever do that for an installer from this page or afkify.com.

## Staying safe

- **Only download AFKify from [afkify.com](https://afkify.com) or this page.** Copies anywhere else (other websites,
  file-sharing links, Discord DMs) aren't ours and may be harmful.
- AFKify never asks for your Roblox password, cookies or sign-in codes, and never changes Roblox's files or memory.
- The AFKify team never asks for your password or payment details in a DM.
- Found a fake copy of AFKify? Tell us at [support@afkify.com](mailto:support@afkify.com).

## Open source

AFKify includes open-source software. Its licences come with the app (**Help › About AFKify › Licences…**). The source
code of the parts used under the GNU LGPL (Qt, Qt for Python and GEOS), in the exact versions each release uses, is
published here as `lgpl-sources-…` releases, and each app release's notes link to its own.

## About

AFKify is made by **AFKify Ltd**, a company registered in England and Wales (company number 17556954).
[Terms](https://afkify.com/terms) · [Privacy](https://afkify.com/privacy) · [Refunds](https://afkify.com/refunds)

AFKify isn't made by, endorsed by or affiliated with Roblox Corporation. Roblox is a trademark of Roblox Corporation.
