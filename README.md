# Pholdr
 
A small desktop app for copying and renaming files in bulk, with a thumbnail-grid file browser and automatic folder organization.
 
![Python](https://img.shields.io/badge/python-3.8%2B-blue)
![Platform](https://img.shields.io/badge/platform-Windows-lightgrey)

### 👉 [Download the latest version](https://github.com/RicFausto/Pholdr/releases/tag/v1.2.0)
 
## Features
 
- **Thumbnail file browser** — pick a folder and see real photo previews (or a labeled placeholder for other file types) in a scrollable grid that reflows as you resize the window. A zoom slider adjusts thumbnail size on the fly.
- **Token-based renaming** — build new filenames from file metadata and your own custom text:
  - `Name` — original filename (without extension)
  - `Year`, `Month`, `Day` — from the file's last-modified date
  - `Time` — last-modified time (`HHMMSS`)
  - `Counter` — zero-padded sequence number
  - `Custom` — your own free-text input
- **Automatic subfolder organization** — optionally sort copies into nested folders built from the same tokens (e.g. `Year/Year-Month/Year-Month-Day` → `2026/2026-08/2026-08-14`). Folders are created if they don't exist, and reused if they do.
- **Metadata-preserving copies** — uses `shutil.copy2`, so timestamps are preserved on the copies. Files are copied, never moved or altered.
- **Dark mode** — toggle switch in the title bar; the whole UI re-themes instantly.
- **No network access** — everything runs locally.
