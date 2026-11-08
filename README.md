# reunyt-site

Static pages for reunyt.com, served by GitHub Pages.

| Path | Purpose |
|---|---|
| `/` | Holding page |
| `/confirmed/` | Landing page after a user taps the email confirmation link. Supabase's Site URL points here. Shows an "expired link" message when Supabase adds `error` / `error_code` to the URL. |
| `/terms/` | Terms of Use. Linked from the holding page. Update the effective date at the top whenever the text changes. |
| `/privacy/` | Privacy Policy. Linked from the holding page and the Terms. Keep it in line with what the app and database actually collect and keep (retention periods come from the migrations' purge jobs). |
| `/404.html` | Not found |

Later additions: `/support` (required for App Store submission) and `/.well-known/apple-app-site-association` (universal links).

No build step: edit the HTML and push to `main`.
