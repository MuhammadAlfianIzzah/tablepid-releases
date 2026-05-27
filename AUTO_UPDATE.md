# Auto Update Guide

How TablePID handles updates.

---

## Current Update Strategy

TablePID currently uses **manual updates**. Users check GitHub Releases for new versions.

## Checking for Updates

Users can check for updates by:
1. Visiting the GitHub Releases page
2. Comparing their version with the latest release
3. Downloading the new installer if available

## Future: Auto-Update

### Planned Implementation

TablePID will implement auto-update using Tauri's built-in updater:

```json
{
  "updater": {
    "active": true,
    "dialog": true,
    "pubkey": "YOUR_PUBLIC_KEY",
    "endpoints": [
      "https://tablepid.dev/updates/{{target}}/{{current_version}}"
    ]
  }
}
```

### Update Flow

1. App checks for updates on startup
2. If update available, shows notification
3. User can choose to update now or later
4. Downloads update in background
5. Installs on restart

### Security

- Updates are signed with Ed25519
- Signature verification before install
- HTTPS-only update endpoints

---

## For Developers

### Creating an Update

1. Build the new version
2. Sign the update with your private key
3. Upload to GitHub Releases
4. Update the update manifest

### Update Manifest

```json
{
  "version": "0.2.0",
  "notes": "Bug fixes and improvements",
  "pub_date": "2026-06-01T00:00:00Z",
  "platforms": {
    "windows-x86_64": {
      "signature": "SIGNATURE_HERE",
      "url": "https://github.com/tablepid/tablepid/releases/download/v0.2.0/tablepid_0.2.0_x64.msi.zip.sig"
    }
  }
}
```

---

## Questions?

Open an issue on GitHub or contact: hello@tablepid.dev
