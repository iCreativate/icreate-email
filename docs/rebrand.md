# Rebrand checklist (Thunderbird → iCreate Email)

Complete before any public Alpha installer.

## Identity

- [ ] Product name: **iCreate Email** everywhere (window title, About, installers, Start Menu, .desktop).
- [ ] Bundle / AppUserModelID: `za.co.icreativate.icreate-email`.
- [ ] Asset stem: `email-*` or `icreate-email-*` (match launcher `apps.json` when flipping to Alpha).
- [ ] User-agent / client id strings do not say Thunderbird or Mozilla as the product name.

## Visual

- [ ] Original Slate icon (envelope motif on slate field — see `branding/`); no Thunderbird bird.
- [ ] Splash / about logo: iCreate Email, not ArtCraft or Mozilla.
- [ ] Theme / chrome: original layout; do not clone Thunderbird three-pane defaults or Outlook ribbon.
- [ ] Remove Mozilla/Thunderbird start page promo chrome that implies endorsement.

## Legal

- [ ] `NOTICE` and `LICENSE` ship in the installer and About → Licence.
- [ ] about:license (or equivalent) lists MPL 2.0 for modified files.
- [ ] No “official Thunderbird” or “Mozilla approved” wording.

## Channels

- [ ] Update URL points at iCreativate releases.
- [ ] Telemetry prefs default off (`docs/security.md`).
