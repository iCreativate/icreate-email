# Upstream sync (Thunderbird → iCreate Email)

Mirror the PhotoCraft pattern: keep a clear upstream remote, merge regularly, resolve
rebrand conflicts in branding-only paths first.

## Remotes (intended)

```text
origin    https://github.com/iCreativate/icreate-email.git
upstream  https://hg.mozilla.org/comm-central   # or the Git mirror used for the fork
```

Exact clone URL is chosen when the first full import lands (comm-central / thunderbird
release tag). Prefer a tagged Thunderbird release over arbitrary tip for reproducible builds.

## Sync loop

1. Fetch upstream release tag.
2. Merge into `main` (or `thunderbird-sync` then PR).
3. Re-apply branding overlays (`branding/`, icons, About, user-agent, update URL).
4. Re-run security defaults checklist (`docs/security.md`).
5. Build installers; smoke-test IMAP + Google OAuth + Microsoft OAuth on one platform each.
6. Publish GitHub Release only when artifacts are signed/notarized as required per platform.

## Do not

- Ship Mozilla update channels.
- Restore Thunderbird or Mozilla trademarks in UI or packages.
- Enable iCreate cloud mail sync by default.
