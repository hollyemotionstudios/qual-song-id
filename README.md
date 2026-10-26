# Song ID prop (Snapdragon)

Mock Shazam-style song-recognition app for film, built from the Figma frame "Shazam App - Open Screen" (Snapdragon_UI_kimi_NIL-20261023a, node 112:6024). Tap the red half: the Snapdragon logo beats like a heart and the rings pulse outward while it listens. Then the song is found and the right half fills in: the title, then the play button, then the rest of the UI. English lyrics for Funiculì, Funiculà start at "…to see the sky!" and loop through the whole song. Tap the logo again to reset for the next take. There's no audio; a timer drives the lyrics. The song is public domain (Denza / Turco, 1880); the English lyrics are the prop's own translation, and their timings are estimates until the production's recording is known.

Target sizes (Galaxy Z Fold 8). Every size is the Figma frame's px scaled to the screen, so it also fits other sizes. Not yet checked on a real Fold.
- **Folded / cover screen, 1248 × 1972 px (portrait):** the red listen screen fills the display. When the song is found it shrinks to a band at the top (logo, rings, "Song Found" header) and the player rises beneath it. Any portrait screen, including the inner screen held upright, uses this layout.
- **Unfolded / inner screen, 2448 × 1848 px (landscape):** the two halves side by side, as in Figma. Single static file: `index.html`. Pushes to `main` redeploy on Vercel.

## Full screen on the Fold
- **Best:** open the site in Chrome or Samsung Internet, then use the menu's **Add to Home screen** (or **Install app**). Opened from the home-screen icon, it runs full screen with no address bar or navigation bar.
- **In the browser:** the first tap asks the phone to go full screen and keeps the screen from dimming.

## On set
- **Tap the red half** to listen · **tap the logo** (or the back arrow) to reset · **play/pause button** pauses the lyrics · tap the heart to favourite
- Keyboard: **Space** listen / pause · **R** or **Esc** reset
- URL options: `?listen=6` listening time in seconds (default 4.6) · `?status=0` hides the fake status bar · `?hint=0` hides the "Tap to identify" / "Listening…" text

Edit the title, subtitle and lyric lines (with seconds per line) in `SONG` and `LYRICS` at the top of the script.
