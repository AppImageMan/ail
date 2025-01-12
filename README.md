# App Image List

## Description

Version controlled mirror of AppImage files.

### Motivation

Downloading AppImages is a very manual process. It would be nice to be able to get them from a store or a package manager.

The problem is there is no standard for releasing the AppImages. Some have nice versions, but many are continuous release.

This makes it hard to make sure you have yours updated.

Some AppImages support auto-update, but not all.

Thus, having a centralized clone of AppImage files locked to a specific version is very useful. Hence this repo.

## How It Works

Each branch of this repo is dedicated to an AppImage.

It contains a copy of the main file named "application.AppImage" (added via git lfs) as well as a file called "date.txt" containing a date-version for when the branch was updated in the format: `YY.MM.R` where `YY` is the two digits of the year like 2025 → 25, `MM` is month as a number 0 through 12, and `R` is a counter that goes up each time a new update comes out.

And version.txt is an optional file which can show the real version number of the application.

Then an AppImage package manager can use the date as its version number (while showing the "real" version if it exists).
