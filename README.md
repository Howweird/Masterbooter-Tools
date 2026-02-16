# MasterBooter-Tools — GitHub Release Mirror

This folder is a mirror of what should be uploaded to the GitHub release.

## How to Use

1. Create a GitHub repo called `MasterBooter-Tools`
2. Create a new release tagged `v1.0`
3. Upload ALL ZIP files from this folder as release assets (drag and drop)
4. Copy the download URLs from the release page
5. Update each `pe_tools/*/tool.toml` file:
   - Replace `YOURUSER` with your GitHub username

## Files in This Folder

| File | Size | Tool |
|------|------|------|
| WinXShell_2.5.zip | 3.1 MB | Desktop shell for PE |
| ExplorerPP_1.4.0.zip | 2.3 MB | File manager |
| PENetwork_0.59.zip | 987 KB | Network config (IP, WiFi, shares) |
| 7-Zip_24.09.zip | 2.5 MB | File archiver |
| Autoruns_14.11.zip | 984 KB | Sysinternals startup manager |
| CrystalDiskInfo_9.7.2.zip | 7.6 MB | Disk health monitor |

Total: ~18 MB

## WiFi Drivers

WiFi drivers are NOT in this folder — they are extracted automatically
from the local Windows installation during PE build (C:\Windows\INF).
No download or hosting needed.
