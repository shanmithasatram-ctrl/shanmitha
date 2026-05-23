# Allo Inventory Reservation System

A Next.js based inventory reservation platform that prevents overselling during checkout by temporarily reserving stock units.

## Features

- Product inventory management
- Warehouse-wise stock tracking
- Temporary inventory reservations
- Reservation confirmation
- Reservation cancellation/release
- Automatic reservation expiry
- Concurrency-safe reservation logic
- REST APIs using Next.js App Router
- Prisma + PostgreSQL integration

## Tech Stack

- Next.js 14
- TypeScript
- Prisma ORM
- PostgreSQL
- Tailwind CSS

## Setup Instructions

### Install Dependencies

```bash
npm install
```

### Configure Environment Variables

Create a `.env` file:

```env
DATABASE_URL="your_postgresql_database_url"
```

### Generate Prisma Client

```bash
npx prisma generate
```

### Run Migration

```bash
npx prisma migrate dev --name init
```

### Run Application

```bash
npm run dev
```

Open:
http://localhost:3000

## API Endpoints

- GET /api/products
- GET /api/warehouses
- POST /api/reservations
- POST /api/reservations/:id/confirm
- POST /api/reservations/:id/release

## Concurrency Handling

Prisma transactions are used to avoid race conditions.

## Reservation Expiry

Reservations automatically expire after 10 minutes.

## Deployment

- Vercel
- Supabase / Neon

## Author

Shanmitha Satram
