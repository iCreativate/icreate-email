# iCreate Email — security model

## Credentials

- Account passwords and OAuth refresh tokens are stored only in the OS keychain (preferred) or the
  client’s encrypted password database (Thunderbird NSS/SQLite path after rebrand).
- Paths and algorithms are documented in the in-app About / Security notes before Alpha ships.
- Credentials are never uploaded to iCreate servers by default.

## Mail content

- Message bodies, headers, attachments and address books stay on the device and the user’s mail
  providers (IMAP/SMTP/Graph/etc.).
- No “phone home” of mail content to iCreate for analytics, training or sync unless the user later
  enables an explicit opt-in product with a separate consent UI and design review.

## Telemetry

- Mozilla telemetry and studies are disabled or gated off in branded builds by default.
- No iCreate install or usage telemetry that includes mail content.
- Crash reporting, if enabled later, must strip account identifiers and message data; off by default
  until reviewed.

## Updates

- Updates come from iCreativate-signed GitHub Releases (or a signed CDN you control).
- Mozilla’s Balrog / Mozilla update endpoints are not used for iCreate Email packages.

## Network

- Direct connections only to user-configured mail providers and OAuth endpoints.
- No hidden iCreate relay for send/receive in the default product.
