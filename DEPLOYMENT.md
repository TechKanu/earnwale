# Deployment Checklist

## Pre-Deployment

- [x] Database schema created and pushed
- [x] Sample data seeded
- [x] Environment variables configured
- [x] API routes tested
- [x] Frontend components working

## Vercel Deployment Steps

### 1. Push to GitHub

```bash
git add .
git commit -m "Initial commit: EarnWale rummy affiliate site"
git remote add origin YOUR_GITHUB_REPO_URL
git push -u origin main
```

### 2. Import to Vercel

1. Go to https://vercel.com
2. Click "Add New Project"
3. Import your GitHub repository
4. Configure project settings

### 3. Add Environment Variables

In Vercel dashboard, add these environment variables:

```
DATABASE_URL=mongodb+srv://Vercel-Admin-test:EThpo1em6LmNqCGe@test.e9mpzij.mongodb.net/earnwale?retryWrites=true&w=majority

MONGODB_URI=mongodb+srv://Vercel-Admin-test:EThpo1em6LmNqCGe@test.e9mpzij.mongodb.net/?retryWrites=true&w=majority

BLOB_READ_WRITE_TOKEN=vercel_blob_rw_8hCeE0FxpTEaifte_ji0FypdaVgKbUeq3Lpx65KZbuCfMyc
```

### 4. Deploy

Click "Deploy" and wait for the build to complete.

### 5. Post-Deployment

After deployment, you may need to:

1. Run database migrations (Vercel will run `prisma generate` automatically)
2. Seed the production database if needed
3. Test all API endpoints
4. Verify affiliate links work correctly

## Custom Domain (Optional)

1. Go to your project settings in Vercel
2. Navigate to "Domains"
3. Add your custom domain
4. Update DNS records as instructed

## Monitoring

- Check Vercel Analytics for traffic
- Monitor API response times
- Track affiliate click conversions
- Review error logs in Vercel dashboard

## Updates

To update your site:

```bash
git add .
git commit -m "Your update message"
git push
```

Vercel will automatically redeploy.

## Important Notes

- Replace example.com affiliate URLs with real ones
- Update game images with high-quality assets
- Add proper legal pages (Privacy Policy, Terms)
- Consider adding authentication for admin panel
- Set up proper error tracking (Sentry, etc.)

## Support

For issues:
- Check Vercel deployment logs
- Verify environment variables
- Test API endpoints locally first
- Check MongoDB connection
