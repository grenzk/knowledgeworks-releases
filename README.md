# KnowledgeWorks Releases

Public distribution repository for KnowledgeWorks, a desktop automation hub for eGain workflows.

KnowledgeWorks currently includes:

- **MediaBridge** for linking media files and related articles in the eGain article editor.
- **ArticleFlow** for importing filesystem folder structures and HTML articles into eGain.
- **DocSweep** for checking spreadsheet-based document lists for updated files across supported sources.

The application source code is maintained separately and is not published in this repository.

## Download and Install

Download the installer from the [latest release](https://github.com/grenzk/knowledgeworks-releases/releases/latest).
Windows users should select `KnowledgeWorks-Setup-<version>.exe`.

Running a newer installer upgrades an existing KnowledgeWorks installation. The Windows installer is relatively large
because it includes Chrome for Testing, which allows the automation tools to use a controlled browser without relying on
the company-managed Chrome installation.

Current team distribution targets Windows x64. Automatic updates are disabled on macOS.

## Automatic Updates

Installed Windows builds check this repository for a newer published version. When an update is available,
KnowledgeWorks downloads it and prompts the user to restart the application.

Updates require a higher semantic version than the installed build. Drafts and prereleases are not offered to users on
the stable update channel.

## Publishing a Release

Each Windows release must include:

- `KnowledgeWorks-Setup-<version>.exe`
- `KnowledgeWorks-Setup-<version>.exe.blockmap`
- `latest.yml`

The Windows ZIP archive is optional. Files such as `builder-debug.yml` and `builder-effective-config.yaml` are build
diagnostics and should not be uploaded as release assets.

Publish the GitHub release only after all required assets finish uploading. Existing MediaBridge releases remain
available for installation history and update continuity.

## Source Code Archives

GitHub automatically adds **Source code (zip)** and **Source code (tar.gz)** to every release. Those archives contain
only this repository's release documentation; they do not contain the private KnowledgeWorks application source.
