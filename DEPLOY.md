# Quick Deployment Guide

## What I Need From You

1. **Your GitHub username** (e.g., `yourname`)
2. **GitHub Personal Access Token** (for pushing code)
   - Go to: https://github.com/settings/tokens
   - Click "Generate new token (classic)"
   - Give it a name like "NutriLog Deploy"
   - Check the "repo" checkbox
   - Click "Generate token"
   - **Copy the token** (it looks like `ghp_xxxxxxxxxxxx`)
   - Save it somewhere safe (you can't see it again!)

## What I'll Do

Once you give me:
- Your GitHub username
- The personal access token

I'll run these commands for you:

```bash
cd "/Users/rahul/Desktop/Personal/Nutrition logging app"

# Initialize git
git init
git add .
git commit -m "Initial commit: NutriLog PWA

Co-Authored-By: Claude Sonnet 4.5 <noreply@anthropic.com>"

# Create repo on GitHub (using gh CLI if available, or manual instructions)
# Push to GitHub
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/nutrilog.git
git push -u origin main
```

Then I'll guide you through enabling GitHub Pages in the repo settings.

## Alternative: Manual Setup (No Token Needed)

If you prefer to do it yourself:

1. Go to https://github.com/new
2. Create a new repository named `nutrilog`
3. Don't initialize with README
4. Copy the commands shown and paste them in Terminal

Then I can help you with the GitHub Pages setup!

## After Deployment

Once the site is live at `https://YOUR_USERNAME.github.io/nutrilog/`:

1. Open that URL on your iPhone (in Safari)
2. Tap the Share button (box with arrow pointing up)
3. Scroll down and tap "Add to Home Screen"
4. Tap "Add"
5. The NutriLog icon will appear on your home screen!

## Updating Later

When you want to update the app:

```bash
cd "/Users/rahul/Desktop/Personal/Nutrition logging app"
git add .
git commit -m "Update: description of what changed"
git push
```

Wait 1-2 minutes, then refresh the app on your iPhone 1-2 times.
