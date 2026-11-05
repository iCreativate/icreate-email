# Build and CI plan

## Phases

1. **Scaffold (this commit)** — docs, NOTICE, licence, icon brief; no Thunderbird tree yet.
2. **Import** — clone Thunderbird release tag into this repo (or git subtree); apply rebrand overlays.
3. **CI** — GitHub Actions matrix: Windows (MSI/NSIS), macOS (signed .app / DMG when team id exists),
   Linux (Flatpak or .deb/.rpm). Cache mozbuild toolchains.
4. **Alpha artifact** — publish GitHub Release with checksums.
5. **Catalogue** — only then set `email` status to `alpha` in `icreate-launcher/apps.json` with real
   `repo`, stems and bundle. Until step 5, launcher shows **Planned**.

## Local policy

Do not mark the catalogue installable without a working update source. A stub empty repo must not
unlock Install (maturity gate in the launcher already enforces this).
