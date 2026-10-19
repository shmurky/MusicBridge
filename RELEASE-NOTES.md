# MusicBridge 0.3.3 — Artwork fix (Preview)

Download **MusicBridge-0.3.3-universal.dmg** below. Quit MusicBridge, open the disk image, replace the app in Applications, and reopen it. Your settings are preserved.

## Fixed

- Searches public Apple Music album pages for streaming releases missing from the iTunes catalog, including ADL.
- Caches matching album tracks in memory so subsequent songs can reuse their artwork immediately.
- Improves matching for collaborations, accented titles, featured artists, and Single/EP labels while preserving live/remix/deluxe distinctions.
- Adds fallback search variants and retries unsuccessful matches sooner.
- Removes the large Apple Music logo used when no cover was found. The app now reports that the album cover is not available yet.

The first lookup still depends on network response time and catalog availability. Local-only artwork is not uploaded.

## Install

Requires macOS 13 or later, desktop Discord, and a Discord Application ID (see README). Universal Apple Silicon/Intel build; Intel has not been tested on hardware.

This preview is signed ad hoc and **not notarized by Apple**. macOS may block it because the developer is not verified.

SHA-256 checksums are provided in **SHA256SUMS.txt**. GitHub's automatic source archives contain public documentation only; application source remains private.
