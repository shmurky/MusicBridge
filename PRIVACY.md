# MusicBridge privacy

MusicBridge reads the current track title, artist, album, duration, playback position, and playback state from the Music app on your Mac while sharing is enabled.

- Activity metadata is sent to the Discord desktop app through a local IPC connection. Discord then displays your activity according to your account settings.
- The current title and artist are sent to Apple's public iTunes Search API to find album artwork. Results are matched against the title, artist, and album. Artwork is loaded from Apple's image servers.
- Matching artwork URLs are cached temporarily in memory, not as a listening-history database.
- Application ID, sharing preference, and status-display preference are stored locally using macOS preferences. Launch at login is managed by macOS.
- MusicBridge does not request a Discord account token, bot token, password, or Apple Music account password.
- MusicBridge has no analytics service, listening-history database, or developer-operated backend.

Turning off sharing disconnects the Discord presence connection. A catalog request already in flight may finish; no further catalog searches start while sharing is off. Pausing or stopping Music clears the activity at the next successful update. Quitting closes the local Discord connection.

Apple, Discord, and GitHub process requests to their respective services under their own privacy policies. Downloading releases and submitting issues on GitHub are separate from the app's runtime behavior. Do not include passwords, tokens, or private listening data in public issue reports.

MusicBridge also reads embedded artwork directly from the Music app for its local preview. This artwork is kept in memory and is not uploaded. Discord artwork still requires a matching public image URL; local-only covers are not shared automatically. Catalog matches trigger an immediate refresh instead of waiting for the next five-second poll.
