# 🚀 Risen Lord Beneficiary System

**Next.js 16 + Prisma + Next-Auth + PostgreSQL** — full-stack beneficiary & program management SaaS.

![Naruto Yell GIF](Naruto_Yell_GIF_by_Xbox.gif)

## Tech Stack

| Category | Technology |
|---|---|
| **Frontend** | Next.js 16 (App Router), React 19, TypeScript |
| **Styling** | Tailwind CSS 4, Emotion, MUI 7 (Data Grid, Date Pickers) |
| **Icons** | @iconify/react (+ 12 icon sets) |
| **Backend** | Next.js API Routes, Next-Auth 4, Prisma 6 |
| **Database** | PostgreSQL |
| **Validation** | Zod, React Hook Form, @hookform/resolvers |
| **Date/Time** | Dayjs, date-fns |
| **Tooling** | Turbopack, ESLint, tsx, Prisma Migrate/Seed |

## Local Development

```bash
npm install
cp .env.example .env  # set DATABASE_URL to your Postgres URL
npx prismagenerate
npx prismamigrate dev
npm run dev
```

### Demo Seed Users
- `admin@risenlord.local` / `admin123` (ADMIN)
- `caseworker@risenlord.local` / `caseworker123` (CASEWORKER)
- `director@risenlord.local` / `director123` (PROJECT_DIRECTOR)

## Permission Model

| Role | Permissions |
|---|---|
| CASEWORKER | beneficiary, activity, participation, transaction, development + read |
| PROJECT_DIRECTOR | program:write, activity:write, audit:read |
| ADMIN | all + user:manage |

## License

MIT
