# Deploying Tide/Light to Vercel

## Prerequisites
- GitHub account
- Vercel account (free at vercel.com)
- Git installed on your computer

## Step 1: Push to GitHub

1. **Initialize Git repository** (if not already done):
   ```powershell
   cd c:\tidelight
   git init
   git add .
   git commit -m "Initial commit: Tide/Light blog"
   ```

2. **Create a new repository on GitHub**:
   - Go to github.com and create a new repository
   - Name it something like `tidelight-blog`
   - Don't initialize with README (you already have files)

3. **Push your code to GitHub**:
   ```powershell
   git remote add origin https://github.com/YOUR_USERNAME/tidelight-blog.git
   git branch -M main
   git push -u origin main
   ```

## Step 2: Deploy to Vercel

### Option A: Using Vercel Website (Easiest)

1. Go to [vercel.com](https://vercel.com) and sign up/login
2. Click "Add New Project"
3. Import your GitHub repository
4. Vercel will auto-detect it's a static site
5. Click "Deploy"
6. Done! Your site will be live at `your-project.vercel.app`

### Option B: Using Vercel CLI

1. **Install Vercel CLI**:
   ```powershell
   npm install -g vercel
   ```

2. **Login to Vercel**:
   ```powershell
   vercel login
   ```

3. **Deploy**:
   ```powershell
   cd c:\tidelight
   vercel
   ```

4. Follow the prompts:
   - "Set up and deploy"? → Y
   - "Which scope"? → Select your account
   - "Link to existing project"? → N
   - "What's your project's name"? → tidelight (or your choice)
   - "In which directory is your code located"? → ./
   - Want to modify settings? → N

5. **Deploy to production**:
   ```powershell
   vercel --prod
   ```

## Step 3: Custom Domain (Optional)

1. In Vercel dashboard, go to your project
2. Settings → Domains
3. Add your custom domain
4. Follow DNS configuration instructions

## Important Notes

### Before Deploying:
- ✅ All placeholder "coming soon" posts are ready
- ✅ vercel.json is configured for clean URLs
- ✅ All links use relative paths (will work on any domain)
- ⚠️ The `/about` link will 404 until you create that page

### After Deploying:
- Test all three blog cards from landing page
- Test theme switching (click "Tide" or "Light")
- Verify "coming soon" posts open correctly
- When you write your first real post, just:
  1. Replace the dummy blog file
  2. Update the listing page
  3. Git commit and push
  4. Vercel auto-deploys!

## Updating Your Site

Every time you make changes:
```powershell
git add .
git commit -m "Your update message"
git push
```

Vercel will automatically rebuild and deploy your site!

## Troubleshooting

**Images not loading?**
- They're using Unsplash URLs, which should work fine
- If issues occur, download images and put in an `images/` folder

**Links broken?**
- All links use relative paths and should work
- The `/about` link needs a page created

**Theme not persisting?**
- localStorage works on Vercel, no issues expected

## Your Site is Ready! 🎉

Once deployed, share your URL and start writing your first real blog post today!
