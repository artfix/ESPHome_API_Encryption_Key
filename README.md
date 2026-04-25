# ESPHome Encryption Key Generator

A lightweight static HTML page that generates a 32‑byte base64 encryption key in the browser. Double‑click the file or open it in a browser to use it. The key is generated client‑side only; no network requests are made.

## Features
- **No build step** – the page is plain HTML/CSS/JS.
- **Secure random key** – uses the Web Crypto API.
- **Copy / regenerate** – buttons to copy the key to the clipboard or generate a fresh one.

## Usage
1. Open `ESPHome_API_EncryptionKey_page.html` in a modern browser.
2. Click **Copy** to copy the key.
3. Click **Regenerate** to create a new key.

## Development
Since the repo is static, there is no build or test workflow. Any changes can be made directly in the HTML file.

## License
MIT (see LICENSE file if added).