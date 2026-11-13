# SOPHRON

一張屬於你嘅書枱：專注計時、任務、日誌、課程表、唱片機同白噪音，全部擺喺枱面，撳物件就打開。
A desk on your screen: focus timer, tasks, journal, timetable, record player and ambient sounds. Tap an object to open it.

所有資料只會存喺你部電腦，唔會上網。
Everything stays on your computer. Nothing is sent online.

## 下載 · Download

去 [Releases](../../releases/latest) 下載最新版本：

| 系統 System | 檔案 File |
| --- | --- |
| macOS（Apple Silicon，M1 或之後） | `SOPHRON_x.y.z_macOS_AppleSilicon.dmg` |
| Windows 10 / 11（64 位元） | `SOPHRON_x.y.z_Windows_x64-setup.exe` |

## 安裝 · Install

**macOS**：打開 `.dmg`，將 SOPHRON 拖入「應用程式」。因為程式未有 Apple 開發者簽名，第一次打開要喺「應用程式」入面**右撳 SOPHRON → 打開 → 再撳「打開」**。之後就可以正常雙擊。

**Windows**：執行 `setup.exe`。如果見到「Windows 已保護您的電腦」，撳**其他資訊 → 仍要執行**（程式未有數碼簽名）。Windows 10 如果未有 WebView2，安裝程式會自動下載。

## 檢查檔案 · Verify

每個 Release 都附有 `SHA256SUMS.txt`。

```
shasum -a 256 SOPHRON_*.dmg        # macOS
certutil -hashfile SOPHRON_*.exe SHA256   # Windows
```

---

呢個 repo 只發佈安裝檔，唔包含原始碼。
This repository only distributes installers; the source code is not published.
