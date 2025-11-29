# Portfolio Deployment Guide

## ✅ Setup Complete!

Your portfolio is now configured with Vite and ready for deployment to Vercel.

## 📂 Project Structure

```
Portfolio/
├── index.html       # Main portfolio (v1 - Comic theme)
├── v2.html         # Alternative portfolio version
├── package.json    # Dependencies & scripts
├── vite.config.js  # Multi-page configuration
├── vercel.json     # Deployment settings
└── README.md       # Full documentation
```

## 🚀 Quick Start

### Local Development
```bash
npm run dev
```
Visit: http://localhost:5173/

### Build for Production
```bash
npm run build
```
Output will be in the `dist/` folder.

## 🌐 Deploy to Vercel

### Method 1: Vercel CLI (Fastest)
```bash
# Install Vercel CLI
npm install -g vercel

# Deploy
vercel

# Deploy to production
vercel --prod
```

### Method 2: Git + Vercel Dashboard (Recommended for CI/CD)

1. **Initialize Git & Push to GitHub:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Portfolio with Vite"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/portfolio.git
   git push -u origin main
   ```

2. **Deploy on Vercel:**
   - Go to https://vercel.com/new
   - Import your GitHub repository
   - Vercel will auto-detect Vite
   - Click "Deploy"
   - Done! Your site will be live in ~30 seconds

### Method 3: Drag & Drop

1. Build your project: `npm run build`
2. Go to https://vercel.com/new
3. Drag the `dist/` folder to the upload area
4. Deploy!

## 🔧 Environment Variables (if needed)

Create a `.env` file in the root:
```
VITE_API_URL=your_api_url
```

Then access in your code:
```js
const apiUrl = import.meta.env.VITE_API_URL
```

## 📱 URLs After Deployment

- Main page: `https://your-project.vercel.app/`
- Version 2: `https://your-project.vercel.app/v2.html`

## 🎯 Next Steps

1. ✅ Development server is running (check terminal)
2. 🔄 Make changes and see live updates
3. 🚀 When ready, deploy to Vercel
4. 🎨 Optionally add custom domain in Vercel dashboard

## 💡 Tips

- **Custom Domain**: Add in Vercel Dashboard → Settings → Domains
- **Analytics**: Enable Vercel Analytics for free traffic insights
- **Preview Deployments**: Every git push creates a preview URL
- **Rollbacks**: Instant rollback to any previous deployment

## 🐛 Troubleshooting

**Dev server not starting?**
```bash
# Kill any process on port 5173
npx kill-port 5173
npm run dev
```

**Build errors?**
- Ensure all HTML files are in the root directory
- Check `vite.config.js` for correct file paths

**Deployment issues?**
- Verify `vercel.json` settings
- Check build logs in Vercel dashboard

---

**Ready to deploy?** Run `vercel` in your terminal! 🚀

