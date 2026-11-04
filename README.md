# tinkly — a puzzle journal

A mobile-first puzzle journal for everyone. Sign-up is required to save puzzles; every user sees only their own entries.

## Set up (about 15 minutes)

1. Create a free project at https://supabase.com/dashboard.
2. In **SQL Editor**, paste and run the entire `schema.sql` file. The row-level security policies protect each person's entries.
3. In **Authentication → Providers → Email**, enable email sign-up and email confirmation. For production, configure custom SMTP/email delivery; default email sending has limitations.
4. In **Project Settings → API** (or **Connect**), copy your project URL and **publishable/anon** key into `config.js`. **Never use a service_role or secret key in browser code.**
5. Upload all project files to a **public GitHub repository**. In repository **Settings → Pages**, select **Deploy from a branch**, `main`, `/ (root)` and save. Visit the GitHub Pages URL once deployment finishes.
6. In **Supabase → Authentication → URL Configuration**, set **Site URL** to your deployed GitHub Pages URL (with a trailing slash), and add the same URL under **Redirect URLs**. This is important for confirmation emails.
7. Create an account, confirm the email, log in, and log a test puzzle. Test a second account to verify it cannot see the first account's entries.

## Important notes

- GitHub Pages hosts the public frontend. Supabase handles account authentication and data storage.
- The Supabase URL and publishable key are safe to expose *only when database row-level security is correctly configured*. Never commit passwords or secret/service-role keys.
- The app works in desktop and mobile browsers. The manifest allows supported browsers to offer home-screen installation.
- This starter uses the Supabase JavaScript library via CDN, so the browser needs an internet connection.
- For a public launch, review abuse prevention, email delivery, privacy policy, accessibility, backups, and applicable data-protection obligations.
- `schema.sql` is intended for initial setup. Running it again after policies already exist may give duplicate-policy errors.
- Password-reset emails are supported, but this starter does not yet implement a dedicated new-password screen. Add one before public launch.
