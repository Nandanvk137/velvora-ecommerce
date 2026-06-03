# PulseMetrics — SaaS Dashboard

Full-stack SaaS dashboard built with **Next.js 14**, **TypeScript**, **Tailwind CSS**, **shadcn/ui**, **MongoDB**, **Prisma**, **NextAuth**, **Zustand**, **React Hook Form**, **Zod**, and **Recharts**.

## Features

- Landing page, auth (login/register)
- Protected dashboard with sidebar
- Projects CRUD with search & filters
- Analytics charts (Recharts)
- Profile & settings pages
- Dark/light mode, toasts, loading & error states

## Prerequisites

- Node.js 18+
- MongoDB Atlas or local MongoDB

## Setup

```bash
git clone <your-repo-url>
cd saas-dashboard
cp .env.example .env.local
# Edit DATABASE_URL and NEXTAUTH_SECRET
npm install
npx prisma generate
npx prisma db push
npm run db:seed
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

**Demo login:** `demo@pulsemetrics.com` / `password123`

## Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Development server |
| `npm run build` | Production build |
| `npm run start` | Start production |
| `npm run db:push` | Sync Prisma schema |
| `npm run db:seed` | Seed demo data |

## Deploy (Vercel)

1. Push to GitHub
2. Import project in [Vercel](https://vercel.com)
3. Set environment variables: `DATABASE_URL`, `NEXTAUTH_URL`, `NEXTAUTH_SECRET`
4. Build command: `prisma generate && next build`
5. Install command: `npm install`

Set `NEXTAUTH_URL` to your production domain.

## ZIP / GitHub upload

```powershell
cd C:\Users\nanda\Projects
Compress-Archive -Path saas-dashboard -DestinationPath saas-dashboard.zip
```

Exclude `node_modules` and `.next` before zipping (or use `.gitignore` and push to GitHub).

## Folder structure

```
app/          # Routes (pages, API)
components/   # UI, layout, forms, charts
hooks/        # useProjects, useDebounce
lib/          # auth, prisma, validations
prisma/       # schema, seed
store/        # Zustand
types/        # Shared TS types
utils/        # constants, api-handler
```

## Tech stack

Next.js 14 App Router · TypeScript · Tailwind · shadcn/ui · MongoDB · Prisma · NextAuth · Zustand · RHF + Zod · Recharts
