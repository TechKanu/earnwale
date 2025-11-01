# EarnWale - Rummy Affiliate Platform

A modern affiliate website for rummy gaming platforms built with Next.js, Prisma, MongoDB, and Hono.

## Features

- 🎮 Beautiful hero section with animated background
- 🎯 Game cards showcasing different rummy platforms
- 💰 Signup bonus information
- ⭐ Rating system
- 📊 Click tracking for affiliate links
- 🚀 Fast API with Hono
- 💾 MongoDB database with Prisma ORM
- 🎨 Tailwind CSS for styling

## Tech Stack

- **Framework**: Next.js 16 (App Router)
- **Database**: MongoDB with Prisma
- **API**: Hono
- **Styling**: Tailwind CSS
- **Icons**: Lucide React
- **Image Storage**: Vercel Blob

## Getting Started

### Prerequisites

- Node.js 18+ installed
- MongoDB database (MongoDB Atlas recommended)

### Installation

1. Clone the repository and navigate to the project:
```bash
cd earnwale
```

2. Install dependencies:
```bash
npm install
```

3. Environment variables are already set in `.env`:
```env
DATABASE_URL="mongodb+srv://..."
MONGODB_URI="mongodb+srv://..."
BLOB_READ_WRITE_TOKEN="vercel_blob_rw_..."
```

4. Push the database schema:
```bash
npm run db:push
```

5. Seed the database with sample games:
```bash
npm run db:seed
```

6. Run the development server:
```bash
npm run dev
```

7. Open [http://localhost:3000](http://localhost:3000) in your browser

## API Routes

- `GET /api/hello` - Test endpoint
- `GET /api/games` - Get all games
- `GET /api/games/:id` - Get single game
- `POST /api/clicks` - Track affiliate clicks

## Project Structure

```
earnwale/
├── app/
│   ├── api/
│   │   └── [[...route]]/
│   │       └── route.ts      # Hono API routes
│   ├── globals.css           # Global styles
│   ├── layout.tsx            # Root layout
│   └── page.tsx              # Home page
├── lib/
│   └── prisma.ts             # Prisma client
├── prisma/
│   ├── schema.prisma         # Database schema
│   └── seed.ts               # Database seeder
└── .env                      # Environment variables
```

## Deployment

Deploy to Vercel:

```bash
vercel
```

Make sure to add environment variables in Vercel dashboard.

## License

MIT
