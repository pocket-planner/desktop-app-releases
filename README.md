# Pocket Planner — Releases

This repository hosts the compiled distribution binaries, installers, and auto-update metadata for **Pocket Planner**, a minimal desktop application for weekly task planning and daily check-ins.

---

## Installation

### macOS (Via Homebrew)
You can easily install and update Pocket Planner on macOS using Homebrew:

```bash
# 1. Tap the repository
brew tap pocket-planner/tap

# 2. Install the app
brew install --cask pocket-planner
```

### macOS (Manual DMG)
1. Download the latest `.dmg` from the [Releases Page](https://github.com/pocket-planner/desktop-app-releases/releases/latest).
2. Open the `.dmg` file and drag **Pocket Planner** to your **Applications** folder.

> [!IMPORTANT]
> **macOS Security Gatekeeper Workaround:**
> Because this app is self-signed/unsigned, macOS may block it or claim the app is "damaged" on first launch. To resolve this, run the following command in your Terminal:
> ```bash
> xattr -cr "/Applications/Pocket Planner.app"
> ```

---

### Windows
1. Download the latest `.exe` installer (e.g., `Pocket-Planner-Setup-X.Y.Z.exe`) from the [Releases Page](https://github.com/pocket-planner/desktop-app-releases/releases/latest).
2. Run the installer to set up and launch Pocket Planner.

---

## Data Migration (from Weekly Planner)
If you are upgrading from the old **Weekly Planner** app on macOS and need to manually migrate your plans and settings:

1. Close both apps completely.
2. Open your Terminal and run:
   ```bash
   mkdir -p "~/Library/Application Support/pocket-planner"
   cp "~/Library/Application Support/weekly-planner/config.json" "~/Library/Application Support/pocket-planner/config.json"
   ```
3. Open **Pocket Planner** to view your migrated data.
