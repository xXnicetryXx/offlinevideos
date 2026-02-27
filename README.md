# OfflineVideos

A browser-based suite for localized video playback and metadata management. This project provides a decentralized approach to media handling, requiring no server-side dependencies or external installation.

## Repository Contents

* `player.html` — The core interface for media playback, supporting local file streaming and playback controls.
* `editor.html` — A utility interface for managing video configurations, metadata, or file parameters.
* `offlinevideos.zip` — A compressed archive containing the full application suite for portable use.

## Technical Specifications

### Architecture
This is a static frontend application. All logic is executed on the client side within the web browser. This ensures complete data privacy and full functionality in offline environments.

### System Requirements
* **Browser:** Any modern web browser (Google Chrome, Mozilla Firefox, Apple Safari, or Microsoft Edge).
* **Extraction Tool:** A standard utility to decompress the `.zip` distribution.

## Usage Instructions

### Direct Execution
To use the application tools:
1. Clone the repository or download the source files.
2. Open `player.html` to begin media playback.
3. Open `editor.html` to access configuration or editing tools.

### Portable Distribution
1. Download `offlinevideos.zip`.
2. Extract the folder to your local drive or a USB storage device.
3. Launch the desired `.html` file directly from the extracted folder.

## Deployment
While designed for local use, this project can be hosted on any static web provider. To deploy via **GitHub Pages**:
1. Navigate to the repository **Settings**.
2. Select **Pages** from the sidebar.
3. Under **Branch**, select `main` and click **Save**.
4. Note: Since there is no `index.html`, you will need to append `/player.html` or `/editor.html` to your generated GitHub Pages URL to view the tools.

## License
This project is released under the MIT License.
