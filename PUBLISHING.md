# Publishing rules for this repository

This repository is **public**. It holds release downloads and user-facing text only.
OZMA's source code lives elsewhere and is never published here.

## Allowed files (whitelist)

Only these paths may exist in this repository:

| Path | What it is |
|---|---|
| `README.md` | Short install summary, links |
| `CHANGELOG.md` | User-facing release notes |
| `PUBLISHING.md` | This file |
| `.github/ISSUE_TEMPLATE/*.yml` | Bug report form |
| `update/latest.json` | Update manifest: newest version, zip URL, size, sha256 (a `.sig` signature is added with the in-app update feature) |
| `media/screenshots/*.png`, `media/*.png` | Screenshots taken from a released build, and artwork from the OZMA brand |

Release zips and their `.sha256` files are **not committed**. They are attached to GitHub
Releases (tag `v<version>`), named `OZMA-<version>.zip` and `OZMA-<version>.zip.sha256`.

## Releasing a new version

1. The zip comes only from the packaging gate (`zip_gate: PASS`) and has passed a Brick run.
2. GitHub: new release, tag `v<version>`, title `OZMA <version>`, attach `OZMA-<version>.zip` and its `.sha256`;
   tick "pre-release" for betas. Check the asset digest shown by GitHub matches the `.sha256`.
3. itch.io: upload the same zip to https://orumet.itch.io/ozma.
4. Update `CHANGELOG.md` (new section on top, with the sha256) and `update/latest.json` (version, url, size,
   sha256) in one commit.
5. If the README status line or screenshots changed, update them in the same commit.

## Never publish

- Source code of any kind, build scripts, tests, emulator tools.
- Internal docs: plans, QA reports, decisions, handoffs, agent notes.
- Samples that are not cleared for redistribution, and any local sample paths or folder names.
- The USB kernel module or any other GPL component (needs its own source offer first).
- Signing keys, tokens, passwords, device addresses, private logs.

## Before every push

1. `git remote -v` must show `github.com/Manticorees/ozma`. If not, stop.
2. `git ls-files` must list only whitelisted paths.
3. Read the full diff (`git diff --cached`). Nothing from "Never publish" may appear.
4. For a release: the zip is the approved final candidate, its sha256 matches, and it was
   checked for private paths and unshippable files before upload.
