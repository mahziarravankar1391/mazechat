# NovaChat

NovaChat is a clean, GitHub-ready React + TypeScript web messenger foundation.

## Important
This repository contains **no fake users, fake conversations, fake messages, or seeded demo content**.

The application starts empty until a real user creates an account and configures Supabase.

## Stack
- React
- TypeScript
- Vite
- Supabase Auth
- Supabase PostgreSQL
- Supabase Realtime
- Supabase Storage

## Run

1. Install Node.js 20+.
2. Copy `.env.example` to `.env`.
3. Add your Supabase project URL and anon key.
4. Run:

```bash
npm install
npm run dev
```

## Supabase setup

Open the SQL editor in your Supabase project and run:

`supabase/schema.sql`

The schema creates the required tables, indexes, triggers and RLS policies.

Then create these Storage buckets:
- avatars
- chat-attachments
- group-images
- channel-images
- voice-messages

Keep private buckets private.

## Environment variables

```env
VITE_SUPABASE_URL=
VITE_SUPABASE_ANON_KEY=
```

Never put a Supabase service-role key in the browser.

## GitHub Pages

GitHub Pages is static hosting. The app can be deployed there, but authentication and realtime data still come from Supabase.

For a Vite project hosted at `https://USERNAME.github.io/REPOSITORY/`, set the Vite `base` value in `vite.config.ts` to `/REPOSITORY/`.

A host with SPA fallback, such as Vercel or Netlify, is simpler for client-side routing.

## No fictional content

The UI uses empty states such as "No conversations yet." It does not pre-populate fictional accounts or messages.
