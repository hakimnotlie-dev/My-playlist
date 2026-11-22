QR MUSIC PLAYER — STARTER PROJECT

1. Put your audio files in the songs/ folder.
2. Edit the playlist array near the bottom of index.html to list each song and its cover image.
   Put cover images in the cover/ folder and set the matching path in the cover property.
   Example:
   { title: "My Song", artist: "Artist Name", src: "songs/my-song.mp3", cover: "cover/my-song.jpg" }
   Each song automatically uses a two-color gradient sampled from its cover.
   The cover property is optional; songs without it show the music-note placeholder.
   Artist cards appear above the tracklist. By default, portrait files in artists/ use
   the artist name in lowercase with spaces replaced by hyphens and a .jpg extension.
   For different filenames or formats, add the artist name and image path to the
   artistCovers object below the playlist in index.html. Yonkagor's existing image is
   configured there as artists/Yonkagor.webp. If no artist image is found, the song
   cover is used instead.
   Scroll below the player to browse playlist cards with each song's cover, title,
   and artist. Selecting a card loads the track without starting playback. To add a
   song manually, copy a playlist entry and update its title, artist, audio path, and
   cover path. Put the audio in songs/ and its cover in cover/. For a new artist,
   place their portrait in artists/ and add its path to artistCovers.
   Click a song's details to select it. Drag a song card outside the playlist to move it
   freely; its playlist slot and song name read Blank until you drag the card back into
   the list.
   Drag cards onto one another to reorder the playlist. Double-click a playlist card
   to pop out the whole card; double-click its cover to pop out the sleeve. The sleeve
   moves independently, and double-clicking a floating card body repeats its pop
   animation. Click the sleeve to eject the record, then drag the record onto
   the turntable to play or back onto its sleeve to return it. The player has no separate
   sleeve beside the turntable. The page uses a neutral theme until a record is on the
   turntable, then switches to that song's theme; removing the record restores the neutral
   theme. Drag song cards onto one another to reorder the playlist. The reordered list is
   saved in this browser. The record stays on the platter when paused. A tonearm swings
   onto the record during playback and parks when paused. Enable Auto-next to start each
   following song automatically (wrapping to the first track at the end), or use Random to
   immediately play a different random track.
   Ambient effects are track-specific: drag the rain-swept leaves on the first track
   or any floating shape on the heart-themed track to move them around. The third
   track uses a milky white and rosy pink palette. After the final song ends, use the
   Autoplay playlist button to start again from the first song.
   The fourth song, "So Long," has larger flickering, star-shaped gold stars, a burst
   of three fast star-shaped shooting stars following one path with long fading trails,
   and a smaller, raised gold train with seven straight, joined blue cars, warm-lit
   windows and headlights, a complete locomotive head, gold lower trim, and
   spinning wheels passing very slowly once
   every two minutes along a smaller straight track in the background.
   Reduced-motion settings disable movement.
   Audio is preloaded to reduce startup wait.
   The Original lyrics and Translation panels can each be moved by dragging anywhere
   except their controls, and resized from the bottom-right handle (or with arrow keys
   after focusing it); their positions and sizes are saved in this browser. Use each
   panel's Edit button to paste plain text or timestamped LRC lines such as
   [00:12.50] Your lyric line, then select Apply. Edited lyrics are saved separately
   in this browser for each song. Use Write to index.html to choose the project file
   and embed that lyric version in the selected song's playlist entry. This clears
   that lyric type's external file reference so the embedded lyrics load on future
   visits. Only songs already listed in the file can be written this way. Timestamped
   LRC lines highlight accurately as the song plays. Lyrics turn white during playback
   and dim again when paused;
   plain-text lyrics do not highlight individual lines without timestamps.
   Lyrics are hidden by default. Use the Show lyrics menu to choose the original,
   translation, both, or neither; each panel's × button closes it, and closing one
   while both are shown leaves the other open. Manual choices are saved in this
   browser. Inactive lyric lines are dimmed, while the active timestamped line is
   white.
   The first song's default lyrics are stored in
   `lyrics/linger-in-the-rain-original.txt` and
   `lyrics/linger-in-the-rain-translation.txt`. Configure file-backed lyrics with
   `lyricsFile` and `translatedLyricsFile` in a playlist entry. Files load when
   that browser has no saved edit; browser edits take precedence. The first song
   also has built-in playlist copies as a fallback if the browser blocks reading
   the text files. Keep those arrays in sync if you edit the default lyric files.
   Other songs can use `lyrics` and `translatedLyrics` arrays. The saved files are
   plain text. Add LRC timestamps such as `[00:12.50] Your lyric line` to sync
   lines accurately; every line needs a timestamp for consistent highlighting.
3. Opening `index.html` directly uses `songs/embedded-audio.js` for playlist tracks
   so playback works without a local server. To play a manually added song this way,
   add its audio data to that file as a base64 entry. Alternatively, run
   `py -m http.server 8000` from this folder and open http://localhost:8000 to play
   audio files directly from songs/.
4. To share the player with GitHub Pages:
   - Create a GitHub repository and add the contents of this folder to its root
     (index.html, songs/, cover/, artists/, and lyrics/).
   - In the repository, open Settings > Pages, choose deployment from a branch,
     select the main branch and root folder, then save.
   - Once GitHub Pages finishes publishing, open the URL it provides. The repository
     file viewer is not the player; use the Pages website URL to listen and share.
   Keep filenames and capitalization exactly as they are because published paths are
   case-sensitive. The website and its audio files will be public to anyone with the URL.
5. Open the published website and use the Share / QR button to copy its URL,
   view its QR code, or download the QR code as a PNG.

Notes:
- Use audio files you own or have permission to distribute.
- Phones usually require the listener to tap Play; browsers commonly block autoplay with sound.
- Keep filenames simple (letters, numbers, hyphens) and match capitalization exactly.
