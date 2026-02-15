# TimeFlow - Deployment Guide for Netlify

## 🚀 Quick Deployment Steps

### Step 1: Prepare Your Files
Make sure you have these 3 files in a folder:
1. `timeflow-app.html` (rename to `index.html`)
2. `manifest.json`
3. `sw.js`

### Step 2: Rename the HTML File
**IMPORTANT:** Rename `timeflow-app.html` to `index.html`

Your folder structure should be:
```
your-folder/
├── index.html
├── manifest.json
└── sw.js
```

### Step 3: Deploy to Netlify

#### Option A: Drag and Drop (Easiest)
1. Go to [netlify.com](https://netlify.com)
2. Sign up or log in
3. Drag your folder to the deploy zone
4. Wait for deployment to complete
5. You'll get a URL like: `https://your-app-name.netlify.app`

#### Option B: GitHub Deploy
1. Create a GitHub repository
2. Upload all files (index.html, manifest.json, sw.js)
3. Connect repository to Netlify
4. Deploy automatically

### Step 4: Configure Netlify (Important!)

Create a file named `netlify.toml` in your folder with this content:

```toml
[[redirects]]
  from = "/*"
  to = "/index.html"
  status = 200

[[headers]]
  for = "/manifest.json"
  [headers.values]
    Content-Type = "application/manifest+json"

[[headers]]
  for = "/sw.js"
  [headers.values]
    Content-Type = "application/javascript"
    Service-Worker-Allowed = "/"

[[headers]]
  for = "/*"
  [headers.values]
    X-Frame-Options = "DENY"
    X-Content-Type-Options = "nosniff"
```

This ensures:
- Proper MIME types for PWA files
- Service worker can control all pages
- Security headers are set

### Step 5: Test PWA Installation

After deployment:
1. Open your Netlify URL on your Android phone in Chrome
2. You should see an install prompt
3. Tap "Install" or go to menu (⋮) → "Install app"
4. The app icon appears on your home screen
5. Open it - it should work as a standalone app!

## 📱 Installing on Android Phone

### Method 1: Chrome Browser (Recommended)
1. Open your Netlify URL in Chrome: `https://your-app.netlify.app`
2. Wait for the install banner to appear at the bottom
3. Tap "Install" or "Add to Home Screen"
4. The app installs and appears on your home screen
5. Open it from home screen - it works offline!

### Method 2: Manual Installation
1. Open the URL in Chrome
2. Tap the menu button (⋮) in the top-right
3. Select "Install app" or "Add to Home screen"
4. Confirm the installation
5. App appears on home screen

### Method 3: Settings Menu
1. Open the app in Chrome
2. Go to app settings (look for install icon in address bar)
3. Tap "Install"

## 🔧 Troubleshooting

### Problem 1: "Opens in Browser Instead of App"

**Solution:**
1. **Check if actually installed:** Look for TimeFlow icon in app drawer (not just home screen bookmark)
2. **Reinstall:**
   - Uninstall the current version
   - Clear Chrome cache: Settings → Privacy → Clear browsing data
   - Visit the URL again
   - Install fresh using Chrome's install prompt
3. **Check manifest.json:** Make sure `"display": "standalone"` is set
4. **Use HTTPS:** Netlify provides HTTPS automatically - make sure you're using the https:// URL

### Problem 2: "Install Prompt Doesn't Appear"

**Causes & Solutions:**
- **Already installed:** Check app drawer - might already be installed
- **Browser issue:** Try Chrome Beta or Edge browser
- **Cache issue:** Clear Chrome cache and revisit
- **PWA criteria not met:** Check browser console for errors

### Problem 3: "App Doesn't Work Offline"

**Solutions:**
1. Open the app at least once while online
2. Service worker needs initial registration
3. Check browser console for service worker errors
4. Try reinstalling the app

### Problem 4: "Tasks Not Showing for Each Day"

**Solution:**
This is now fixed! Make sure you're using the latest version:
1. Add tasks to each day separately in "Weekly Template"
2. Tasks will automatically show on their respective days
3. No need to copy to all days unless you want to

### Problem 5: "Data Not Persisting"

**Check:**
1. Browser isn't in incognito mode
2. Storage isn't full (Settings → Storage)
3. Chrome isn't set to clear data on exit
4. App has storage permissions

## 🎯 Verification Checklist

After installation, verify these work:
- [ ] App opens from home screen (not in browser)
- [ ] No browser address bar visible
- [ ] Status bar color matches app theme (teal)
- [ ] Works completely offline
- [ ] Can add tasks to each day separately
- [ ] Today tab shows current day's tasks
- [ ] Notifications work (after granting permission)
- [ ] Audio uploads work
- [ ] Dark mode toggle works
- [ ] Weekly template saves properly

## 📊 Making It Feel Like a Native App

### What Makes It App-Like:
✅ **Standalone display mode** - No browser UI
✅ **Custom splash screen** - Shows TimeFlow branding
✅ **Theme color** - Matches Android navigation
✅ **App icon** - Shows in app drawer and home screen
✅ **Offline functionality** - Works without internet
✅ **Local storage** - Data persists like native apps

### What's Different from Native:
❌ Can't be published to Play Store (use PWABuilder to convert)
❌ No access to advanced Android APIs
❌ Widget must be previewed in-app (not on home screen)

## 🔄 Updating the App

When you make changes:
1. Upload new files to Netlify
2. Users will get updates automatically when they open the app
3. Service worker updates in background
4. May need to close and reopen app to see changes

## 💾 Data & Privacy

**Good news:**
- All data stored locally on user's device
- No data sent to any server
- Works completely offline
- No analytics or tracking
- Privacy-first design

**User should know:**
- Clearing Chrome data will delete app data
- Uninstalling removes all tasks and templates
- No cloud backup (intentional for privacy)
- Can't sync across devices

## 🆘 Still Having Issues?

### Check These:
1. **Using HTTPS URL?** (Netlify provides this automatically)
2. **Chrome version updated?** (Update from Play Store)
3. **Storage space available?** (Check phone storage)
4. **Using correct URL?** (Not localhost or IP address)

### Debug Mode:
1. Open app in Chrome
2. Go to `chrome://inspect/#service-workers`
3. Find your app
4. Check for errors

### Fresh Start:
1. Uninstall app completely
2. Clear Chrome cache
3. Restart phone
4. Visit URL and install again

## 📱 Making It Even Better

### Optional Enhancements:

1. **Custom Domain:**
   - Buy domain from Namecheap/Google Domains
   - Connect to Netlify
   - Users access via your-app.com

2. **Convert to APK:**
   - Use [PWABuilder](https://www.pwabuilder.com/)
   - Upload your Netlify URL
   - Download APK
   - Distribute to users

3. **Analytics (Optional):**
   - Add Google Analytics to track usage
   - See how many users install

## 🎉 Success!

Once deployed and installed correctly:
- Opens like a real app (no browser UI)
- Works offline perfectly
- Data persists across restarts
- Feels native and fast
- Each day has its own unique schedule
- Copy function available for convenience

Your app is now ready for daily use! 📅✨

---

**Need Help?**
Check the README.md for detailed feature documentation.
