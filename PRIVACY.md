# MusicBridge privacy

MusicBridge reads the current track title, artist, album, album artist, duration, playback position, and playback state from the Music app on your Mac while sharing is enabled.

- Activity metadata is sent to the Discord desktop app through a local IPC connection. Discord then displays your activity according to your account settings.
- Album and album artist are sent to public Apple Music search pages to find artwork. Fallback requests send title, artist, and album search terms to Apple's public iTunes Search API. Results are matched against track metadata. Artwork is loaded from Apple's image servers.
- Matching artwork URLs are cached temporarily in memory, not as a listening-history database.
- Application ID, sharing preference, and status-display preference are stored locally using macOS preferences. Launch at login is managed by macOS.
- MusicBridge does not request a Discord account token, bot token, password, or Apple Music account password.
- MusicBridge has no analytics service, listening-history database, or developer-operated backend.

Turning off sharing disconnects the Discord presence connection. An artwork lookup already in progress, including its fallback requests, may finish after sharing is turned off. Pausing or stopping Music clears the activity at the next successful update. Quitting closes the local Discord connection.

Apple, Discord, and GitHub process requests to their respective services under their own privacy policies. Downloading releases and submitting issues on GitHub are separate from the app's runtime behavior. Do not include passwords, tokens, or private listening data in public issue reports.

MusicBridge also reads embedded artwork directly from the Music app for its local preview. This artwork is kept in memory and is not uploaded. Discord artwork still requires a matching public image URL; local-only covers are not shared automatically. Catalog matches trigger an immediate refresh when a match becomes available.
