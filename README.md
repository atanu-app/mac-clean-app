# Mac Clean

Free up space on your Mac by removing files that can be rebuilt or downloaded again: old Xcode device files, unused simulators, Android emulators and SDK versions, package caches, app and browser caches, and build folders from projects you haven't touched in a while.

Mac Clean shows everything it finds, explains what happens if you delete each item, and asks before deleting anything. It never touches your source code, documents or app data.

**[Download Mac Clean](https://github.com/atanu-app/mac-clean-app/releases/latest/download/MacClean.dmg)**

Works on macOS 12 Monterey or later, on Apple silicon and Intel Macs.

## Who it's for

People who use **Xcode, Android Studio, Flutter, Node.js or Python** on their Mac. These tools quietly keep many gigabytes of caches and old files.

Everyone else can still use it to clear **app caches**: browsers (Chrome, Brave, Edge, Firefox, Arc), editors (VS Code, Cursor), chat and work apps (Slack, Discord, Postman) and any other app that keeps a cache in the standard macOS place. Mac Clean skips the caches of apps that are open, so quit an app first to include it.

## Install

1. Click **Download Mac Clean** above.
2. Open the downloaded **MacClean.dmg**.
3. Drag **Mac Clean** into the **Applications** folder.
4. Open **Mac Clean** from Applications.

### The first time you open it

macOS may say *"Apple could not verify 'Mac Clean' is free of malware"*. To open it anyway:

1. Click **Done**.
2. Open **System Settings** › **Privacy & Security**.
3. Scroll down to the message about **Mac Clean** and click **Open Anyway**.
4. Enter your Mac password, then click **Open Anyway** again.

You only need to do this once. If macOS asks whether Mac Clean may access your **Documents** folder, click **Allow**. That's where it looks for project build files.

## How to use it

1. **Wait a few seconds** while it scans.
2. **Look at what it found.** Each item shows its size and a label:
   - **Safe**: rebuilt automatically. These are ticked for you.
   - **Review**: you'll need to reinstall or re-download something later. Read the note before ticking it.
   - **Protected**: found but kept, like projects you worked on recently. These can't be deleted.
3. Click **ⓘ** on any item for details, or **Show in Finder** to see it.
   To choose where your projects are, click **Choose Folders…** under Project Build Files.
   To never be offered something again, open its details and click **Always Keep** (undo it with **Stop Keeping**).
4. Click **Clean…**, check the summary, and confirm. Items marked **Review** go to the **Trash**, so you can put them back; everything else is deleted.

Click the clock button at the top to see your **Cleaning History**: everything Mac Clean has cleaned, and how much space it freed.

Quit Xcode and the Simulator before cleaning.

## What it never deletes

- Your source code, project files and Git history
- Project settings such as `package.json`, `Podfile` or `pubspec.yaml`
- Anything in a project you edited in the last 30 days (you can change this)
- Your documents, photos, app data, passwords and settings (for apps, only their caches are removed; sign-ins, history and settings stay)
- macOS's own caches, and the caches of apps that are open
- Xcode, simulator and Android files while Xcode, Simulator or Android Studio is open
- Anything you chose to always keep

Before deleting, Mac Clean checks every item again and skips anything that no longer matches these rules.

## After cleaning

- The first build of each project takes a little longer.
- When you plug in an iPhone, Xcode prepares it again (about 5 minutes).
- If you removed a project's dependencies, reinstall them before working on it (for example `npm install`).

## Privacy

Mac Clean works entirely on your Mac. It doesn't need an internet connection and doesn't send any data anywhere.

## Help

Found a problem? [Open an issue](https://github.com/atanu-app/mac-clean-app/issues).

---

Copyright © 2026 Atanu. All rights reserved. Free to download and use; see [LICENSE](LICENSE). The source code is not public.
