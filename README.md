# Desk Alert Bridge — Frontend (Vercel static SPA)

Password-protected dashboard that mirrors phone notifications in real time via Supabase Realtime.

- Calls (`type: "CALL"`) flash red with a pulse and a short beep until you click the card.
- Tab title shows `(X New) Desk Alert Bridge`; favicon shows the count badge.
- "Clear history" deletes all rows through the backend.

## Setup
1. Deploy the backend repo first and note its URL.
2. Edit `config.js`: `SUPABASE_URL`, `SUPABASE_ANON_KEY`, `BACKEND_URL`.
3. Run the SQL from the backend repo (`supabase.sql`) so the anon key can only SELECT (needed for Realtime).
4. Import this repo into Vercel (framework: Other, no build). Optionally set backend `ALLOWED_ORIGIN` to this site's URL.

Local: `npx serve .`
