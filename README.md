# TimeFlow - Smart Timetable App v2.0

A comprehensive offline-first timetable management app with weekly templates, notifications, and progress tracking.

## 🆕 What's Fixed in v2.0

### Problem 1: ✅ FIXED - Different Schedules for Each Day
- **Before:** Tasks only showed on home screen after copying to all days
- **Now:** Each day has its own independent schedule
- Add tasks to Monday, Tuesday, etc. separately
- They automatically appear on the correct day
- "Copy to Days" feature is optional and selective
- Choose specific days to copy to, not forced to copy to all

### Problem 2: ✅ FIXED - True Standalone App
- **Before:** Opened in Chrome browser after installation
- **Now:** Opens as a real standalone app
- No browser UI or address bar
- Works completely offline
- Data persists like a native app
- Proper PWA configuration for Android

## 🌟 Features

### ✅ Core Features Implemented

1. **Weekly Template System**
   - Create a master timetable for each day of the week
   - Tasks automatically repeat every week
   - Easy editing and modification of templates
   - Copy schedule to all days with one click

2. **Today's Schedule**
   - View only today's tasks from your weekly template
   - Check off tasks as you complete them
   - Real-time progress tracking with circular indicator
   - Automatic missed task detection (shown in red)

3. **Smart Notifications**
   - Browser-based notifications using your system clock
   - Upload custom notification sounds from your phone's files
   - Set a default sound for all tasks in settings
   - Override default with custom sounds per task (optional)
   - Works completely offline once set up

4. **Progress Tracking**
   - Daily completion percentage with visual circle
   - Weekly progress view showing all 7 days
   - Monthly calendar with color-coded performance
   - Track completed, remaining, and missed tasks

5. **Widget Preview**
   - See how your widget would look
   - Interactive checkboxes that work in preview
   - Shows only incomplete tasks
   - Updates in real-time as you check tasks

6. **Complete Offline Support**
   - All data stored locally on your device
   - Works without internet connection
   - No server or cloud dependency
   - Install as standalone app on Android

7. **Beautiful Design**
   - Light and dark mode toggle
   - Smooth animations and transitions
   - Responsive design for all screen sizes
   - Clean, minimal interface

## 📱 Installing on Android

### Quick Start - 3 Steps:

1. **Deploy to Netlify:**
   - Rename `timeflow-app.html` to `index.html`
   - Upload `index.html`, `manifest.json`, `sw.js`, and `netlify.toml` to Netlify
   - Get your app URL (e.g., `https://timeflow.netlify.app`)

2. **Open on Phone:**
   - Open the URL in Chrome on your Android phone
   - You'll see an install prompt at the bottom

3. **Install:**
   - Tap "Install" or menu (⋮) → "Install app"
   - App appears on home screen
   - Opens as standalone app (no browser UI!)

### Detailed Deployment Guide

See **DEPLOYMENT.md** for complete step-by-step instructions including:
- Netlify deployment process
- PWA installation steps
- Troubleshooting common issues
- Making it feel like a native app
- Converting to APK (optional)

### Method 1: Install as PWA (Progressive Web App) - Recommended

1. **Using Chrome or Edge:**
   - Open `timeflow-app.html` in Chrome or Edge browser
   - Tap the menu (⋮) in the top-right
   - Select "Install app" or "Add to Home screen"
   - The app will be installed like a native app
   - You'll see an install prompt at the top of the app

2. **Access the installed app:**
   - Find "TimeFlow" icon on your home screen or app drawer
   - Tap to open - it runs fullscreen without browser UI
   - Works completely offline after installation

### Method 2: Create APK using Web2App Tools

If you need a traditional APK file:

1. **Use a web-to-APK converter:**
   - Use tools like [PWABuilder](https://www.pwabuilder.com/)
   - Or [AppsGeyser](https://appsgeyser.com/)
   - Upload the HTML file or host it online
   - Generate APK file

2. **Install the APK:**
   - Transfer APK to your phone
   - Enable "Install from unknown sources" in Settings
   - Tap the APK file to install

### Method 3: Bookmark Method (Basic)

1. Open `timeflow-app.html` in your mobile browser
2. Add to bookmarks or home screen
3. Access anytime - works offline

## 🎯 How to Use

### Initial Setup

1. **Set Up Notifications (Optional but Recommended)**
   - Click "Enable" on the notification banner
   - Grant notification permission when prompted
   - This allows the app to remind you of tasks

2. **Upload Default Sound (Optional)**
   - Click the ⚙️ Settings icon
   - Upload an audio file from your phone as default notification sound
   - This sound will play for all tasks unless you set custom sounds

3. **Create Your Weekly Template**
   - Go to "Weekly Template" tab
   - Select a day (Monday, Tuesday, etc.)
   - Click "+ Add Task"
   - Fill in task details:
     - Task name (e.g., "Morning Workout")
     - Start and end time
     - Duration
     - Optional: Upload custom notification sound for this specific task
   - **Repeat for each day** - each day can have different tasks!
   - **Optional:** Use "Copy to Days..." to duplicate a schedule to specific days
     - Select which days you want to copy to
     - Great for weekday routines that differ from weekends

### Daily Usage

1. **View Today's Schedule**
   - Open the app (or go to "Today" tab)
   - See all tasks scheduled for today from your weekly template
   - View your completion progress in the circular indicator

2. **Complete Tasks**
   - Check the box next to each task as you complete it
   - Progress updates automatically
   - Completed tasks appear faded with strikethrough
   - Missed tasks (past their end time) appear in red

3. **Track Progress**
   - Today: See real-time completion percentage
   - Weekly: View your performance for the current week
   - Monthly: See your productivity across the entire month

4. **Widget Preview**
   - Go to "Widget Preview" tab
   - See how your tasks would appear in a home screen widget
   - Check boxes work just like in the main view

### Notification Sounds

**Option 1: Use Default Sound for All Tasks**
1. Go to Settings (⚙️ icon)
2. Upload audio file as "Default Notification Sound"
3. All tasks will use this sound

**Option 2: Custom Sound Per Task**
1. When adding/editing a task in Weekly Template
2. Upload a custom sound file for that specific task
3. This overrides the default sound
4. Completely optional - leave blank to use default

**Audio File Support:**
- Supports: MP3, WAV, OGG, M4A
- Upload from your phone's local files
- Test sounds with the ▶️ play button
- Remove sounds with the 🗑️ delete button

## 🔧 Settings

Access settings by clicking the ⚙️ icon in the header:

- **Default Notification Sound**: Set a global sound for all tasks
- **Clear All Data**: Reset the app and delete all data (use with caution)

## 💡 Tips & Tricks

1. **Battery Optimization**: Ensure the app is excluded from battery optimization for reliable notifications
2. **Weekly Planning**: Set up your template once and forget it - tasks repeat automatically
3. **Flexible Completion**: You can check off tasks anytime, even before or after their scheduled time
4. **Dark Mode**: Perfect for nighttime planning
5. **Copy Schedule**: Use "Copy to All Days" to quickly set up a consistent routine
6. **Theme**: Toggle between light/dark mode with the 🌙/☀️ button

## 📊 Technical Details

- **Storage**: All data stored in browser localStorage (typically 5-10MB limit)
- **Offline First**: Works completely offline after initial load
- **No Account Required**: Everything stays on your device
- **Privacy**: No data sent to any server
- **Compatibility**: Works on Android 5.0+ (Chrome/Edge required for PWA install)

## 🐛 Troubleshooting

**Notifications not working:**
- Ensure you granted notification permission
- Check if browser notifications are enabled in Android settings
- Make sure the app isn't restricted by battery optimization

**Audio not playing:**
- Check your phone's volume settings
- Ensure audio file is in supported format (MP3, WAV, OGG)
- Try re-uploading the audio file
- Test with the play button in settings

**Can't install as app:**
- Make sure you're using Chrome or Edge browser
- Try the "Add to Home Screen" option from browser menu
- Some browsers may not fully support PWA installation

**Data not saving:**
- Ensure localStorage isn't disabled in browser settings
- Check available storage space on device
- Try clearing browser cache and reloading

**Widget not working:**
- The "Widget Preview" tab shows how a widget would work
- Actual home screen widgets require native app development
- For now, use the PWA installation for quick home screen access

## 🔄 Updates

To update the app:
1. Reload the page or clear cache
2. The service worker will update automatically
3. Your data is preserved during updates

## 📝 Data Backup

Since data is stored locally:
- No automatic cloud backup
- To backup: use browser's export feature or manually copy localStorage
- Clearing browser data will delete all tasks and templates

## 🎨 Customization

The app comes with:
- Light and Dark themes (toggle anytime)
- Customizable notification sounds
- Flexible task scheduling

---

**Version**: 2.0  
**Last Updated**: 2024

Enjoy staying organized with TimeFlow! 📅✨
