CUEVAULT VIDEO PLAYBACK FIX

WHAT WAS WRONG
- The earlier Blogger embed used placeholder URLs (YOUR_PUBLIC_MEDIA_HOST), so its players could not find actual video files.

BEST OPTION (RECOMMENDED)
1. Download CueVault-Storefront-Bundle.zip and extract it.
2. Upload the entire CueVault-Storefront folder contents to a static host such as GitHub Pages or Netlify. Upload index.html AND the complete assets/ folder.
3. The video files must remain at assets/videos/automatic-tool-demo.mp4 and assets/videos/cueball-prediction-demo.mp4 relative to index.html.
4. Open the published HTTPS page and tap each player's play control. Videos do not autoplay.

BLOGGER OPTION
- CueVault-Blogger-Embed.html now embeds both video files directly and does not contain fake placeholder URLs.
- This makes the HTML much larger and can cause a slow page load or a save/render timeout on some connections. If Blogger accepts it, preview the published page on Android, iPhone and desktop.
- If Blogger strips the videos or the page is too slow, host the complete website as described above and link to it from Blogger. This is the more reliable production setup.

COMPATIBILITY
- Videos were encoded as MP4 with H.264 Constrained Baseline, 8-bit yuv420p and fast-start metadata to maximize support on common current browsers and phones.
- No web video can be promised to play on literally every device: old browsers, unsupported system codecs, data-saving modes, browser extensions, connectivity, or host/CDN settings can still prevent playback.
- The page shows an “Open the video directly” fallback if the embedded player reports a playback error.

CHECKS
- Both MP4s were inspected with ffprobe and tested in Chromium with playback metadata loaded. This does not substitute for testing on your own published Blogger page and physical phones.
