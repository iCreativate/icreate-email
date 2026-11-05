# iCreate Email

Desktop mail for the iCreate Work suite. **Foundation: Mozilla Thunderbird (MPL 2.0), fully rebranded.**

This repository is the fork pipeline home. Catalogue entry `email` stays **Planned** in the launcher until a real installer and update channel ship — there is no fake Install button.

## Status

| Item | Value |
|------|--------|
| Development status | Planned (scaffolding) |
| Licence (shipping binary) | MPL 2.0 for Thunderbird-derived files + iCreate additions (documented in `NOTICE`) |
| Bundle id (intended) | `za.co.icreativate.icreate-email` |
| Update source (intended) | GitHub Releases on `iCreativate/icreate-email` |

## Product requirements

IMAP, SMTP, Google and Outlook / Microsoft 365 accounts (OAuth where supported), Exchange/EWS where still viable with Graph prioritized, multiple identities, signatures, search, attachments, spam controls, OpenPGP/S/MIME, local/offline mail.

## Original UI and icon

Do **not** copy Thunderbird, Outlook or ArtCraft chrome. Slate-family icon and an original layout/theme. Placeholder catalogue icon lives in the launcher assets; product chrome is designed here before Alpha.

## Docs

- [Foundation decision](../docs/work/EMAIL_FOUNDATION.md)
- [Upstream sync](docs/upstream.md)
- [Security model](docs/security.md)
- [Rebrand checklist](docs/rebrand.md)
- [Build / CI plan](docs/build.md)

## Licence

See `LICENSE` and `NOTICE`. Thunderbird source remains under MPL 2.0. iCreate-owned files added beside it use MIT or Apache-2.0 where they are not derivative of MPL-covered files.
