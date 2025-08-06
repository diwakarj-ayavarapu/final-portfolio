# Netlify Deployment Guide

## Quick Deploy Steps

### Method 1: Drag & Drop (Easiest)
1. Go to [netlify.com](https://netlify.com)
2. Sign up/login with GitHub
3. Drag the entire `Portfolio-Website` folder to the deploy area
4. Your site will be live instantly!

### Method 2: GitHub Integration (Recommended)
1. Push your `Portfolio-Website` folder to a GitHub repository
2. Go to [netlify.com](https://netlify.com)
3. Click "New site from Git"
4. Connect your GitHub account
5. Select your repository
6. Build settings:
   - Build command: (leave empty)
   - Publish directory: (leave empty or use `.`)
7. Click "Deploy site"

### Method 3: Netlify CLI (Advanced)
```bash
npm install -g netlify-cli
cd "Diwakar's Portfolio/Portfolio-Website"
netlify deploy --prod --dir .
```

## Configuration Files Created
- ✅ `netlify.toml` - Main configuration with security headers and redirects
- ✅ `_redirects` - SPA routing support

## Site Settings
- **Build Command**: None (static site)
- **Publish Directory**: `.` (root)
- **Functions Directory**: Not needed

## Custom Domain (Optional)
1. Go to Site Settings → Domain Management
2. Add custom domain
3. Update DNS records as instructed

## Environment Variables (If needed)
Add in Netlify Dashboard → Site Settings → Environment Variables:
- `EMAILJS_PUBLIC_KEY` - For contact form
- Any other API keys

## Troubleshooting
- **404 on refresh**: The `_redirects` file handles this
- **Assets not loading**: Check all paths use `./` relative format
- **Contact form**: Ensure EmailJS configuration is correct

## Performance Optimizations
- ✅ Security headers configured
- ✅ Asset caching enabled
- ✅ SPA routing configured
- ✅ Gzip compression enabled by default

Your portfolio is now ready for Netlify deployment! 🚀
