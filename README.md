# Good2Dou

![release](https://img.shields.io/github/v/release/Cyperaceae/good2dou)

Extract Goodreads metadata and autofill Douban new subject pages.

🔗 [Landing page](https://good2dou.pages.dev/)

## Installation

### Chrome / Edge

Install directly from the [Chrome Web Store](https://chromewebstore.google.com/detail/good2dou/jepndkfbipginmljbjmgnkpomhpdehid).

Alternatively, for manual installation:

1. Download the latest `good2dou-chrome-*.zip` from the [Releases](https://github.com/Cyperaceae/good2dou/releases) page.
2. Unzip the downloaded file.
3. Go to `chrome://extensions`, enable **Developer mode**, click **Load unpacked**, and select the unzipped folder.

### Firefox

Install directly from [Firefox Add-ons](https://addons.mozilla.org/en-US/firefox/addon/good2dou/).

Alternatively, for manual installation:

1. Download the latest `good2dou-firefox-*.zip` from the [Releases](https://github.com/Cyperaceae/good2dou/releases) page.
2. Go to `about:debugging#/runtime/this-firefox`, click **Load Temporary Add-on...**, and select the downloaded ZIP file.
3. Alternatively, package or install it permanently via `about:addons`.

### Tampermonkey

Install directly from [Greasy Fork](https://greasyfork.org/en/scripts/554760-good2dou), or grab the latest `good2dou.user.js` from the [Releases](https://github.com/Cyperaceae/good2dou/releases) page and drag it into your browser with Tampermonkey installed.

## Features

- Extracts book metadata from Goodreads pages.
- Autofills the corresponding fields on Douban's new subject submission page.
- Downloads the book cover directly on Douban's subject submission page.

## Changelog

See [CHANGELOG.md](./CHANGELOG.md) for the full version history.

## Development

This project has three build targets kept in sync under one version number:

- `chrome/` — Chrome/Edge extension (Manifest V3)
- `firefox/` — Firefox extension
- `tampermonkey/` — Userscript for Tampermonkey / Greasy Fork

To release a new version:

```bash
node scripts/sync-version.js <version>
git add . && git commit -m "chore: sync version to <version>"
git push
git tag v<version>
git push origin v<version>
```

The tag push triggers a GitHub Actions workflow that syncs the version into all three targets, packages the Chrome and Firefox builds, and creates a GitHub Release with the artifacts attached.

## License

This project is licensed under the [GNU GPLv3](LICENSE) License.
