# How to Update Your Fork - Quick Guide

## TL;DR - Your Fork Status

Your fork `SherifBeshr/dlt-viewer` is **1,395 commits behind** the upstream `COVESA/dlt-viewer` repository.

## Quick Answer to Your Question

**"What are changes that my master is behind?"**
- See [UPSTREAM_CHANGES_ANALYSIS.md](UPSTREAM_CHANGES_ANALYSIS.md) for comprehensive details
- See [RECENT_CHANGES_SUMMARY.md](RECENT_CHANGES_SUMMARY.md) for top 30 recent commits

**"What will be new if I pull latest changes?"**

You'll get:
- ✅ **7 major new features** (RAII wrapper, ECU filtering, file explorer, DLTv2, configurable ports, keyboard shortcuts, search history)
- ✅ **Multiple critical bug fixes** (index creation, markers, encoding, etc.)
- ✅ **Qt6 migration** - Modern Qt framework
- ✅ **CMake standardization** - qmake removed
- ✅ **Code cleanup** - 966 lines of legacy code removed
- ✅ **Enhanced CI/CD** - Windows 2022, macOS 15, Ubuntu Noble support
- ✅ **1,938 lines added**, 1,110 lines removed across 38 files

## Step-by-Step Update Process

### 1. Preparation (IMPORTANT!)

```bash
# Backup your current state
git checkout master
git status
# Commit or stash any local changes

# Create a backup branch (optional but recommended)
git checkout -b backup-before-upstream-merge
git checkout master
```

### 2. Add Upstream Remote (if not already added)

```bash
# Check if upstream is configured
git remote -v

# If upstream is not listed, add it:
git remote add upstream https://github.com/COVESA/dlt-viewer.git

# Fetch upstream changes
git fetch upstream
```

### 3. Pull Upstream Changes

```bash
# Ensure you're on master
git checkout master

# Pull from upstream
git pull upstream master

# If there are merge conflicts, resolve them:
# 1. Open conflicted files in your editor
# 2. Resolve conflicts (look for <<<<<<, ======, >>>>>> markers)
# 3. Stage resolved files: git add <file>
# 4. Complete the merge: git commit
```

### 4. Push to Your Fork

```bash
# Push updated master to your fork
git push origin master
```

### 5. Post-Update Verification

```bash
# Verify you're up to date
git log --oneline -5

# Rebuild the project
mkdir -p build
cd build
cmake ..
cmake --build .

# Run tests
ctest
```

## Important Notes

### ⚠️ Breaking Changes

1. **Qt6 Required**: The upstream now uses Qt6. Ensure you have Qt6 installed.
2. **CMake Only**: qmake project files removed. Use CMake.
3. **mainwindow.cpp**: Major refactoring - check if you have custom modifications here.

### 💡 Recommended Approach

Given the large number of changes (1,395 commits), consider:

**Option A: Direct Merge (Faster)**
- Pull all changes at once
- Deal with conflicts as they arise
- Best if you have minimal custom changes

**Option B: Incremental Updates (Safer)**
```bash
# Cherry-pick major PRs one by one
git cherry-pick <commit-hash>
# Test after each major change
```

**Option C: Fresh Fork (Cleanest)**
- If you have no custom changes
- Delete your fork and re-fork from upstream
- Start fresh with latest code

## Need Help?

### View Changes Online

Before pulling, review changes at:
```
https://github.com/COVESA/dlt-viewer/compare/e682f96...c713fa8
```

### Check Specific PR

To see details of a specific pull request:
```
https://github.com/COVESA/dlt-viewer/pull/<PR_NUMBER>
```

For example:
- PR #740: RAII wrapper - https://github.com/COVESA/dlt-viewer/pull/740
- PR #725: ECU filtering - https://github.com/COVESA/dlt-viewer/pull/725

### If You Get Stuck

1. Check conflict resolution in Git documentation
2. Create an issue in the upstream repository
3. Ask the COVESA/dlt-viewer community

## After Successful Update

- ✅ Update your development environment to Qt6 if needed
- ✅ Review new features and test them
- ✅ Update your local documentation
- ✅ Consider contributing back to upstream!

## Summary of Analysis Files

This repository now contains:

1. **UPSTREAM_CHANGES_ANALYSIS.md** - Comprehensive analysis
   - All major features
   - All bug fixes
   - File statistics
   - Detailed recommendations

2. **RECENT_CHANGES_SUMMARY.md** - Quick reference
   - Top 30 recent commits
   - Categorized changes
   - Key highlights

3. **HOW_TO_UPDATE_FORK.md** - This file
   - Quick guide
   - Step-by-step instructions
   - Troubleshooting tips

---

**Last Updated**: 2025-10-31  
**Upstream**: COVESA/dlt-viewer  
**Your Fork**: SherifBeshr/dlt-viewer  
**Commits Behind**: 1,395
