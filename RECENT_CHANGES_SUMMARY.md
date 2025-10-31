# Recent Changes Summary - Top 30 Commits

This document provides a quick overview of the most recent 30 commits in the upstream repository that are not in your fork.

## Latest Changes (Most Recent First)

| # | Commit | Description | Category |
|---|--------|-------------|----------|
| 1 | c713fa8 | Merge pull request #740 - RAII DLT msg wrapper | Feature |
| 2 | 97b7924 | Add tests for QDltMsgWrapper | Testing |
| 3 | 7a008c7 | Cleanup unit tests cmake | Build |
| 4 | e901f96 | Optimize qdltmsgwrapper interface | Performance |
| 5 | 1a06512 | Add QDltMsgWrapper to handle variable payload | Feature |
| 6 | 45b7c1d | Implement RAII wrapper for DltMessage | Feature |
| 7 | 64343a8 | Merge pull request #738 - MainWindow cleanup | Refactoring |
| 8 | 6f0c092 | Move autoscroll timer to appropriate place | Refactoring |
| 9 | 6b6fc86 | Make drawInterval a function local variable | Refactoring |
| 10 | abec892 | Remove commented function (unused since 2019) | Cleanup |
| 11 | b7f6513 | Remove redundant draw_timeout method | Cleanup |
| 12 | 7a87a29 | Configurable UDP Ports for DLT Import from Pcap (#739) | Feature |
| 13 | e015a01 | Correct syntax | Fix |
| 14 | 4b6a0b8 | Merge pull request #735 - Update codesign | Build |
| 15 | c7982b1 | Remove macOS13 specific codesign | Build |
| 16 | c2778b1 | Update intel macOS build | Build |
| 17 | d7d3a4a | xCode update intel | Build |
| 18 | 628cd11 | Replace x86_64 macOS build | Build |
| 19 | 825f46c | Replace x86_64 macOS build | Build |
| 20 | 28d7ef7 | Fix creating wrong index when loading empty files (#732) | Bug Fix |
| 21 | 425c73b | Merge pull request #720 - Custom file explorer | Feature |
| 22 | 3567c3f | Process explorer menu requests in mainwindow | Feature |
| 23 | 273bb15 | Disable multiselection in file explorer tab | Feature |
| 24 | 1c9cba4 | Improve layout of fileexplorertab | UI |
| 25 | 6bc2616 | Use custom promoted FileExplorer class for fs view | Feature |
| 26 | ff11946 | Fix spelling errors in comments and documentation (#728) | Documentation |
| 27 | 0c913d2 | Merge pull request #725 - Filter and Group by ECU ID | Feature |
| 28 | 7004c6a | Merge pull request #723 - Add DLTv2 support for raw files | Feature |
| 29 | 1545197 | Added Support for messages with synchronized time | Feature |
| 30 | 4d0a329 | Merge branch 'COVESA:master' | Merge |

## Key Highlights

### 🚀 Major Features (Top 10)
1. **RAII DLT Message Wrapper** - Memory safety improvements
2. **ECU ID Filtering and Grouping** - Enhanced log organization
3. **Custom File Explorer** - Better file system navigation
4. **DLTv2 Support** - Support for newer DLT message format
5. **Configurable UDP Ports** - Flexible PCAP import
6. **Keyboard Shortcuts** - User customization
7. **Search History** - Persistent search across sessions
8. **Qt6 Migration** - Modern Qt framework support
9. **CMake Improvements** - Better build system
10. **CI/CD Enhancements** - Automated testing and releases

### 🐛 Critical Bug Fixes
- Fixed wrong index creation when loading empty files
- Fixed marker behavior when changing filters
- Fixed ECUs config tree import issues
- Fixed regexp replace in commander
- Fixed string encoding issues
- Fixed ECU tree clearing on log clear

### 🔧 Infrastructure Updates
- Qt6 migration for all platforms
- Windows 2022 support
- macOS 15 support
- Ubuntu Noble (24.04) packaging
- Removed qmake, standardized on CMake
- Unified CI/CD pipeline

### 📊 Code Quality
- Removed 966 lines of legacy code from mainwindow.cpp
- Added comprehensive unit tests
- Fixed spelling and documentation
- Removed obsolete unused code
- Updated copyright notices

## Pull Command

To get all these changes:

```bash
git checkout master
git pull upstream master
git push origin master
```

## View Changes Online

Compare your fork with upstream at:
https://github.com/COVESA/dlt-viewer/compare/e682f96...c713fa8

---
Generated: 2025-10-31
Fork: SherifBeshr/dlt-viewer
Upstream: COVESA/dlt-viewer
Commits Behind: 1,395
