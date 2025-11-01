# EarnWale Setup Guide

## ✅ What's Been Created

Your modern rummy affiliate website is ready with:

1. **Homepage** (`/`) - Beautiful hero section with animated background and game cards
2. **Admin Panel** (`/admin`) - Manage games and view statistics
3. **API Routes** - RESTful API with Hono for game management and click tracking
4. **Database** - MongoDB with Prisma ORM, already seeded with 6 sample games

## 🚀 Quick Start

The development server is already running at:
- **Local**: http://localhost:3000
- **Admin**: http://localhost:3000/admin

## 📁 Project Structure

```
earnwale/
├── app/
│   ├── api/[[...route]]/route.ts  # API endpoints (Hono)
│   ├── admin/page.tsx              # Admin dashboard
│   ├── page.tsx                    # Homepage
│   ├── layout.tsx                  # Root layout
│   └── globals.css                 # Global styles
├── lib/
│   └── prisma.ts                   # Prisma client
├── prisma/
│   ├── schema.prisma               # Database schema
│   └── seed.ts                     # Sample data
└── .env                            # Environment variables
```

## 🎨 Features

### Homepage
- Animated gradient hero section
- Responsive game cards with hover effects
- Star ratings and bonus displays
- Click tracking for affiliate links
- Mobile-friendly design

### Admin Panel
- View all games in a table
- Manage game listings
- Track performance

### API Endpoints
- `GET /api/games` - List all games
- `GET /api/games/:id` - Get single game
- `POST /api/clicks` - Track affiliate clicks

## 🔧 Available Commands

```bash
npm run dev      # Start development server
npm run build    # Build for production
npm run start    # Start production server
npm run db:push  # Push schema to database
npm run db:seed  # Seed database with sample data
```

## 🎯 Next Steps

1. **Customize Games**: Edit `prisma/seed.ts` and run `npm run db:seed`
2. **Update Affiliate Links**: Replace example.com URLs with real affiliate links
3. **Add Real Images**: Upload images to Vercel Blob or use your own CDN
4. **Customize Design**: Edit colors and styles in `app/globals.css`
5. **Deploy**: Push to GitHub and deploy on Vercel

## 🌐 Deployment to Vercel

1. Push your code to GitHub
2. Import project in Vercel
3. Add environment variables:
   - `DATABASE_URL`
   - `MONGODB_URI`
   - `BLOB_READ_WRITE_TOKEN`
4. Deploy!

## 📝 Environment Variables

Already configured in `.env`:
- MongoDB connection for database
- Vercel Blob token for image storage

## 🎮 Sample Games Included

1. RummyCircle - ₹2000 bonus
2. Junglee Rummy - ₹5250 bonus
3. Ace2Three - ₹1500 bonus
4. KhelPlay Rummy - ₹2500 bonus
5. Classic Rummy - ₹3000 bonus
6. RummyBaazi - ₹4000 bonus

## 💡 Tips

- Update affiliate URLs in the database to your actual affiliate links
- Use high-quality images for better conversion
- Monitor clicks through the admin panel
- Add more games by creating them through the API or database

## 🆘 Support

If you need to restart the dev server:
```bash
npm run dev
```

Visit http://localhost:3000 to see your site!
