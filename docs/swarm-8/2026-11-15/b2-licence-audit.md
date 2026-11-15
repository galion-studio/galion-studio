# Swarm 8 / B2 licence audit

Inspected 2026-11-15 with the GitHub API (pull request metadata, the pull request file list and patches, and `LICENSE` / `.gitignore` contents on each pull request head). No other repository was pushed, merged, or edited.

## Canonical text

The canonical licence is the file on `galion-studio/galion-one-voice` `main`, git blob `1d74abe087aab5dbfaaa0a48158030f4dd18408a`. It landed in merged pull request [galion-one-voice#127](https://github.com/galion-studio/galion-one-voice/pull/127) (`bce5e3a9688d71bb9b657cd19d1356de166ab68a`, merged 2026-11-14T19:36:08Z). `main` is 27 commits ahead of that commit and 0 behind, so the commit is still an ancestor of `main`, and the blob on `main` is the same.

That file is the standard MIT permission text, year 2026, with these four branding lines above it:

```
G.A.L.I.O.N. — General Autonomous Local Intelligence Open Network
Developed and distributed by Galion Labs
Perpetual Open MIT License
Copyright © 2026 Galion Labs. All rights reserved.
```

The MIT copyright line is exactly `Copyright (c) 2026 Maciej Grajczyk`. The string `FRXDEL STUDIOS` does not appear.

Two other default-branch files were read and not used as the canonical text:

- `galion-studio/galion-operating-system` `main`, blob `bf6f1fa137b13fbb93228ea73f57711642c75aad`, from merged pull request [galion-operating-system#9](https://github.com/galion-studio/galion-operating-system/pull/9) (merged 2026-11-14T18:57:38Z). Same four branding lines and the same MIT permission text, but the MIT line is `Copyright (c) 2026 Galion Labs`. That is the blob every draft below still points at. It is earlier than galion-one-voice#127 and does not name Maciej Grajczyk.
- `galion-studio/obsidian-open-mind` `main`, blob `127c2e723c261f488196baa498e09a7643842bd9`. No branding lines. The MIT line is `Copyright (c) 3000 Galion / galion-studio`. There is no `galion-operating-system/obsidian-open-mind` repository on the account that can see these repos; `galion-operating-system` and `obsidian-open-mind` are two repositories under `galion-studio`.

`matches canonical` below means the pull request head `LICENSE` blob is `1d74abe087aab5dbfaaa0a48158030f4dd18408a`.

## Pull requests

Every draft changes only `LICENSE` and `.gitignore`. No pull request removes a file. No patch contains a private-key block, a token prefix, or an IPv4 address. `FRXDEL STUDIOS` is absent from all seven head licences. The MIT year on every head is 2026.

| Repo | PR | Matches canonical | Exact problems | Suggested fix | Merge-ready |
| --- | --- | --- | --- | --- | --- |
| galion-studio | [#1](https://github.com/galion-studio/galion-studio/pull/1) | yes | Inspected head `f0ac8c2` (blob `bf6f1fa`) had `Copyright (c) 2026 Galion Labs` on the MIT line. This update replaces `LICENSE` with blob `1d74abe`. `.gitignore` was already the new 25-line file (blob `753d78f`): `.env`, `.env.*`, `*.pem`, `*.key`, `node_modules/`, `dist/`, `build/`, `target/`. Additions only; nothing deleted. Still a draft. | Done on this branch. Leave the draft open. | yes |
| community | [#1](https://github.com/galion-studio/community/pull/1) | no | Head `a56f40a`, draft, `mergeable_state` clean. `LICENSE` blob `bf6f1fa`: MIT line is `Copyright (c) 2026 Galion Labs`. The previous line was `Copyright (c) 2026 Galion Studio`. The MIT paragraphs were also rewrapped (4 deletions, 21 licence additions), so the pull request text that says the body is unchanged byte for byte is not true of the diff. The resulting permission text is the standard wrapped MIT text. New `.gitignore` blob `753d78f` covers `.env`, `*.pem`, `*.key`, `node_modules/`, `dist/`, `build/`, and `target/`. No file removed. | Replace `LICENSE` with blob `1d74abe` (MIT line `Copyright (c) 2026 Maciej Grajczyk`). Keep the `.gitignore`. | no |
| forge | [#1](https://github.com/galion-studio/forge/pull/1) | no | Head `1aa7179`, draft, `mergeable_state` clean. `LICENSE` blob `bf6f1fa`. The only licence deletion is `Copyright (c) 2026 galion-studio`, replaced by `Copyright (c) 2026 Galion Labs`. Resulting `.gitignore` (blob `1c05a27`) already had `.env`, `.env.*`, `*.pem`, `*.key`, `dist/`, `build/`, `target/`, and `**/target/`; the hunk adds `node_modules/` plus audio and model patterns. No file removed. | Replace `LICENSE` with blob `1d74abe`. Keep the `.gitignore`. | no |
| galion-marine | [#3](https://github.com/galion-studio/galion-marine/pull/3) | no | Head `99fd177`, draft, `mergeable_state` clean. `LICENSE` blob `bf6f1fa`. The only licence deletion replaces `Copyright (c) 2026 Maciej Grajczyk / Galion Studio` with `Copyright (c) 2026 Galion Labs`. `.gitignore` hunk adds `.env`, `.env.*`, `*.pem`, `*.key`, `node_modules/`, `dist/`, `build/`, and `target/` (head blob `b3cbff6`). No file removed. | Set the MIT line to exactly `Copyright (c) 2026 Maciej Grajczyk` (blob `1d74abe`). Keep the `.gitignore` additions. | no |
| Corpus-Nova | [#5](https://github.com/galion-studio/Corpus-Nova/pull/5) | no | Head `09797bf`, draft, `mergeable_state` clean. `LICENSE` blob `bf6f1fa`. The only licence deletion replaces `Copyright (c) 2026 Corpus Nova contributors` with `Copyright (c) 2026 Galion Labs`. Head `.gitignore` (blob `cac7674`) has `.env`, `.env.*`, `*.pem`, and `*.key` from the file already on `main`, and the hunk adds `node_modules/`, `dist/`, `build/`, and `target/`. No file removed. | Replace `LICENSE` with blob `1d74abe`. Keep the `.gitignore`. | no |
| Teglenica-TSO-36 | [#1](https://github.com/galion-studio/Teglenica-TSO-36/pull/1) | no | Head `14bf941`, draft, `mergeable_state` clean. `LICENSE` blob `bf6f1fa`. The only licence deletion replaces the correct line `Copyright (c) 2026 Maciej Grajczyk` with `Copyright (c) 2026 Galion Labs`. Head `.gitignore` (blob `8fce80f`) already had `.env`; the hunk adds `.env.*`, `*.pem`, `*.key`, `node_modules/`, `dist/`, `build/`, and `target/`. No file removed. | Restore the MIT line to `Copyright (c) 2026 Maciej Grajczyk` and add only the four branding lines (blob `1d74abe`). Keep the `.gitignore` additions. | no |
| hermes-research | [#1](https://github.com/galion-studio/hermes-research/pull/1) | no | Head `8b39189`, draft, `mergeable` false, `mergeable_state` dirty. `LICENSE` blob `bf6f1fa`. The licence hunk replaces `Copyright (c) 2026 Galion Studio` with `Copyright (c) 2026 Galion Labs`. The pull request `.gitignore` (blob `753d78f`) would cover `.env`, `*.pem`, `*.key`, `node_modules/`, `dist/`, `build/`, and `target/`, but `main` has moved. Compare of base `e204789` to `main` is ahead by 8 commits (through `ed3ce9993f`, 2026-11-15T00:38:47Z) and those commits add a different `.gitignore` (blob `e291fa1`) plus the research app. `main` `LICENSE` is already blob `bf6f1fa`. `main` `.gitignore` has `.env` and `node_modules/` and does not have `*.pem`, `*.key`, `dist/`, `build/`, or `target/`. No file is removed by the pull request diff itself. | Merge `main` into the pull request branch with a normal merge. Do not force-push and do not drop the files that landed on `main`. Then set `LICENSE` to blob `1d74abe`. Keep `main`'s `.gitignore` rules and add the missing `*.pem`, `*.key`, `dist/`, `build/`, and `target/` lines. | no |

## Merge-ready

Only [galion-studio#1](https://github.com/galion-studio/galion-studio/pull/1) matches the canonical licence and already has the required ignore rules, with no secret material and no deleted files. It is still a draft. The other six are not merge-ready. All six still carry `LICENSE` blob `bf6f1fa` (`Copyright (c) 2026 Galion Labs`). hermes-research#1 also conflicts with `main`.
