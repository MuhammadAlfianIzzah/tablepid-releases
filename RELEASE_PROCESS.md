# Release Process

How to release a new version of TablePID.

---

## Pre-Release Checklist

- [ ] All features tested
- [ ] No critical bugs
- [ ] Version number updated in `Cargo.toml`
- [ ] Version number updated in `package.json`
- [ ] CHANGELOG.md updated
- [ ] Documentation updated if needed

## Release Steps

### 1. Update Version

```toml
# src-tauri/Cargo.toml
[package]
version = "0.2.0"
```

```json
// package.json
{
  "version": "0.2.0"
}
```

### 2. Update CHANGELOG

Add new version entry to `release/CHANGELOG.md`:

```markdown
## [0.2.0] - 2026-06-01

### Added
- New features...

### Fixed
- Bug fixes...
```

### 3. Build Release

```bash
# Build for Windows
npm run tauri build
```

Output will be in `src-tauri/target/release/`:
- `tablepid.exe` - Application
- `bundle/msi/TablePID_0.2.0_x64_en-US.msi` - Installer

### 4. Test the Build

1. Install the MSI
2. Test all major features
3. Verify version number
4. Check for any issues

### 5. Create GitHub Release

1. Go to GitHub → Releases → New Release
2. Tag: `v0.2.0`
3. Title: `TablePID v0.2.0`
4. Description: Copy from CHANGELOG
5. Upload:
   - MSI installer
   - Any additional files

### 6. Update Website

Update download links on landing page:
- `web/index.html` - Update version number
- Update download button URL

### 7. Announce

Post announcement:
- GitHub Discussions
- Social media
- Dev communities

---

## Version Numbering

TablePID follows [Semantic Versioning](https://semver.org/):

- **Major** (1.0.0): Breaking changes
- **Minor** (0.1.0): New features, backward compatible
- **Patch** (0.1.1): Bug fixes, backward compatible

### Current Version: 0.1.0

---

## Hotfix Process

For critical bugs:

1. Create branch from release tag
2. Fix the bug
3. Bump patch version (0.1.0 → 0.1.1)
4. Build and test
5. Release immediately

---

## Release Schedule

- **Major releases**: Every 6-12 months
- **Minor releases**: Every 1-2 months
- **Patch releases**: As needed

---

## Questions?

Contact: hello@tablepid.dev
