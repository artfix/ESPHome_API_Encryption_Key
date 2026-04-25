# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview
The project is a single static HTML page (`ESPHome_API_EncryptionKey_page.html`) that generates a cryptographically secure 32‑byte base64 encryption key in the browser. There is no build system, no tests, and no backend server.

## Common Development Tasks
- **Open the page locally** – Run a lightweight HTTP server to serve the file so you can view it in a browser.
  ```bash
  python -m http.server 8000  # opens http://localhost:8000/ESPHome_API_EncryptionKey_page.html
  ```
- **Edit the page** – Open `ESPHome_API_EncryptionKey_page.html` in an editor. Changes are instantly reflected when you reload the browser.
- **Run a single test** – The repository contains no automated tests; manual inspection in a browser is the only verification method.

## Architecture & Flow
1. **Static Asset** – The HTML file includes inline CSS and JavaScript.
2. **Key Generation** – On page load, `generateBase64Key()` creates 32 random bytes via `crypto.getRandomValues`, then encodes them to base64.
3. **UI Update** – The generated key is shown in the key display area and inserted into a YAML snippet template.
4. **User Actions** – Users can copy the key to the clipboard or regenerate a new one.
5. **Security Note** – The key is generated client‑side only; no network requests are made.

## How to Run the Page
```bash
# From the repository root
python -m http.server 8000
```
Navigate to `http://localhost:8000/ESPHome_API_EncryptionKey_page.html`.

No linting, building, or testing is required for this repository.

## Useful Shortcuts
- **Ctrl+Shift+E** – Open the file explorer in VS Code.
- **Ctrl+Shift+F** – Search the entire project.
- **Ctrl+P** – Quick open the HTML file.
