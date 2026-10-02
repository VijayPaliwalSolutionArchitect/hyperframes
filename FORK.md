# Why SHIVAM ITCS maintains this fork

This repository is a **source-preserving, rebranded fork** of
[`heygen-com/hyperframes`](https://github.com/heygen-com/hyperframes), maintained by
**SHIVAM ITCS** (https://shivamitcs.in). This document records the *rationale* for the
fork — the *provenance* and licence obligations are recorded separately in
[`NOTICE.md`](NOTICE.md) and [`LICENSE`](LICENSE).

## What HyperFrames is

HyperFrames is an open-source framework that turns HTML, CSS, media and seekable
animations into **deterministic MP4 video**. It runs a headless browser plus an FFmpeg
`image2pipe` pipeline, and ships first-class support for AI coding agents via installable
skills. In short: *write HTML, render video, built for agents.*

That is directly relevant to how SHIVAM ITCS builds agentic systems — an agent that can
produce a deterministic, pixel-stable media artefact from declarative markup is a
capability worth holding close rather than reaching for over the network every time.

## Why this fork exists

1. **A stable reference pin.** Upstream `main` moves fast. This fork holds a known-good,
   self-hosted copy of the engine inside the SHIVAM ITCS organisation, so the rendering
   layer can be inspected, built and referenced without depending on upstream's release
   cadence or network availability.
2. **Architecture evaluation.** It gives SHIVAM ITCS a controlled copy to study the
   deterministic-render pipeline (headless capture, frame ordering, FFmpeg muxing) as a
   candidate rendering core for agent-native media pipelines.
3. **Licence hygiene by construction.** Keeping a first-class copy of an Apache-2.0
   dependency, with its provenance and notices intact, is a standing reminder of how
   third-party open source is expected to be consumed inside the firm.

## What this fork proves

- **Disciplined open-source intake** — imports are made from a pinned source tarball, not
  by scraping a moving branch, and the upstream origin is named explicitly.
- **Licence and attribution respect** — the Apache 2.0 licence and all upstream credits
  are preserved unchanged; see [`CREDITS.md`](CREDITS.md) and [`NOTICE.md`](NOTICE.md).
- **Rebrand without vandalism** — the site branding and package metadata carry the SHIVAM
  ITCS identity, while upstream source code is left functionally intact so the engine can
  still be compared and updated against its origin.

## What this fork is *not*

- It is **not affiliated with, endorsed by, or supported by HeyGen**. Upstream support
  channels do not apply here.
- It is **not a redistribution product**. It is an internal reference and evaluation copy.
- It does **not claim upstream work as SHIVAM ITCS work.** All upstream authorship remains
  recognised; SHIVAM ITCS's contribution is the intake, branding and the documentation in
  this repository.

## Keeping it honest

Only these changes are made to upstream, and they are logged in [`NOTICE.md`](NOTICE.md):

- removal of build artefacts and local development environments from the source import;
- addition of `NOTICE.md`, this `FORK.md`, and SHIVAM ITCS branding in `README.md` and
  package metadata;
- everything else is upstream, unchanged.

To update from upstream, diff against the tracked origin before importing — do not edit
upstream code in place here.

## Contact

**SHIVAM ITCS** — https://shivamitcs.in · MD@ShivamITConsultancy.com
