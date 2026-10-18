# SkyWorld Online Shop (customer site only)

This is the website for buyers. It contains no owner portal files.

## Deploy on GitHub Pages
1. Upload everything in this folder to the ROOT of a new GitHub repository.
2. Repo -> Settings -> Pages -> Source: `main` branch, `/ (root)`. Your shop will be at `https://<you>.github.io/<repo>/`.

## Connect it to the owner portal (so orders reach the owners)
1. Supabase: SQL Editor -> paste `setup.sql` -> Run (only once, skip if the owner site was already set up).
2. Supabase: Project Settings -> API -> copy the Project URL and the `anon public` key.
3. Open `shared/config.js` and paste them into `supabaseUrl` and `supabaseKey`. Use the SAME values as the owner site.
4. Commit. Orders, stock, and reviews are now shared with the owner portal on any device.

Direct link to one stall: `https://<you>.github.io/<repo>/#/s/5` (stall 5).
Leave the keys empty only for local testing (data stays in that one browser).
