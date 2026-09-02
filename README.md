# KNHS DocumentTrack V5 — GitHub Pages Edition

## What this is
A static HTML/CSS/JavaScript frontend designed for GitHub Pages. GitHub Pages can publish static files directly from a repository.

## Current database mode
The included site uses browser localStorage, so it works immediately after publishing. This is NOT a shared multi-user database.

## Recommended production architecture
GitHub Pages = frontend
Supabase/Firebase = shared database + authentication + file storage

Do not put confidential school records or passwords into a public GitHub repository.

## Publish
1. Create/open your GitHub Pages repository.
2. Upload `index.html` to the publishing source (usually repository root).
3. In Settings > Pages, choose Deploy from a branch, select your branch and `/(root)`, then Save.
4. Open the generated github.io URL.

## Important
If the repository is `USERNAME.github.io`, the site URL is `https://USERNAME.github.io/`.
If it is a project repository, the URL is `https://USERNAME.github.io/REPOSITORY/`.

## Shared database
V5 is intentionally prepared so the dashboard and registry can be switched from localStorage to a cloud database. Before doing that, provide the Supabase project URL and public anon key (never provide a service-role key). The database schema should include documents, document_movements, users/roles, and audit_logs, with Row Level Security enabled.
