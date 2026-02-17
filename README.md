# MasterBooter-Tools — GitHub Release Mirror

Fallback download mirror for PE tools used by [MasterBooter](https://github.com/Howweird/MasterBooter).

MasterBooter downloads tools from their original manufacturer sites first.
If that fails (site down, link changed, etc.), it automatically falls back
to these GitHub-hosted copies.

## How It Works

1. Each tool has a `tool.toml` with `download_url` (manufacturer) and `fallback_url` (GitHub)
2. MasterBooter tries the manufacturer URL first
3. If that fails, it retries from `https://github.com/Howweird/MasterBooter-Tools/releases/download/v1.0/{filename}`
4. The ZIP contents extract directly into the tool's folder — no nested subfolders

## Release Assets (v1.0)

### Shell & Desktop

| File | Size | Description |
|------|------|-------------|
| WinXShell.zip | 3.1 MB | Desktop shell for WinPE (taskbar, start menu, file manager) |
| Explorer++.zip | 2.3 MB | Tabbed file manager — from [derceg/explorerplusplus](https://github.com/derceg/explorerplusplus) |
| FileExplorer.zip | 655 KB | Dual-pane file explorer with search — .NET 4.8 |

### Network & Web

| File | Size | Description |
|------|------|-------------|
| PENetwork.zip | 987 KB | Network configuration (IP, WiFi, shares, ping) |
| WebBrowser.zip | 98 KB | Compact portable web browser — .NET 4.8 |

### Disk & System

| File | Size | Description |
|------|------|-------------|
| CrystalDiskInfo.zip | 7.6 MB | Disk health monitor (SMART data) — from [SourceForge](https://sourceforge.net/projects/crystaldiskinfo/) |
| DiskCheck.zip | 2.2 MB | SMART status monitor using smartctl — .NET 4.8 |
| DISMTool.zip | 4.6 MB | GUI for DISM (running OS, mounted WIM, offline OS) — .NET 4.8 |

### Utilities

| File | Size | Description |
|------|------|-------------|
| 7-Zip.zip | 2.5 MB | Portable file archiver |
| Autoruns.zip | 984 KB | Sysinternals auto-start manager — from [Microsoft](https://learn.microsoft.com/en-us/sysinternals/downloads/autoruns) |
| EventViewer.zip | 24 MB | Windows event log viewer for WinPE/live Windows — .NET 4.8 |
| InstalledSoftware.zip | 24 MB | Software inventory from offline/live Windows — .NET 4.8 |

**Total: ~72 MB across 12 tools**

### Tool Sources

| Source | Tools |
|--------|-------|
| GitHub (primary host) | WinXShell, PENetwork, 7-Zip |
| [derceg/explorerplusplus](https://github.com/derceg/explorerplusplus) | Explorer++ |
| [Microsoft Sysinternals](https://learn.microsoft.com/en-us/sysinternals/) | Autoruns |
| [SourceForge](https://sourceforge.net/projects/crystaldiskinfo/) | CrystalDiskInfo |
| [pcassistsoftware.co.uk](https://www.pcassistsoftware.co.uk) | DiskCheck, DISMTool, WebBrowser, EventViewer, InstalledSoftware, FileExplorer |

## Notes

- .NET 4.8 tools require the `WinPE-NetFx` ADK package (enabled by default in MasterBooter)
- WiFi drivers are NOT hosted here — they are extracted from the local Windows installation during PE build
- All tools work in both WinPE and live Windows environments
