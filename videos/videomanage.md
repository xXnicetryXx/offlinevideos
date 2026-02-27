# Video Management

This document provides technical information regarding how media is stored, processed, and managed within the OfflineVids ecosystem.

## Storage Architecture (The Vault)

OfflineVids does not store video files in traditional server directories. Instead, it utilizes **IndexedDB**, a low-level API for client-side storage of significant amounts of structured data.

* **Media Blobs:** Raw video data is stored as Binary Large Objects (Blobs) within the browser's internal database.
* **Persistence:** Once a video is "Published to Vault" via `Editor.html`, it remains available offline even after the browser is closed or the machine is restarted.
* **Privacy:** Since all data is stored locally in your browser's private storage, no third-party servers ever have access to your video library.

## Asset Specifications

The system is optimized for the following configurations:

### 1. Standard Video (Widescreen)
* **Aspect Ratio:** 16:9 or 4:3
* **Interface:** Viewed via the standard cinematic player in `Player.html`.
* **Use Case:** Movies, episodes, and long-form content.

### 2. Vertical Content (Shorts)
* **Aspect Ratio:** 9:16 or 1:1
* **Interface:** Automatically detected by the Editor and directed to the "Shorts" scroll-player.
* **Use Case:** Social media archives and mobile-optimized clips.

## Managing Your Collection

### Importing Content
To add videos to your local collection:
1. Navigate to `Editor.html`.
2. Provide a source file and a title.
3. The system will generate a localized thumbnail and calculate the aspect ratio before saving to the database.

### External Resources
For users looking to source content for their offline collection, common tools for retrieving personal media from web platforms include:
* **Command-line Utilities:** Tools like `yt-dlp` are industry standards for media archival.
* **Web Services:** Various third-party web-based converters allow for the retrieval of video files for offline use.

### Deleting Content
Media can be permanently removed from the "Vault" using the delete function within `Player.html`. This action clears the associated entry from both the metadata and blob stores in IndexedDB.

## Troubleshooting Storage
If videos fail to save, ensure that your browser has sufficient "Site Storage" permissions. Most modern browsers allow several gigabytes of IndexedDB storage, but this can be limited if your hard drive is nearly full.
