<p align="center">
  <img src="docs/images/icon.png" width="112" height="112" alt="SOPHRON icon">
</p>

<h1 align="center">SOPHRON</h1>

<p align="center">
  A private desk for your work
</p>

<p align="center">
  <a href="https://github.com/HelloWorld233a/SOPHRON/releases"><img alt="Version" src="https://img.shields.io/badge/version-0.1.0--beta.1-8a5a3c"></a>
  <img alt="Platforms" src="https://img.shields.io/badge/platform-macOS%20%7C%20Windows-555">
  <img alt="Tauri 2" src="https://img.shields.io/badge/Tauri-2-24c8db">
  <img alt="React 19" src="https://img.shields.io/badge/React-19-61dafb">
  <img alt="Rust" src="https://img.shields.io/badge/Rust-2024%20edition-b7410e">
  <img alt="SQLite" src="https://img.shields.io/badge/SQLite-local-0f80cc">
</p>

<p align="center">
  <a href="README.zh-Hant.md">繁體中文</a> · <b>English</b>
</p>

<p align="center">
  <img src="docs/images/desk.jpg" alt="SOPHRON desk" width="860">
</p>

---

## 1. SOPHRON

**A private desk for your work.**

## 2. Overview

SOPHRON is a productivity app built around the idea of a private digital desk. The main screen is a desk, and each object on it opens one feature: an index card for the focus timer, a sticky note for tasks, a composition book for the journal, a folder for the archive and a timetable card for your weekly classes. You can arrange, resize, add and remove these objects to suit the way you work.

SOPHRON is a local-first desktop app. All data stays on your own computer: there is no account and nothing is sent over the network.

> This repository only distributes installers. The source code is not currently public.

## 3. Screenshots

The screenshots below come from the current version and show demo data.

| The desk | First-run setup |
| :---: | :---: |
| <img src="docs/images/desk.jpg" alt="The desk" width="420"> | <img src="docs/images/onboarding.jpg" alt="First-run setup" width="420"> |
| **Tasks** | **Timetable** |
| <img src="docs/images/tasks.jpg" alt="Tasks" width="420"> | <img src="docs/images/timetable.jpg" alt="Timetable" width="420"> |
| **Archive** | **Record player and ambient mixer** |
| <img src="docs/images/archive.jpg" alt="Archive" width="420"> | <img src="docs/images/mixer.jpg" alt="Record player and ambient mixer" width="420"> |

## 4. Features

| Feature | Description |
| --- | --- |
| Focus timer | Pomodoro-style timer with focus, short break and long break; adjustable lengths and auto-start; can be linked to the task you are working on; statistics for today and the last seven days; a system notification when a phase ends. |
| Tasks | Add, complete and reorder tasks; three priority levels; notes; filter by open, done or all; start a focus session on a task directly. |
| Journal | One page per day with bold, italic, headings, bulleted and numbered lists and quotes; saves automatically; date navigation; word count. |
| Archive | Weekly focus chart (twelve weeks), a month calendar showing focus minutes and journal entries per day, focus history, completed tasks and a list of journal entries. |
| Timetable | Weekly timetable with subject, time, room, teacher, colour and notes; shows the class in progress and the next class today. |
| Record player | Plays music files you choose from your computer, with a playlist; or switch to ambient mode and layer rain, thunder, wind, waves, fireplace, white, pink and brown noise freely, with eight presets. |
| Data safety | Local SQLite database; automatic daily backup (the latest ten are kept); manual backup and JSON export; undo when deleting items. |
| Language reminder | Shows a small note when swear words are typed in Cantonese, English or Mandarin. The text is never changed, and the reminder can be turned off. |

## 5. Desk customisation and plugin system

### Customising the desk

- Drag an object to move it, and drag its bottom-right corner to resize it.
- Any object can be pinned so it stays above the others.
- Some objects have their own colour options: the alarm clock case, the task note paper, the timetable card header and the record player plinth.
- Desk settings: five wood finishes; eight desk mat colours plus a custom colour; three mat sizes; a tidy mode that keeps every object on the mat; keep the window on top.
- First-run setup: on first launch, SOPHRON helps you choose the desk style, the objects on the desk and the focus length. It can be run again from desk settings.

### Plugin system (current state)

Every object on the desk is a desk plugin. The plugin system currently works as follows:

| Item | Current state |
| --- | --- |
| Where plugins come from | Built into the app and registered automatically at build time. Loading third-party plugins at runtime is not supported yet. |
| Built-in plugins | Alarm clock, Focus, Tasks, Journal, Archive, Timetable, Record player, Memo and Crisps: nine in total. |
| What you can do with them | Add or remove them from the "+" drawer in the bottom-left corner; drag; resize (aspect ratio is kept); pin on top; change colours per object. Memos, alarm clocks and crisps can be placed more than once. |
| Storage | The position, size, stacking order and settings of every object are saved in the local database and restored on the next launch. |
| 3D plugins | **Planned; development has not started.** |

## 6. Architecture and technology

| Layer | Technology |
| --- | --- |
| Desktop framework | [Tauri 2](https://tauri.app/), a lightweight desktop framework that renders the interface with the system web engine |
| Interface | React 19, TypeScript, Vite |
| Backend | Rust (2024 edition) |
| Database | SQLite (through rusqlite, with WAL mode and versioned migrations) |
| Text editor | TipTap |
| Audio | Web Audio API (ambient sounds are synthesised in real time; no recordings are used) |

Key design points:

- **The timer** runs in Rust on wall-clock timestamps, so it stays accurate when you switch rooms or the computer sleeps.
- **The database is backed up automatically before each migration**, so an upgrade cannot lose data.
- **The interface** uses a skeuomorphic design (imitating the look of real objects); all textures and icons are original artwork.

## 7. Development status

**Version: 0.1.0-beta.1 (beta)**

| Item | Status |
| --- | --- |
| macOS (Apple Silicon) | Installer available; features tested on the developer's computer with the development build. |
| macOS (Intel) | Not available yet. |
| Windows 10 / 11 (64-bit) | Installer available (cross-compiled on macOS); **not yet tested on a Windows computer**. |
| Code signing | Not signed yet (the system shows a security prompt during installation; see below). |
| Minimum OS version | To be confirmed. |

This is a beta release and may still contain bugs. Please use the Back up button in desk settings regularly.

## 8. Installation and use

Download the latest version from [Releases](https://github.com/HelloWorld233a/SOPHRON/releases):

| System | File |
| --- | --- |
| macOS (Apple Silicon) | `SOPHRON_…_macOS_AppleSilicon.dmg` |
| Windows 10 / 11 (64-bit) | `SOPHRON_…_Windows_x64-setup.exe` |

**macOS**

1. Open the `.dmg` and drag SOPHRON into Applications.
2. The app is not signed by Apple yet. The first time, right-click SOPHRON in Applications, choose Open, then click Open. After that it opens normally.

**Windows**

1. Run `setup.exe`.
2. If you see "Windows protected your PC", click More info, then Run anyway.
3. The installer needs Microsoft WebView2 and downloads it automatically if it is missing.

**Basics**

- Click an object on the desk to open its feature. Click Desk in the top-left corner, or press `Esc`, to return.
- `⌘` (`Ctrl` on Windows) + `1` to `6`: Desk, Focus, Tasks, Journal, Archive, Timetable.

**Where your data is stored**

| System | Location |
| --- | --- |
| macOS | `~/Library/Application Support/app.sophron.desktop/` |
| Windows | `%APPDATA%\app.sophron.desktop\` |

The database is `sophron.db`; automatic backups are in the `backups` folder next to it.

**Verifying downloads**

Each release includes `SHA256SUMS.txt`:

```bash
# macOS
shasum -a 256 SOPHRON_*.dmg
```

```powershell
# Windows
certutil -hashfile SOPHRON_0.1.0-beta.1_Windows_x64-setup.exe SHA256
```

## 9. Roadmap

These items are planned and have no release date yet:

- Full testing on Windows computers.
- Code signing for macOS and Windows.
- 3D plugins (for example, a three-dimensional document or object).
- Confirming and documenting the minimum OS versions.

## 10. Contributing

The source code is not public yet, so code contributions cannot be accepted for now. Bug reports and suggestions are welcome in [Issues](https://github.com/HelloWorld233a/SOPHRON/issues). When reporting a problem, please include your operating system version, the SOPHRON version and the steps to reproduce it.

## 11. License

No license has been specified yet.

## 12. Acknowledgements

SOPHRON is built with these open-source projects: [Tauri](https://tauri.app/), [React](https://react.dev/), [Vite](https://vite.dev/), [TipTap](https://tiptap.dev/), [rusqlite](https://github.com/rusqlite/rusqlite) and [SQLite](https://sqlite.org/). The interface fonts Inter, Caveat and Cormorant Garamond are licensed under the SIL Open Font License and provided through [Fontsource](https://fontsource.org/).
