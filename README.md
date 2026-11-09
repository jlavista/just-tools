# JustTools

100% free, No ads, all happen on the browsers, 100% private, No uploads. No tricks. Just tools.

The home page for a growing collection of free, browser-only tools.

**Website:** https://jlavista.github.io/just-tools/

## Tools

| Tool | Description | Website | Source |
|---|---|---|---|
| PDF Manager | Merge, split, reorder, and rotate PDFs; convert images to PDF pages. | [Open tool](https://jlavista.github.io/pdf-manager/) | [Repository](https://github.com/jlavista/pdf-manager) |
| QR Code Generator | Turn links into QR codes and download PNG or SVG files. | [Open tool](https://jlavista.github.io/qr-code/) | [Repository](https://github.com/jlavista/qr-code) |
| Voice Tools | Record, split, cut, join, and export audio; transcribe speech on the device. | [Open tool](https://jlavista.github.io/voice-tools/) | [Repository](https://github.com/jlavista/voice-tools) |

The directory is static HTML and CSS with no application dependencies, build step, or accounts. A Cloudflare Web Analytics script provides cookie-free traffic and performance statistics, disclosed in the footer. The directory works without JavaScript or when analytics is blocked. The linked tools process documents, links, and audio locally in the browser. Voice Tools downloads a speech model on first transcription use, after permission; recordings and transcripts remain on the device.

Analytics sends ordinary page-traffic and performance data to Cloudflare, not document contents, filenames, form values, URLs entered into the QR generator, audio, or transcripts. The public beacon token is shared across `/just-tools/`, `/pdf-manager/`, `/qr-code/`, and `/voice-tools/` under `jlavista.github.io`; use the page-path breakdown in Cloudflare to compare tools. GitHub Pages also receives ordinary website and asset requests. "No uploads" refers to user files and entered links, not analytics requests or model downloads.

## Add a tool

Add a new `.tool-card` link inside `.tool-grid` in `index.html`, with a unique heading and description ID, a short description, its supported formats, and its website URL. Update the tool count in `.badge` and the table above. Follow the existing cards for consistent styling and accessibility.

## Run locally

Serve this directory with any static web server:

```powershell
python -m http.server 8000 --bind 127.0.0.1
```

Open `http://localhost:8000`. The directory also works without JavaScript.

## GitHub Pages

In **Settings > Pages**, deploy from the `main` branch and **/ (root)**. Keep `index.html`, `styles.css`, `icon.svg`, and `.nojekyll` in the repository root. Asset paths are relative, so the site works under `/just-tools/`.
