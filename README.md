# Song ID prop (Snapdragon)

Mock Shazam-style song-recognition app for film, built from the Figma frame "Shazam App - Open Screen" (Snapdragon_UI_kimi_NIL-20261023a, node 112:6024). Tap the red half: the Snapdragon logo beats like a heart and the rings pulse outward while it listens. Then the song is found and the right half fills in: the header and bottom nav, then the title, the album cover, "Let’s Go to the Top" and the Open song button. The square album cover (`cover.jpg`, 1200 × 1200) sits above the title. The lyrics card is hidden for now; its English lyrics for Funiculì, Funiculà are still in the code. Tap the logo again to reset for the next take. There's no audio; a timer drives the lyrics. The song is public domain (Denza / Turco, 1880); the English lyrics are the prop's own translation, and their timings are estimates until the production's recording is known.

Target size: Galaxy Z Fold 8 inner screen unfolded, 2448 × 1848 px, landscape. Every size is the Figma frame's px scaled to the screen, so it also fits other sizes. Landscape screens show the two halves side by side; portrait or narrow screens stack the listen area over the player. Not yet checked on a real Fold. Single static file: `index.html`. Pushes to `main` redeploy on Vercel.

## Full screen on the Fold
- **Best:** open the site in Chrome or Samsung Internet, then use the menu's **Add to Home screen** (or **Install app**). Opened from the home-screen icon, it runs full screen with no address bar or navigation bar.
- **In the browser:** the first tap asks the phone to go full screen and keeps the screen from dimming.

## On set
- **Tap the red half** to listen · **tap the logo** or the **home icon** to reset · **Open song** starts the lyrics · tap the heart to favourite
- Keyboard: **Space** listen, then start / pause the lyrics · **R** or **Esc** reset
- URL options: `?listen=6` listening time in seconds (default 4.6) · `?status=1` shows a mock status bar (time and connection icons; hidden by default, with space left at the top for the device's own) · `?hint=0` hides the "Tap to identify" / "Listening…" text

Edit the title, subtitle and lyric lines (with seconds per line) in `SONG` and `LYRICS` at the top of the script.
