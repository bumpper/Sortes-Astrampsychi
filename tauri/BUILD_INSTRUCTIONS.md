# Build Instructions - Sortes Astrampsychi

Complete guide for building the Sortes Astrampsychi desktop application.

## Prerequisites

### Required Software

1. **Node.js** (v16 or higher)
   - Download from: https://nodejs.org/
   - Verify installation: `node --version`

2. **Rust** (latest stable)
   - Download from: https://rustup.rs/
   - Verify installation: `rustc --version`

3. **npm** (comes with Node.js)
   - Verify installation: `npm --version`

### Platform-Specific Requirements

#### Windows
- Visual Studio C++ Build Tools
- WebView2 (usually pre-installed on Windows 10/11)

#### macOS
- Xcode Command Line Tools: `xcode-select --install`

#### Linux
- Development packages:
  ```bash
  sudo apt-get update
  sudo apt-get install -y libwebkit2gtk-4.0-dev \
    build-essential \
    curl \
    wget \
    libssl-dev \
    libgtk-3-dev \
    libayatana-appindicator3-dev \
    librsvg2-dev
  ```

## Quick Build Methods

### Method 1: Quick Build Script (Windows)

```batch
quick-build.bat
```

This script will:
1. Install npm dependencies
2. Build the application
3. Create installers in `src-tauri/target/release/bundle/`

### Method 2: Manual Build

```bash
# Install dependencies
npm install

# Build the application
npm run build
```

## Development Mode

### Quick Development (Windows)

```batch
quick-dev.bat
```

### Manual Development

```bash
# Install dependencies (first time only)
npm install

# Start development server
npm run dev
```

The application will open with hot-reload enabled. Changes to the frontend will automatically refresh.

## Build Outputs

After a successful build, installers will be located in:

```
src-tauri/target/release/bundle/
├── msi/          # Windows MSI installer
├── nsis/         # Windows NSIS installer
├── deb/          # Linux Debian package
├── rpm/          # Linux RPM package
├── dmg/          # macOS disk image
└── macos/        # macOS app bundle
```

## Build Targets

### Windows

```bash
npm run build:windows
```

Creates:
- MSI installer (recommended)
- NSIS installer

### Linux

```bash
npm run build:linux
```

Creates:
- DEB package (Debian/Ubuntu)
- RPM package (Fedora/RHEL)

### macOS

```bash
npm run build:macos
```

Creates:
- DMG disk image
- APP bundle

## Troubleshooting

### Common Issues

#### 1. Rust Not Found
```
Error: Rust installation not found
```
**Solution**: Install Rust from https://rustup.rs/

#### 2. WebView2 Missing (Windows)
```
Error: WebView2 not found
```
**Solution**: Download and install WebView2 Runtime from Microsoft

#### 3. Build Dependencies Missing (Linux)
```
Error: Package 'libwebkit2gtk-4.0-dev' not found
```
**Solution**: Install required packages (see Linux prerequisites above)

#### 4. Permission Denied
```
Error: EACCES: permission denied
```
**Solution**: Run with appropriate permissions or fix npm permissions

### Clean Build

If you encounter persistent issues:

```bash
# Clean npm cache
npm cache clean --force

# Remove node_modules
rm -rf node_modules

# Remove Cargo build artifacts
cd src-tauri
cargo clean
cd ..

# Reinstall and rebuild
npm install
npm run build
```

## Build Configuration

### Customizing the Build

Edit `src-tauri/tauri.conf.json` to customize:
- Application name and version
- Window size and behavior
- Bundle settings
- Icons and resources

### Release Optimization

The release build is optimized for size and performance:
- Dead code elimination
- Link-time optimization (LTO)
- Binary stripping
- Size optimization (`opt-level = "s"`)

## Verification

After building, test the installer:

1. Locate the installer in `src-tauri/target/release/bundle/`
2. Install the application
3. Launch and verify all features work correctly
4. Test dark mode toggle
5. Verify help documentation loads
6. Test oracle question selection and answers

## Next Steps

- See [README.md](README.md) for usage instructions
- See [PROJECT_SUMMARY.md](PROJECT_SUMMARY.md) for project overview
- Report issues or contribute improvements

---

**Build Time**: Typical build takes 2-5 minutes depending on your system.

**Installer Size**: Approximately 5-10 MB depending on platform.
