# Project Summary - Sortes Astrampsychi

## Overview

Sortes Astrampsychi is a desktop application that brings the ancient Greek oracle divination system to modern computers. Built with Tauri, it provides an authentic oracle consultation experience with over 100 traditional questions and mystical answers.

## Project Information

- **Name**: Sortes Astrampsychi
- **Version**: 1.0.0
- **Type**: Desktop Application (Cross-platform)
- **Framework**: Tauri 2.0
- **License**: MIT
- **Author**: Radius.Center

## Technology Stack

### Frontend
- **HTML5**: Structure and content
- **CSS3**: Styling with dark mode support
- **JavaScript**: Interactive functionality and oracle logic
- **Assets**: Parchment background image, favicon, help documentation

### Backend
- **Rust**: Core application logic
- **Tauri 2.0**: Desktop application framework
- **Cargo**: Rust package manager and build system

### Build Tools
- **npm**: Package management
- **Tauri CLI**: Application bundling and building
- **Rust Compiler**: Backend compilation

## Features

### Core Functionality
1. **Oracle Consultation**
   - 103 traditional Greek oracle questions
   - Random mystical answer generation
   - Authentic parchment display for answers

2. **User Interface**
   - Clean, intuitive dropdown question selection
   - Answer button for oracle consultation
   - Reset button to start new consultation
   - Dark mode toggle for comfortable viewing

3. **Help System**
   - Built-in help documentation
   - Information about the oracle's history
   - Usage instructions

4. **Persistence**
   - Dark mode preference saved locally
   - Offline operation after installation

## Project Structure

```
sortes-astrampsychi/
├── src/                          # Frontend source files
│   ├── index.html               # Main application HTML
│   ├── parchment.png            # Answer background image
│   ├── favicon.ico              # Application icon
│   ├── help.html                # Help documentation
│   └── help_files/              # Help documentation assets
├── src-tauri/                   # Tauri backend
│   ├── src/
│   │   ├── main.rs             # Rust entry point
│   │   └── lib.rs              # Library code
│   ├── icons/                   # Application icons
│   ├── capabilities/            # Permission configuration
│   ├── Cargo.toml              # Rust dependencies
│   ├── tauri.conf.json         # Tauri configuration
│   └── build.rs                # Build script
├── package.json                 # npm configuration
├── quick-dev.bat               # Development script
├── quick-build.bat             # Build script
├── README.md                    # Project documentation
├── BUILD_INSTRUCTIONS.md        # Build guide
└── .gitignore                  # Git ignore rules
```

## Key Components

### Oracle System
- **Questions Database**: 103 authentic ancient Greek oracle questions
- **Answer Pool**: Traditional mystical responses
- **Random Selection**: JavaScript-based random answer generation
- **Display System**: Parchment-styled answer presentation

### User Interface
- **Question Selector**: Dropdown menu with all oracle questions
- **Answer Display**: Parchment background with centered text
- **Theme Toggle**: Light/dark mode switch
- **Help Access**: Quick access to documentation

### Configuration
- **Window Settings**: 1000x800 default, resizable, centered
- **Bundle Targets**: MSI, NSIS, DEB, RPM, DMG, APP
- **Permissions**: Core defaults + shell:allow-open
- **Asset Protocol**: Enabled for local file access

## Development Workflow

### Setup
1. Install Node.js and Rust
2. Clone repository
3. Run `npm install`

### Development
1. Run `quick-dev.bat` or `npm run dev`
2. Application opens with hot-reload
3. Make changes to frontend files
4. Changes reflect automatically

### Building
1. Run `quick-build.bat` or `npm run build`
2. Installers created in `src-tauri/target/release/bundle/`
3. Test installer on target platform

## Build Outputs

### Windows
- MSI installer (Windows Installer)
- NSIS installer (Nullsoft Scriptable Install System)

### Linux
- DEB package (Debian/Ubuntu)
- RPM package (Fedora/RHEL)

### macOS
- DMG disk image
- APP bundle

## Performance Characteristics

- **Bundle Size**: ~5-10 MB (platform-dependent)
- **Memory Usage**: ~50-100 MB
- **Startup Time**: < 2 seconds
- **Build Time**: 2-5 minutes

## Security Features

- Sandboxed execution environment
- Limited system permissions
- No network access required
- Local data storage only

## Future Enhancements

Potential improvements:
- Custom icon design specific to oracle theme
- Additional oracle questions
- Answer history tracking
- Export consultation results
- Multiple language support
- Sound effects for mystical atmosphere

## Dependencies

### Frontend
- No external JavaScript libraries (vanilla JS)
- Self-contained HTML/CSS

### Backend
- tauri: ^2.0.0
- tauri-plugin-shell: ^2.0.0
- serde: ^1.0
- serde_json: ^1.0

### Development
- @tauri-apps/cli: ^2.0.0
- Node.js: >=16
- Rust: latest stable

## Maintenance

### Regular Tasks
- Update dependencies periodically
- Test on all target platforms
- Monitor for Tauri framework updates
- Review and update documentation

### Known Limitations
- Icons are placeholder (from photo-reader template)
- Help documentation is basic
- No answer history feature
- Single language (English) only

## Contact & Support

- **Developer**: Radius.Center
- **Repository**: [Add repository URL]
- **Issues**: [Add issues URL]
- **Website**: https://radius.center

---

**Last Updated**: 2025
**Status**: Production Ready
