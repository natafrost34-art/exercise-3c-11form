# Grammar Studio — Spotlight 11, Module 3

## Publish on Netlify
1. Upload this project to a new GitHub repository.
2. In Netlify choose **Add new site → Import an existing project** and select the repository.
3. Build settings: publish directory `public`; functions directory `netlify/functions` (already in `netlify.toml`).
4. In **Site configuration → Environment variables**, add:
   - `ADMIN_PASSWORD` — the teacher password supplied in the private setup chat.
   - `SESSION_SECRET` — generate a long random secret (at least 32 characters).
5. Deploy. Netlify Blobs stores student results and edited questions persistently across redeploys.

## Important
- Do not put the admin password in HTML, JavaScript, or Git.
- Netlify Blobs is provisioned automatically for deployed Netlify Functions.
- For local development, run `npm install` then `npx netlify dev`; configure the two environment variables in a local `.env` file (never commit it).
- The current exercise editor keeps the quiz at 15 items and requires four options per item; the six rule-check items are also selectable rule statements.
