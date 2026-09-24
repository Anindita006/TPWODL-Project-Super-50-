# Project SUPER 50 — GitHub + Supabase package

This package uses the supplied dashboard code as the base and keeps its dashboard UI/layout/data-processing behavior unchanged. Supabase is used only as the shared backend so uploaded datasets can be seen by other viewers.

## Files to upload to GitHub Pages
- `index.html`
- `config.js`

## One-time Supabase setup
Run `Supabase_Setup.sql` in the Supabase SQL Editor for the configured project.

## GitHub Pages
Create a repository, upload `index.html` and `config.js` to the repository root, then enable GitHub Pages from the `main` branch and `/ (root)`.

Do not upload Excel files to GitHub for routine dashboard updates.

## Important
The dashboard's existing upload password UI is retained. The Supabase table policy in this package permits browser clients using the publishable key to write dashboard data; this is intentional for preserving the existing upload flow without adding a new login screen or changing the dashboard UI. If stronger server-side administrator enforcement is required later, it should be added separately without changing the dashboard presentation.


FIX NOTE: This package fixes the Supabase viewer-load adapter so it reads the `payload` column used by `dashboard_data`. Replace the GitHub `index.html` with this version. `config.js` remains unchanged.

