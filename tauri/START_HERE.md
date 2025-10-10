# START HERE - Sortes Astrampsychi

Welcome to the Sortes Astrampsychi project! This guide will help you get started quickly.

## What is This?

Sortes Astrampsychi is a desktop application that brings the ancient Greek oracle divination system to your computer. Consult the oracle by selecting from 103 traditional questions and receive mystical answers displayed on an authentic parchment background.

## Quick Start Guide

### For Users (Just Want to Use the App)

1. **Download** the installer for your platform from the releases page
2. **Install** by running the installer
3. **Launch** the Sortes Astrampsychi application
4. **Select** a question from the dropdown menu
5. **Click** "Answer" to receive your oracle response
6. **Toggle** dark mode using the switch in the top-right corner

### For Developers (Want to Build or Modify)

#### First Time Setup

1. **Install Prerequisites**
   - Node.js (v16+): https://nodejs.org/
   - Rust: https://rustup.rs/
   
2. **Open Terminal** in the project directory

3. **Run Quick Development**
   ```batch
   quick-dev.bat
   ```
   
   The application will open automatically with hot-reload enabled.

#### Making Changes

- **Frontend**: Edit files in `src/` folder
  - `src/index.html` - Main application interface
  - Inline CSS and JavaScript included
  
- **Backend**: Edit files in `src-tauri/src/` folder
  - `src-tauri/src/main.rs` - Rust entry point
  
- **Configuration**: Edit `src-tauri/tauri.conf.json`

Changes to frontend files will automatically reload in development mode.

#### Building Installers

```batch
quick-build.bat
```

Find installers in: `src-tauri/target/release/bundle/`

## Project Structure

```
sortes-astrampsychi/
├── src/                    # Frontend (HTML, CSS, JS, images)
├── src-tauri/             # Backend (Rust, Tauri config)
├── quick-dev.bat          # Start development
├── quick-build.bat        # Build installers
└── README.md              # Full documentation
```

## Key Features

✨ **103 Oracle Questions** - Authentic ancient Greek divination questions  
🎨 **Parchment Display** - Answers shown on beautiful parchment background  
🌙 **Dark Mode** - Toggle between light and dark themes  
📖 **Help System** - Built-in documentation about the oracle  
💾 **Offline** - Works completely offline after installation  
🖥️ **Cross-Platform** - Windows, macOS, and Linux support

## Common Tasks

### Development Mode
```batch
quick-dev.bat
```

### Build for Production
```batch
quick-build.bat
```

### Clean Build (if issues occur)
```bash
npm cache clean --force
rm -rf node_modules
npm install
```

## Need Help?

- **Full Documentation**: See [README.md](README.md)
- **Build Instructions**: See [BUILD_INSTRUCTIONS.md](BUILD_INSTRUCTIONS.md)
- **Project Details**: See [PROJECT_SUMMARY.md](PROJECT_SUMMARY.md)

## Troubleshooting

### "Rust not found"
Install Rust from https://rustup.rs/

### "Node not found"
Install Node.js from https://nodejs.org/

### Build fails
1. Run `npm cache clean --force`
2. Delete `node_modules` folder
3. Run `npm install` again
4. Try building again

### Application won't start
- Check that all dependencies are installed
- Try running `quick-dev.bat` to see error messages
- Ensure no other instance is running

## What's Next?

1. **Try the App**: Run `quick-dev.bat` to see it in action
2. **Explore Code**: Look at `src/index.html` to see how it works
3. **Make Changes**: Modify the oracle questions or answers
4. **Build**: Create your own installer with `quick-build.bat`

## Contributing

Improvements welcome! Consider:
- Adding more oracle questions
- Creating custom icons
- Enhancing the UI
- Adding new features
- Improving documentation

---

**Ready to Begin?**

Run `quick-dev.bat` and start exploring! 🚀

**Questions?** Check the other documentation files or open an issue.
