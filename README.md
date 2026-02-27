# OfflineVids

OfflineVids is a localized, browser-based media management suite designed for high-performance video playback and metadata organization without the need for a backend server. The system leverages modern web technologies to provide a secure, private, and entirely offline experience.

## Technical Specifications

### Architecture
The application is built as a static frontend suite. It utilizes **IndexedDB** for persistent local storage of video blobs, thumbnails, and metadata. This architecture ensures that media remains on the user's local machine, providing fast retrieval and complete data privacy.

### Core Components
* `Player.html` — The primary interface for media consumption. It features a library view, search functionality, category filtering, and a specialized "Shorts" scroll player for vertical content.
* `Editor.html` — The management utility used to import new media into the local "Vault." It supports automatic thumbnail generation, aspect ratio detection (Widescreen vs. Shorts), and metadata tagging.
* `offlinevideos.zip` — A portable, compressed distribution of the full application suite.

## Key Features

* **Local Vault Storage:** Save videos directly to the browser's IndexedDB for instant offline access.
* **Smart Detection:** Automatic identification of 9:16 portrait or 1:1 square videos to categorize them as "Shorts."
* **Advanced Playback:** Includes queue management, playback speed controls, and a dedicated vertical scroll mode.
* **Zero Dependencies:** No Python, Node.js, or external database required. Runs natively in any modern web browser.

## Getting Started

### Installation
1. Clone the repository:
   `git clone https://github.com/xXnicetryXx/offlinevideos.git`
2. Alternatively, download and extract `offlinevideos.zip`.

### Usage
1. **Importing Media:** Open `Editor.html` in your browser. Drag and drop a video file to begin the "Publish to Vault" process.
2. **Viewing Content:** Open `Player.html` to browse your local library and begin playback.

## Requirements
* **Browser:** A modern web browser with IndexedDB support (Chrome, Firefox, Edge, or Safari 15.4+).
* **Storage:** Sufficient local disk space for the browser to store video blobs in its internal database.

## TIP
use [y2mate](y2mate.ws) (recommended) to download YouTube videos/shorts OR [TurboscribeAI](https://turboscribe.ai/downloader/youtube/video) (Faster but limited)
## License
This project is released under the MIT License.
