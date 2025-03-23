# Image Downloader Userscript

A Tampermonkey userscript that adds download buttons next to image links on web pages and provides a bulk download option.

## Features

- Automatically detects image links on web pages
- Adds download buttons next to each image link
- Bulk download option via a floating button
- Download progress notifications
- Configurable allowed domains
- Supports dynamic content loading

## Supported Image Formats

- .jpg
- .jpeg
- .png
- .gif
- .bmp
- .webp
- .tiff
- .svg

## Installation

1. Install the Tampermonkey browser extension
2. Create a new userscript in Tampermonkey
3. Copy and paste the contents of `scm-image-downloader.user.js
` into the editor
4. Save the script

## Configuration

### Allowed Domains

To configure which domains the script works on, edit the `allowedDomains` array at the top of the script:

```javascript
const allowedDomains = ['*']; // Allow all domains
// OR
const allowedDomains = ['example.com', 'images.com']; // Specific domains only
```

## Usage

- Individual downloads: Click the "Download" button next to any image link
- Bulk download: Click the floating "Bulk Download" button in the bottom left corner
- Progress notifications appear when downloads start and complete
- The bulk download counter shows how many downloadable images are found on the page

## Notes

- The script only processes direct image file links in `<a>` tags
- Downloads are processed with a 500ms delay between each file to prevent overwhelming the browser
- The script automatically scans for new content every 2 seconds
- Can be used alongside the Video Downloader script without conflicts
