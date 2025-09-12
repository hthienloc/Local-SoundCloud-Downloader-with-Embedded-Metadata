# Local SoundCloud Downloader (Userscript)

Download SoundCloud tracks directly in your browser without external services.  
This userscript fetches the progressive MP3 stream, embeds metadata (title, artist, album), and attaches cover art (if available) into the MP3 file before saving.

## ✨ Features
- Adds a **Download** button on SoundCloud track pages.
- Downloads MP3 files directly (progressive stream).
- Embeds ID3 metadata:
  - Title (track title)
  - Artist (SoundCloud author)
  - Album (if available)
  - Cover art (if available)
- Uses [StreamSaver.js](https://github.com/jimmywarting/StreamSaver.js) to support large files.

## ⚠️ Limitations
- Entire MP3 file is loaded into memory before saving (needed to inject ID3 tags). Large files may consume significant RAM.
- Cover art fetch may fail due to **CORS restrictions**. In that case, file downloads without cover.
- Only works on SoundCloud track pages (not playlists, stations, etc.).

## 📦 Installation
1. Install a userscript manager:
   - [Tampermonkey](https://www.tampermonkey.net/) (recommended)
   - [Violentmonkey](https://violentmonkey.github.io/)
2. Install this script:  
   - [Raw GitHub script link](https://raw.githubusercontent.com/hthienloc/Local-SoundCloud-Downloader-with-Embedded-Metadata/main/LocalSoundCloudDownloader.user.js)

## 🛠 Development
- Script entry point: `LocalSoundCloudDownloader.user.js`
- Update `@version` in header when releasing new versions.
- Push to GitHub and/or update on Greasy Fork.

## 📄 License
MIT — see [LICENSE](LICENSE).
