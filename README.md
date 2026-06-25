# clawx-cdn

ClawX CDN repository for auto-updates and hot updates.

## Directory Structure

```
clawx-cdn/
├── win/           # Windows update packages
│   ├── latest.yml # Auto-update manifest
│   └── clawx-*.zip
└── asar/          # Hot update resources
    ├── version.json # Version info for hot updates
    └── app-*.asar   # Application ASAR files
```

## Auto-update

Auto-update uses electron-updater and checks `win/latest.yml` for new versions.

## Hot-update

Hot-update checks `asar/version.json` for new ASAR versions and only updates the application code without reinstalling the entire app.