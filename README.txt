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
   and artist. Selecting a card loads the track without starting playback.
   Use Add song in the playlist header to add a title, audio file, song cover, and
   artist. Choose an existing artist to reuse their artwork, or add a new artist and
   portrait. Save to project asks you to select this project folder, then writes the
   files to songs/, cover/, and (for a new artist) artists/, and updates index.html.
   It also updates songs/embedded-audio.js so the new track plays when index.html is
   opened directly. Existing songs previously saved in this browser remain local to it.
   The album cover is a separate, draggable sleeve beside the turntable. When the record is
   inside, it follows the sleeve as you move it around the screen. Drag the sleeve aside
   to reveal the record. Click the sleeve to pop out the record, then drag it onto the
   turntable to play or back onto the sleeve to return it. Clicking or moving the sleeve
   won't start or pause playback; use the play control to pause. The sleeve tilts while
   the record is out, lifts larger while grabbed, and settles back when released. The
   whole turntable deck is a forgiving drop target. The record stays on the platter
   when paused. Changing songs loads the next record into its sleeve, so eject and place
   it on the platter to play. A tonearm swings onto the record during playback and parks
   when paused. During playback the album art is prominent on the record label, and the
   sleeve layers above the record if moved over it. The turntable colors follow the song
   cover. Enable Auto-next to start each following song automatically (wrapping to the
   first track at the end), or use Random to immediately play a different random track.
   Ambient effects are track-specific: drag the rain-swept leaves on the first track
   or any floating shape on the heart-themed track to move them around. The third
   track uses a milky white and rosy pink palette. After the final song ends, use the
   Autoplay playlist button to start again from the first song.
   Audio is preloaded to reduce startup wait.
   The Original lyrics and Translation panels can each be moved by dragging anywhere
   except their controls, and resized from the bottom-right handle (or with arrow keys
   after focusing it); their positions and sizes are saved in this browser. Use each
   panel's Edit button to paste plain text or timestamped LRC lines such as
   [00:12.50] Your lyric line, then select Apply. Edited lyrics are saved separately
   in this browser for each song. Use Write to index.html to choose the project file
   and embed that lyric version in the selected song's playlist entry. This clears
   that lyric type's external file reference so the embedded lyrics load on future
   visits. Only songs already listed in the file can be written this way; songs added
   in the browser remain browser-local. Timestamped LRC lines highlight accurately as
   the song plays. Lyrics turn white during playback and dim again when paused;
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
3. Opening `index.html` directly uses `songs/embedded-audio.js` for the playlist
   tracks so playback works without a local server. This generated file contains
   copies of the audio and grows by about one-third of each added audio file's size
   because of base64 encoding. Add song updates it automatically. Alternatively, run
   `py -m http.server 8000` from this folder and open http://localhost:8000 to use
   the original MP3 files instead.
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
