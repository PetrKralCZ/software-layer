# Default Branch Migration Guide

## Overview

This repository has migrated from using `2023.06-software.eessi.io` as the default branch to using `main` as the default branch. This document explains how to complete the migration process.

## Current Status

- ✅ **Main branch created**: The `main` branch exists and contains the full software layer structure
- ✅ **Content migrated**: All easystack files for all EESSI versions are now in the `main` branch
- ✅ **Workflows updated**: GitHub Actions workflows reference the `main` branch
- ✅ **Documentation updated**: README.md reflects the new branch structure
- ⚠️ **GitHub default branch**: The repository's default branch setting needs to be updated on GitHub

## How to Change the Default Branch on GitHub

To complete the migration, a repository administrator needs to:

1. **Go to the repository settings**:
   - Navigate to https://github.com/PetrKralCZ/software-layer/settings
   - Click on "General" in the left sidebar

2. **Change the default branch**:
   - Scroll down to the "Default branch" section
   - Click the ⚖️ button next to the current default branch
   - Select `main` from the dropdown
   - Click "Update"
   - Confirm the change in the dialog that appears

3. **Verify the change**:
   - Visit the main repository page
   - Confirm that the `main` branch is now shown as default
   - Verify that new clones and pull requests target the `main` branch by default

## What This Change Accomplishes

- **Simplified workflow**: New contributors will automatically target the `main` branch
- **Better organization**: The `main` branch contains easystack files for all EESSI versions, not just 2023.06
- **Future-proofing**: The repository structure supports multiple EESSI versions
- **Consistency**: Aligns with standard Git practices and the EESSI software layer architecture changes

## For Contributors

After the default branch is changed:

- **New clones**: Will automatically check out the `main` branch
- **Existing clones**: Run `git remote set-head origin main` to update your local default
- **Pull requests**: Should target the `main` branch (this will be automatic for new PRs)
- **Old branch**: The `2023.06-software.eessi.io` branch contains a retirement notice directing users to `main`

## Technical Details

The migration involved:

1. Creating a new `main` branch with the complete software layer structure
2. Updating GitHub Actions workflows to reference `main`
3. Adding comprehensive documentation and easystack files for all EESSI versions
4. Creating retirement notices on the old branch

The repository is now ready for the `main` branch to serve as the default branch.