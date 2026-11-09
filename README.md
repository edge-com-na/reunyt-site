# reunyt-site

Static pages for reunyt.com, served by GitHub Pages. No build step and no framework: edit the HTML and push to `main`.

| Path | Purpose |
|---|---|
| `/` | Home: coming soon, how it works, privacy, finders, alerts |
| `/support/` | Support and FAQ. The App Store support URL |
| `/partners/` | For organisations (shelters, vets, lost-property desks) |
| `/privacy/` | Privacy Policy. The App Store privacy policy URL. Keep it in line with what the app and database actually collect and keep (retention periods come from the migrations' purge jobs). Update the effective date whenever the text changes |
| `/terms/` | Terms of Use. Update the effective date whenever the text changes |
| `/confirmed/` | Landing page after a user taps the email confirmation link. Supabase's Site URL points here. Shows an "expired link" message when Supabase adds `error` / `error_code` to the URL |
| `/404.html` | Not found |

## Shared parts

- `assets/site.css` holds the design tokens (Reunyt teal and mint, from the design system) and every style. Light mode only for now.
- Every page repeats the same header and footer. When you change one, change it on all seven pages.
- Fonts: Museo Sans from the Adobe Fonts kit `akp5rmp` (reunyt.com must be in the kit's allowed domains), falling back to the system font.
- Favicons and `site.webmanifest` come from the brand package.
- No cookies, no analytics and no third-party scripts apart from the font kit. Pages work without JavaScript; only `/confirmed/` uses a small script.

## Content rules

- Plain, calm and kind, in British spelling, with no exclamation marks.
- Only claims that are true of the app today. Label anything planned "Coming next" or "Later".
- Nothing suggests a partnership with the police or a ministry.
- No personal names.

Later: the notify-me form, `/f/RY-…` share links and `/.well-known/apple-app-site-association` (universal links).
