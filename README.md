# Free AI — Vercel-ready

This version replaces local SQLite with PostgreSQL so user accounts and settings persist on Vercel.

## Required Vercel environment variables
DATABASE_URL — PostgreSQL connection string.
AUTH_SECRET — long random secret.
ADMIN_EMAIL — first/admin account email.
ADMIN_PASSWORD — first/admin account password.

Optional AI variables:
AI_API_URL
AI_API_KEY
AI_MODEL

Deploy this folder as a Next.js project. Add the environment variables in Vercel Project Settings → Environment Variables, then redeploy. Vercel supports Next.js with zero-config deployment. A PostgreSQL database can be connected through Vercel Marketplace storage integrations.

Admin: log in with ADMIN_EMAIL/ADMIN_PASSWORD. The Admin button appears only for the admin role. The `/api/admin/*` endpoints independently reject non-admin sessions with 403.
