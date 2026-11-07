# OZMA

OZMA is a music tracker for the **TrimUI Brick**. This repository is the public home for
OZMA releases: download zips, the changelog and the bug report form.

> **Status:** open beta test (OBT) is being prepared. No release has been published yet.

The source code is not published here. OZMA is closed-source freeware; see "License" below.

## Install (short version)

1. Download `OZMA-<version>.zip` from [Releases](../../releases) and check its `.sha256` if you like.
2. Turn the Brick off and put its microSD card in your computer.
3. Unzip the archive **into the root of the card** and allow it to merge folders.
   You will get `App/OZMA` (the app and your data) and `Apps/OZMA` (a menu entry for the stock OS).
4. Put the card back, turn the Brick on and start **OZMA** from the Apps menu.

| Brick OS | Status |
|---|---|
| spruce | supported |
| stock TrimUI OS / CrossMix | experimental |

Your songs live in `App/OZMA/data/Songs`. Put your own samples (WAV) in
`App/OZMA/data/Samples`; subfolders are fine.

To update, unzip the new release over the old one. Your songs and samples are not touched.

The full guide (studio mode, troubleshooting, removing OZMA) is on the OZMA website's
**Getting started** page. The link will be added here with the first release.

## Reporting bugs

During the beta, please report bugs in the OZMA Discord (`#bugs`). The invite link will be
added here with the first release. Attach `App/OZMA/log.txt` from the card if you can.

## License

Copyright © OZMA authors. All rights reserved.
You may download and use the released builds for free. You may not redistribute, modify or
reverse-engineer them unless a release note says otherwise.
