# OneDrive & Data Science: Avoiding "Empty File" Errors

## The Problem

OneDrive's **Files On-Demand** feature keeps files as cloud-only placeholders to save disk space. They show up in File Explorer with a normal name and size, but the actual bytes aren't on your hard drive until something requests them.

GUI apps (Word, Excel, Photos, etc.) know how to trigger a download automatically when opened. Most data science tools — Python, R, command-line utilities, Jupyter, etc. — do not reliably trigger this. The result: `FileNotFoundError`, permission errors, or files that read as empty/zero-byte, even though Explorer shows them as present. **OneDrive can totally bork a git repo!**

## Solutions

### Option A: Keep All OneDrive Files Downloaded Locally

Forces every file in your OneDrive folder to stay fully downloaded, disabling the placeholder behavior.

1. Open **File Explorer**.
2. In the left sidebar, right-click **OneDrive**.
3. Select **Always keep on this device**.
4. Wait for sync to finish — a checkmark icon will replace the cloud icon on all files.

**Trade-off:** Uses full local disk space equal to your OneDrive storage. Fine for moderate amounts of data; may be a problem if you're storing very large datasets in OneDrive.

### Option B: Point Known Folders Back to Your Local Home Directory

Un-redirects Documents/Desktop/Pictures from OneDrive so they live in your normal Windows user profile instead — this is how a non-university-managed laptop is typically set up.

1. Click the **OneDrive cloud icon** in the system tray (bottom-right, may be under the ^ arrow).
2. Click the **gear icon** → **Settings**.
3. Go to the **Sync and backup** tab.
4. Click **Manage backup**.
5. For each folder (Desktop, Documents, Pictures), toggle it **off**.
6. Confirm when prompted — this moves the folder's content back out of OneDrive into your local user profile (e.g., `C:\Users\yourname\Documents`).

**⚠️ Warning:** Once unlinked, these folders are **no longer backed up to the cloud automatically**. If your laptop is lost, stolen, or its drive fails, anything in them is gone unless you're backing up some other way. Make sure you have a separate backup plan (external drive, manual OneDrive uploads, git repos, etc.) before doing this.