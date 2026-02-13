# NutriLog

A Progressive Web App (PWA) for personal nutrition and calorie tracking. Designed for iPhone, works offline, and can be installed as a standalone app on your home screen.

## Features

- **Quick Tap Logging**: Log most food items in 2-3 taps
- **Offline First**: All data stored locally using localStorage
- **Dark Theme**: Optimized for mobile viewing
- **PWA**: Install on your iPhone home screen for a native app experience
- **Smart Combos**: Pre-configured meals with adjustable components
- **Custom Entries**: Add your own food items on the fly
- **History Tracking**: View past days and 7-day rolling averages
- **Export**: Download your data as CSV or JSON

## Deployment to GitHub Pages

1. **Create a new GitHub repository**
   - Go to [github.com](https://github.com) and create a new repository
   - Name it something like `nutrilog`
   - Don't initialize with README (you already have one)

2. **Push the code**
   ```bash
   cd "/Users/rahul/Desktop/Personal/Nutrition logging app"
   git init
   git add .
   git commit -m "Initial commit: NutriLog PWA"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/nutrilog.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**
   - Go to your repository on GitHub
   - Click **Settings** → **Pages**
   - Under **Source**, select **Deploy from a branch**
   - Select branch **main** and folder **/ (root)**
   - Click **Save**

4. **Wait for deployment** (1-2 minutes)
   - GitHub will build and deploy your site
   - Your app will be available at: `https://YOUR_USERNAME.github.io/nutrilog/`

5. **Install on iPhone**
   - Open the GitHub Pages URL on your iPhone (Safari)
   - Tap the **Share** button (box with arrow)
   - Tap **"Add to Home Screen"**
   - Tap **Add**
   - Done! The NutriLog icon will appear on your home screen

## Local Testing

To test locally, you'll need a simple HTTP server (can't open index.html directly due to service worker restrictions):

```bash
# Using Python 3
python3 -m http.server 8000

# Then open http://localhost:8000 in your browser
```

## Updating the App

When you make changes and want to update the live version:

1. **Bump the cache version** in `sw.js`:
   ```javascript
   const CACHE_VERSION = 'v1.0.1'; // Increment this
   ```

2. **Push the changes**:
   ```bash
   git add .
   git commit -m "Update: description of changes"
   git push
   ```

3. **Wait 1-2 minutes** for GitHub Pages to rebuild

4. **On your iPhone**, open the app and refresh 1-2 times (the service worker will update in the background)

## Data Storage

All data is stored locally in your browser's localStorage:
- Today's log
- History of completed days
- Custom food items

**Important**: This data is tied to the browser. If you clear browser data or reinstall the app, you'll lose your data. Use the **Export** features regularly to back up your data.

## App Structure

- `index.html` - The entire app (HTML + CSS + JavaScript)
- `manifest.json` - PWA configuration
- `sw.js` - Service worker for offline caching
- `icon-192.png` & `icon-512.png` - App icons

## Technical Details

- **Framework**: Vanilla JavaScript (no dependencies, no build step)
- **Storage**: localStorage
- **Offline**: Service worker with stale-while-revalidate strategy
- **Style**: Mobile-first, dark theme, optimized for iPhone
- **Performance**: Loads instantly, works 100% offline after first load

## License

MIT - This is for personal use. Modify as needed!
