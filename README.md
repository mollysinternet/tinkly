# tinkly — a puzzle journal

A mobile-first puzzle journal for everyone. Sign-up is required to save puzzles; every user sees only their own entries.

## Important notes

- GitHub Pages hosts the public frontend. Supabase handles account authentication and data storage.
- The Supabase URL and publishable key are safe to expose *only when database row-level security is correctly configured*. Never commit passwords or secret/service-role keys.
- The app works in desktop and mobile browsers. The manifest allows supported browsers to offer home-screen installation.
- This starter uses the Supabase JavaScript library via CDN, so the browser needs an internet connection.
- For a public launch, review abuse prevention, email delivery, privacy policy, accessibility, backups, and applicable data-protection obligations.
- `schema.sql` is intended for initial setup. Running it again after policies already exist may give duplicate-policy errors.
- Password-reset emails are supported, but this starter does not yet implement a dedicated new-password screen. Add one before public launch.
