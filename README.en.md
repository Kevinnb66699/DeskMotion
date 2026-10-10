# DeskMotion

[中文](README.md) | English

A live wallpaper player for macOS: set a video, image, GIF or web page as your desktop wallpaper, playing full screen beneath your desktop icons.

Version 1.4.1 · Requires macOS 14 or later · Runs on Macs with Apple silicon and Intel processors

## Installing and opening for the first time

The installer is on the download page https://deskmotion.jiling.chat/ — please download it with a browser such as Safari or Chrome. When a friend installs DeskMotion for the first time, just send them this link (don't forward the installer through a chat app; see "The application can't be opened" in the FAQ for why).

1. Double-click `DeskMotion-1.4.1.dmg` and drag **DeskMotion** to the Applications folder (labeled "应用程序" in the installer window).
2. Double-click DeskMotion in Applications to open it.
3. If macOS says the app can't be opened, or that the developer can't be verified:
   - Open System Settings → Privacy & Security, find the message about DeskMotion near the bottom, click "Open Anyway" and enter your password to confirm.
   - On macOS 14 you can also **right-click** DeskMotion in Applications and choose "Open".
   - You only need to do this once; after that DeskMotion opens normally. The message appears because DeskMotion isn't notarized by Apple (that requires a paid developer account); it doesn't mean anything is wrong with the file.
   - If the message is “The application “DeskMotion” can’t be opened.” and Privacy & Security has no "Open Anyway", see "The application can't be opened" in the FAQ below.
4. DeskMotion doesn't stay in the Dock; it shows a small TV icon in the menu bar at the top of the screen. The first time it opens, the "DeskMotion Library" window appears on its own.

You can also use the installer package `DeskMotion-<version>.pkg` instead (it's on the download page too):

- Double-click it and follow the steps; it asks for an administrator password. It always installs to the Applications folder and replaces the same or an older DeskMotion there (a newer one is left as it is); a running DeskMotion quits first, and the new one opens when the installation finishes.
- The installer isn't signed with an Apple developer certificate either, so macOS blocks it the first time you double-click it: close the message, open System Settings → Privacy & Security, click "Open Anyway" near the bottom and enter your password to confirm (on macOS 14 you can also **right-click** the installer and choose "Open"). You only need to approve it this once; the installed DeskMotion doesn't need approving again.

## Using DeskMotion

### Opening the library

Click the DeskMotion icon in the menu bar → "Open Library". While the library or settings window is open, DeskMotion appears in the Dock for the time being and shortcuts such as ⌘H, ⌘W and ⌘Q work; the icon goes away once all its windows are closed.

### Importing wallpapers

- **Drag files or folders into the library window**, or click "Import Files…" in the toolbar.
- For an online web page, click "Add URL…" and enter an address that starts with `http://` or `https://`.
- Imported files are **copied** into the library, so moving or deleting the originals afterwards doesn't affect them.
- Videos that need converting show their progress at the bottom of the window; click "Cancel Import" to stop while they convert.

### Setting a wallpaper

- **Double-click** a wallpaper card to make it the wallpaper of the selected display. Click a display in the "Displays" panel on the right to select it.
- **Right-click** a wallpaper card for "Set as Wallpaper for “display”", "Apply to All Displays", "Show in Finder", "Rename…" and "Delete…".
- Each display has its own settings:
  - **Scaling**: Fill (the default; fills the screen and crops what doesn't fit), Fit (shows the whole picture with black bars at the sides), Stretch, and Center (original size). Web wallpapers lay out their own pages, so this setting doesn't apply to them.
  - **Mute** and **Volume** (video and web wallpapers).
  - **Clear Wallpaper**: goes back to the system wallpaper.
- When you connect or disconnect displays, each screen gets its own settings back automatically.
- A display you connect for the first time shows the same wallpaper or playlist as the main display, with the same scaling, and starts muted; you can change it in the "Displays" panel afterwards. If the main display has no wallpaper, it copies another display that has one; with the lid closed and only an external display in use, a display connected for the first time has nothing to copy, so choose a wallpaper for it in the panel. Displays connected before keep their settings; one that an earlier version left without a wallpaper, and that you never set up, also copies the main display the next time you connect it after updating to 1.4 (if you had cleared it on purpose, clear it once more; it then stays cleared).

### Playlists and rotation

Put several wallpapers in a playlist to rotate them automatically.

- **Create one**: switch to "Playlists" at the top of the library window and click "New Playlist" (the + button); or right-click a wallpaper card → "Add to Playlist" → "New Playlist…".
- **Add and reorder**: click "Add Wallpapers…" in the playlist to choose several, or right-click a wallpaper card → "Add to Playlist". Drag the thumbnails to change the order.
- **Switching** (set separately for each playlist):
  - **Interval**: switch every 1 minute up to every 24 hours, in order or shuffled (when shuffled, every wallpaper comes up once per round).
    - "Let videos play to the end before switching": when it's a video's turn, it plays through once before the next one.
    - "Switch when unlocking or starting up": moves on to the next wallpaper each time you unlock the screen or DeskMotion starts.
  - **Time of Day**: pick one wallpaper each for Morning, Day, Evening and Night; the start times can be adjusted, and wallpapers switch on time automatically.
- When **several displays** use the same playlist, choose "Switch together (same wallpaper on every display)" or "Each display on its own".
- **Use it on a display**: in the "Displays" panel on the right, set "Content" to "Playlist" and choose the playlist; or right-click it on the Playlists page → "Set as Playlist for “display”".
- The panel shows which wallpaper is on and when the next switch is, and has a "Next" button; the menu bar menu also has "Next Wallpaper".
- Rotation follows real time: it still switches on schedule while wallpapers are paused (on battery, screen locked and so on), and after DeskMotion restarts it carries on where it left off.

### Sound

Video and web wallpapers play sound by default, but **only the main display plays sound by default**; other displays start muted so several soundtracks don't mix, including a newly connected display that copies another one (even if it becomes the main display). "Mute All" in the menu bar mutes every wallpaper at once.

### Pausing and automatic pausing

- Menu bar → "Pause Playback" pauses all wallpapers; click "Resume Playback" to continue.
- DeskMotion pauses automatically in the situations below to save battery and performance. Each one can be turned off under menu bar → "Settings…" → "Pause Automatically":
  - When a full-screen app covers the desktop (only the covered display pauses)
  - When a maximized window covers the desktop (see below)
  - When on battery power
  - When the screen is locked or asleep (this pauses only the desktop; macOS draws the lock screen, so to play wallpapers there turn on "Play wallpapers on the lock screen" below, which needs macOS 26 or later)
  - When Low Power Mode is on
  - When the Mac is too hot (all wallpapers pause when the system reports serious heat and starts throttling, and resume once it has cooled down)
- "When a maximized window covers the desktop": when a window fills everything on a display except the menu bar and the Dock (the small gaps left by tiled windows count too), that display's wallpaper pauses. It's independent of "When a full-screen app covers the desktop": with that one turned off, full-screen apps don't pause the wallpaper through this one.
  - Exceptions: when the Dock hides automatically or is on another display, a window filling the screen is exactly the size of a full-screen app and is treated as one; when the menu bar is set to show in full screen as well, full-screen apps are treated as windows filling the screen.
- While paused automatically, the menu bar menu shows "Paused:" and the reason.

### Opening at login

Menu bar → "Settings…" → turn on "Open at login". DeskMotion then starts when you log in and brings back your last wallpapers.

### Interface language

DeskMotion has a Simplified Chinese and an English interface. By default it follows the system: if Simplified Chinese comes before English in your preferred languages under System Settings → General → Language & Region, it's shown in Chinese; otherwise in English.

To choose a language just for DeskMotion, go to menu bar → "Settings…" → "General" → "Language", choose "简体中文" or "English", then click "Reopen Now" (DeskMotion quits and opens again by itself), or wait until it next opens. Setting a language for DeskMotion under System Settings → General → Language & Region works too; both places change the same setting.

### Syncing with the system wallpaper

On by default (menu bar → "Settings…" → "Sync with system wallpaper"). DeskMotion sets a frame of the current wallpaper as the macOS system wallpaper, so the lock screen, Mission Control and the menu bar colors match your desktop:

- Videos use a frame near the start, GIFs their first frame, web pages what they show once loaded, scenes playing live their current frame, and images the original picture, each fitted with that display's scaling. Syncing the same wallpaper with the same settings again reuses the earlier picture.
- Turning this off, clearing a display's wallpaper or quitting DeskMotion brings back your original system wallpaper. If you chose a different wallpaper in System Settings in the meantime, DeskMotion leaves your choice alone.
- On macOS 26, if your original wallpaper is a dynamic one such as an aerial, or other desktop Spaces show the synced picture, turning this off or quitting rewrites the system's wallpaper settings and restarts the system wallpaper service once (the desktop briefly flickers), so every Space and display gets its original back, aerials still moving. Logging out or shutting down doesn't restart the service: an original picture comes back on the current Space only, and a dynamic wallpaper such as an aerial keeps the synced picture for now (it could only come back as a still then); the rest follows later (the next time DeskMotion opens with syncing off, or the next time you turn syncing off or quit).
- Earlier versions may have left synced pictures on other desktop Spaces. On macOS 26, "Settings…" then shows "Replace the DeskMotion stills left on other desktop Spaces with the current system wallpaper"; click "Replace" to switch them to the wallpaper currently chosen in System Settings.
- Known limitations (macOS versions other than 26):
  - macOS only lets apps change the system wallpaper of the current Space; DeskMotion sets the others when you switch to them, and when quitting it can only restore the current Space.
  - If your original system wallpaper was one of macOS's dynamic aerial wallpapers, the system only provides a still image of it, so it comes back as a still. To get the motion back, choose it again in System Settings → Wallpaper.

### Playing wallpapers on the lock screen (macOS 26 and later)

macOS draws the lock screen itself, and DeskMotion's windows can't be seen while the screen is locked, so normally the lock screen only shows the still picture set by "Sync with system wallpaper". On macOS 26 and later, DeskMotion can be a system wallpaper of its own, which plays video wallpapers on the lock screen (and, if you like, as the screen saver):

1. Menu bar → "Settings…" → "Lock Screen": turn on "Play wallpapers on the lock screen".
2. DeskMotion makes itself the system wallpaper of every desktop Space and display; there's no need to visit System Settings. The system wallpaper service restarts, so the desktop briefly flickers; once "Lock Screen" shows "Active", you're set. Your screen saver stays as it was.
3. (Optional) To have the screen saver play too, choose "DeskMotion" in System Settings → Screen Saver.

If it can't set itself up (the system wallpaper service didn't accept it, say, or the macOS version hasn't been verified yet), DeskMotion opens System Settings → Wallpaper, with a small hint floating above it that shows how to choose it: scroll down to the "DeskMotion" section and click "DeskMotion" in it. The hint closes by itself once you have; where DeskMotion can write the system wallpaper settings, it then sets up your other displays and desktop Spaces too (the system wallpaper service restarts once more); otherwise choose it for each display, then switch to each Space and choose it there too.

Then:
- Video wallpapers (including GIFs you converted to videos) loop on the lock screen (and in the screen saver, if you chose DeskMotion there); images, GIFs, web pages and scenes show a still picture. Each display shows its own wallpaper.
- On the desktop DeskMotion keeps playing as usual; after you quit DeskMotion the desktop shows a still picture, while the lock screen keeps playing.
- "Sync with system wallpaper" can stay on: it pauses while lock screen playback is on, so it doesn't set a still picture over DeskMotion. The stills it had set are replaced when DeskMotion sets itself up, and turning lock screen playback off brings back the wallpaper you had before syncing.
- "Pause Playback", and the automatic pauses "When on battery power", "When Low Power Mode is on" and "When the Mac is too hot" (while turned on), also make the lock screen show just the still picture.
- To stop: turn off "Play wallpapers on the lock screen", and DeskMotion brings back your original wallpaper on every Space and display (the system wallpaper service restarts once more); your screen saver stays as it is. If DeskMotion couldn't set itself up and you chose it in System Settings yourself, it sometimes can't be undone (on a macOS version that hasn't been verified, say): DeskMotion then asks you to choose another wallpaper in System Settings → Wallpaper.
- If you choose another wallpaper in System Settings → Wallpaper (even with "Show on all Spaces" turned off), DeskMotion doesn't fight you: it turns off "Play wallpapers on the lock screen" (and "Sync with system wallpaper" if it was on, so it doesn't put a still over your choice), and says so once under "Settings…" → "Lock Screen". Spaces where you didn't choose it keep DeskMotion's still picture: choose your wallpaper there too, or turn lock screen playback on and off once, which brings back the originals there and keeps your choice. Another app changing the wallpaper of one Space only (a full-screen app's, say) isn't a choice of yours: "Play wallpapers on the lock screen" stays on, and DeskMotion sets that Space back the next time it starts.
- Full-screen apps' Spaces have wallpaper settings of their own, which choosing a wallpaper in System Settings doesn't reach. When DeskMotion opens and finds a Space (a full-screen app's included) or a display that doesn't show it, it sets those up too (the system wallpaper service restarts once, so the desktop flickers); when every Space shows it, it changes nothing.

Known limitations:
- The display usually turns off 30 seconds to a minute after locking, so what you see is mostly the moments after locking and after waking it.
- This uses interfaces macOS doesn't document. A major macOS update may break it (the lock screen then shows a still picture or goes black); choose another wallpaper in System Settings → Wallpaper if that happens, and look out for a DeskMotion update.
- FileVault's login screen at startup isn't covered; macOS 14 and 15 aren't supported (the switch is grayed out).
- Videos with a rotation flag (portrait phone videos, for example) show in their stored orientation on the lock screen.

### Web wallpapers and the mouse

Web wallpapers only follow the mouse as it moves, which is enough for effects such as parallax or things that follow the pointer. They don't receive clicks, so buttons and links in the page can't be clicked, and clicking the desktop and the desktop icons works as usual.

### Wallpaper Engine wallpapers

DeskMotion can import Wallpaper Engine video, web and scene wallpapers directly; scenes play live once you give DeskMotion Wallpaper Engine's assets (a preview: some things aren't drawn yet, see below), and show a still picture until then:

- **Import a project folder**: drag a project folder that contains `project.json` into the library (or choose it with "Import Files…"). Video projects import their video (converted if needed, as usual); web projects are imported as web wallpapers; scenes are described below. The wallpaper is named after the project's title, and the project's preview becomes its thumbnail (for scenes, the imported picture does).
- **Import a whole Workshop folder**: drag in a folder with many project subfolders (such as Steam Workshop's content folder) to import all its video, web and scene projects at once, skipping the unsupported ones. When everything is done, a dialog tells you how many were imported, which were skipped and why.
- **Scene wallpapers**: when importing, DeskMotion stacks the scene's layers (image, solid-color and puppet layers) in order into one still picture, with their colors, opacity, tints and masks, and imports it as a still image wallpaper; a scene that is just one video is imported as a video wallpaper. While a scene isn't playing live, wallpaper cards and the "Displays" panel show a "Static" tag: effects, particles, text, animation and reactions to the mouse and sound are left out. For live playback, see "Scenes played live (preview)" below.
  - When no usable picture comes out (for example, the scene is mostly particles, effects, text or video, or a texture format isn't recognized), the project's preview is used instead; with no preview either, the import fails with "This scene has no background picture to show".
  - You can also drag in a `scene.pkg` file on its own. A .pkg that isn't a Wallpaper Engine package (such as a macOS installer) gets "This isn’t a Wallpaper Engine scene.pkg".
  - The scene's original files (project.json, scene.pkg and the preview) are kept in the library too; live playback uses them.
  - For what live playback can't draw yet (such as clocks and other text, or the scene's own videos), record the scene as a video on Windows and import that; see "How do I make scene wallpapers move?" in the FAQ.
- **Scenes played live (preview)**: DeskMotion renders scene wallpapers in real time with its own engine. That needs Wallpaper Engine's own `assets` folder (the shaders, materials and effects scenes share), which DeskMotion doesn't ship.
  - On a Windows PC with Wallpaper Engine, it's in your Steam library at `steamapps\common\wallpaper_engine\assets` (in Steam, right-click Wallpaper Engine → "Manage" → "Browse local files" to open the `wallpaper_engine` folder). Copy the whole `assets` folder (about 80 MB) to this Mac (a USB drive, cloud storage or a network share all work).
  - Menu bar → "Settings…" → "Wallpaper Engine Scenes" → "Wallpaper Engine assets": click "Choose…" and select the `assets` folder (the `wallpaper_engine` folder that contains it, or Steam's `common` folder, work too). DeskMotion copies it into its own data folder (`~/Library/Application Support/DeskMotion`) and shows "Ready" with its size; you can delete the original afterwards. If you pick something else (or only part of the folder was copied), it tells you what to pick. "Remove…" deletes the copy once you confirm.
  - Once the assets are ready, scene wallpapers play live and their "Static" tag becomes "Live". To keep scenes still, turn off "Play scene wallpapers live (preview)" in the same place (it's on by default); scenes then show their imported still.
  - What's drawn so far: the scene's image, solid-color and puppet layers (puppets in their rest pose) with the scene's own shaders, so materials that change over time (such as flowing water) move; effects (such as blur, water ripples, shake, tints and masks), compose layers and blend modes; particles (such as rain, snow, fog, sparks and stars, including ones that follow the mouse or react to sound); bloom, camera shake, camera parallax following the mouse, keyframe (timeline) animations and sprite animations; effects that react to sound (such as audio bars, see "Audio-reactive wallpapers" below). At most 30 frames per second; a scene whose picture doesn't change with time stops drawing once it's drawn, until the mouse, the sound or a property changes it (a scene with particles that keep moving draws every frame). Automatic pausing (full screen, battery, locked screen and so on) applies as usual. Not supported yet: text (clocks and dates included), the scene's own videos and sounds, scripts (what a script controls stays as it starts, and a few script-driven effects aren't drawn), puppet bone animation, and lights; a few rarely used particle features (such as collisions) aren't done yet, and some particle effects don't quite match Wallpaper Engine in density, size or brightness. So some scenes differ quite a bit from Wallpaper Engine when played live (missing a clock, for example); later versions will fill these in.
  - A scene imported as a video (a scene that is just one video) still plays as that video.
  - If a scene fails to load, has nothing in it that can be drawn, the graphics card fails or is too slow for it, or the scenes playing live together would take more graphics memory than allowed (half of what the graphics card recommends), it goes back to its still (and is tried again after the Mac wakes from sleep, the next time DeskMotion opens, or after you choose the assets again).
- Other types (such as applications) aren't supported yet.
- **Wallpaper properties**: if a web wallpaper or a scene playing live has adjustable properties (sliders, colors, switches, menus, text), right-click its card → "Wallpaper Properties…". Changes take effect immediately and are saved automatically; "Restore Defaults" resets them.
- **Audio-reactive wallpapers**: web wallpapers that react to audio, and scenes playing live with effects or particles that react to sound (such as audio bars), move with the sound your Mac is playing. Whether a scene needs the sound depends on what it draws, including parts you can switch on in Wallpaper Properties; for scenes that don't, no sound is captured.
  - The first time this is needed, macOS asks for permission to record system audio; DeskMotion uses it only to make wallpapers move with the sound. If you deny it, the wallpaper still shows, it just doesn't react.
  - It requires macOS 14.2 or later (web and scene wallpapers alike).
  - For web wallpapers, only local ones (imported web files, folders and zip archives) can use it, not online URL wallpapers.
  - Sound is captured only while the wallpaper is showing and not paused (not while the screen is locked or asleep).

### Checking for updates and updating automatically

- DeskMotion checks for a new version when it starts and once a day after that (on the download site in China first, then on GitHub if that fails); it doesn't download anything or open a window by itself. If you don't want this, turn off "Check for updates automatically" under "Settings…" → "General". You can also check at any time with menu bar → "Check for Updates…".
- When there's a new version, a small red dot appears at the top right of the menu bar icon, you get a "DeskMotion x.y.z is available" notification (once per new version; the first time, macOS asks whether DeskMotion may send notifications, and the dot works either way), and "Update to Version x.y.z…" appears at the top of the menu bar menu. Click the notification or the menu item to read what's new in the "DeskMotion Update" window (the dot goes away once you have), then click "Update Now": DeskMotion downloads the new version (showing progress; you can cancel), verifies its signature, then quits, replaces itself and opens again. If any step fails, it tells you why and the old version keeps working.
- If DeskMotion isn't somewhere it can replace itself (for example, opened straight from the installer or the Downloads folder, or without write permission), the button changes to "Go to Download Page"; download the new installer in your browser and install it again. So keep DeskMotion in the Applications folder.
- You can't update while wallpapers are being imported; click "Update Now" once the import has finished.
- Known limitation: since DeskMotion isn't notarized by Apple, macOS treats it as a new app after every update, so the system audio recording permission for audio-reactive wallpapers has to be allowed once more.

## Supported formats

| Type | Formats | Notes |
|---|---|---|
| Video (plays directly) | mp4, m4v, mov | Uses the system's hardware decoding; the most power-efficient |
| Video (converted on import) | webm, mkv, avi, flv, wmv, ogv, ogg, mpg, mpeg, ts, m2ts, mts, 3gp, asf | Converted to mp4 (HEVC) on import, then played like any other video |
| Image | jpg, jpeg, png, heic, heif, webp, tiff, tif, bmp | Turned upright according to the orientation the photo records |
| Animated image | gif, animated webp, apng (extension .png or .apng) | Each frame plays for its own duration; large ones are converted to video on import (see the notes below) |
| Web page | a folder containing index.html, a single .html / .htm file, a .zip archive, an http / https URL | Compatible with Wallpaper Engine web wallpapers (uses the entry page named in project.json) |
| Wallpaper Engine project | a project folder containing project.json, a Workshop folder (imported all at once), a scene.pkg on its own | Video, web and scene projects; scenes play live (preview) once Wallpaper Engine's assets are given, and otherwise show a still picture of their layers (static); see "Wallpaper Engine wallpapers" above |

Notes:

- If the system can't play an mp4 / mov file directly (for example because it contains VP9 video), it's converted instead.
- Converting AV1 video needs a Mac with M3 or later; earlier Macs show "This Mac can’t decode AV1 video".
- Only the first video track and the first audio track are used; if the audio can't be decoded, only the picture is kept.
- WebP and PNG files are checked for frames on import: ones with several frames (animated WebP, APNG) are imported as animated images and play like GIFs; single-frame ones are imported as images.
- Large animated images (GIF, animated WebP or APNG taking more than 150 MB once decoded, such as 1080p with dozens of frames) are converted to video (HEVC) on import, and only the converted video is kept in the library. The bottom of the window shows "Converting" with the progress, and you can cancel it. The picture and every frame's duration stay the same; transparent areas become black.
- Large animated images imported earlier (GIFs, and animated WebP / APNG files imported as stills before 1.3, which DeskMotion recognizes as animated when it starts): right-click the wallpaper card → "Convert to Video (Saves Power)" (only large animated images have this item) and confirm; it converts at the bottom of the window. Afterwards its name, thumbnail and place on every display and in every playlist stay the same; if it fails or you cancel, it stays as it was.
- Steam Workshop scene wallpapers and scene.pkg files need Wallpaper Engine's assets to play live (preview), and text and clocks, scripts and the scene's own sounds and videos aren't supported yet; without the assets they show a still picture (see "Wallpaper Engine wallpapers" above). Other .pkg files (such as macOS installers) can't be imported.

## Resource usage

Measured on a 14-inch MacBook Pro (M5 Max, built-in display at 3024×1964): steady-state values with one wallpaper playing on one display. CPU is per core; 100% means one core fully used.

| Wallpaper | CPU | Memory |
|---|---|---|
| 4K video | about 9% (DeskMotion about 5%, the system's hardware decoding about 4%) | DeskMotion about 90 MB; the system's decoding service uses about 350 MB more for frame buffers |
| Web page (full-screen particle animation, 60 fps) | about 32% (mostly in the web page's process) | web page process about 320 MB |
| Large GIF (1080p, 60 frames), converted to video on import | about 3% (DeskMotion about 2%, the system's hardware decoding about 1%) | DeskMotion about 80 MB, the system's decoding service about 40 MB |
| The same GIF unconverted, decoded while playing (1.2 and earlier) | about 36% | about 400 MB |
| 4K image | almost 0 | — |
| Wallpaper Engine scene (played live, 30 fps) | under 1% for scenes whose picture doesn't move; about 1–14% for animated ones, depending on the scene | about 400 MB–1.8 GB, depending on the scene's textures and effects |
| Paused | 0 | DeskMotion about 160 MB |

- Video uses the system's hardware decoding and is the most power-efficient format; what a web wallpaper uses depends on the page itself.
- The scene figures were measured offscreen in a test program with 31 Workshop scenes (no window compositing), not in the app; the graphics card takes 0.04–4 ms per frame. A scene whose picture doesn't change with time stops drawing once it's drawn and draws again only when the mouse, the sound or a property changes, so it uses almost no CPU; animated scenes of just pictures and simple materials take about 1–3%; scenes with many effects (dozens of drawing passes a frame) or many particles (thousands to tens of thousands worked out on the processor every frame) take more, about 4–14% as measured, and a scene with particles that keep moving draws every frame and never stops. The CPU share moves with the processor's clock at the time, so two measurements of one scene can differ by a factor of two. Scenes with many textures use more memory, two displays showing the same scene each hold their own copy, and a paused scene keeps its textures in memory (the "Paused" row doesn't include them).
- GIFs that take up to 150 MB once decoded (such as 720p with dozens of frames) are decoded once and cached, so playing them uses almost no CPU. Larger GIFs can only be decoded while playing, which uses a lot more CPU, so they're converted to video on import and become as power-efficient as video wallpapers (see the table above). The same goes for animated WebP and APNG. Large GIFs imported earlier can be converted by right-clicking the wallpaper card → "Convert to Video (Saves Power)".
- While paused automatically (on battery, in full screen, with the screen locked and so on), DeskMotion uses almost no CPU. With "Play wallpapers on the lock screen" on, the system wallpaper extension decodes the video in hardware while the screen is locked, until the display turns off.

## Uninstalling

1. If you turned on "Open at login", turn it off in "Settings…" first (or remove DeskMotion under System Settings → General → Login Items).
2. If "Play wallpapers on the lock screen" is on, turn it off under "Settings…" → "Lock Screen" first, which brings back your original system wallpaper; if you chose DeskMotion in System Settings → Wallpaper yourself, choose another wallpaper there first.
3. Menu bar → "Quit DeskMotion". Quitting brings back your original system wallpaper (when "Sync with system wallpaper" is on).
4. Drag DeskMotion from Applications to the Trash.
   - The same goes if you installed it with the .pkg. Afterwards you can also run `sudo pkgutil --forget io.github.kevinnb66699.DeskMotion.pkg` in Terminal (it asks for an administrator password) to remove the installer's receipt (its record of the installation); it's fine to skip this.
5. To delete the imported wallpapers as well, press ⇧⌘G in Finder, then go to and delete each of these:
   - `~/Library/Application Support/DeskMotion` (the library, playlists, wallpaper properties, the copy of Wallpaper Engine's assets, the still pictures used for syncing the system wallpaper and for the lock screen, and a backup of the system wallpaper settings)
   - `~/Library/Containers/io.github.kevinnb66699.DeskMotion.WallpaperExtension` (the folder of the lock screen's system wallpaper extension; there only once the extension has run, on macOS 26)
   - `~/Library/Preferences/io.github.kevinnb66699.DeskMotion.plist` (preferences such as window positions and the interface language)
   - the folders named `io.github.kevinnb66699.DeskMotion` in `~/Library/Caches/` and `~/Library/WebKit/` (caches of web wallpapers)
   - `~/Library/Logs/DeskMotion` (logs of automatic updates)

## FAQ

**"The application can't be opened", and there's no "Open Anyway"**
Most likely the installer was forwarded through a chat app such as Feishu (Lark): files saved by such apps carry a stricter quarantine flag, and macOS refuses to run them outright without offering "Open Anyway". Either:
- download the installer again with a browser (Safari, Chrome and so on) from the download page https://deskmotion.jiling.chat/ (alternative: https://github.com/Kevinnb66699/DeskMotion/releases/latest ) and install it as described in "Installing and opening for the first time"; or
- drag DeskMotion into Applications first, then open Terminal, paste the line below and press Return; after that DeskMotion opens with a double-click:
  ```
  xattr -dr com.apple.quarantine /Applications/DeskMotion.app
  ```

**The wallpaper has stopped moving**
Open the DeskMotion menu in the menu bar and look for "Paused:". Most likely an automatic pause has kicked in (on battery, Low Power Mode, Mac too hot, a full-screen app, a window filling the screen and so on). Turn that automatic pause off in "Settings…", or click "Resume Playback".

**The desktop is black after closing and opening the lid**
When the Mac wakes from sleep (lid closed, display off), DeskMotion loads every display's wallpaper again (after you unlock, if a password is required): videos start from the beginning, web wallpapers reload, and the picture fades in; a wallpaper paused automatically (on battery, for example) stays paused and shows its first frame. A video that fails to play is retried a few times.
Version 1.3.0 and earlier don't do this, and after sleep the wallpaper sometimes stays black. You don't have to restart DeskMotion; first try switching to another wallpaper in the library and back, or, on battery, plugging in power (or turning off "When on battery power" in "Settings…"). If that doesn't help, quit DeskMotion and open it again.
If you use a cleaning, battery-saving or "freeze background apps" tool, it may suspend DeskMotion; add DeskMotion to that tool's exceptions.
If a newer version goes black too, before restarting DeskMotion open Terminal, paste the line below and press Return, and attach `deskmotion-log.txt` from your desktop to your report:
```
/usr/bin/log show --last 3h --predicate 'subsystem == "io.github.kevinnb66699.DeskMotion"' > ~/Desktop/deskmotion-log.txt
```

**There's no sound**
Only the main display plays sound by default. Check that display's "Mute" switch and "Volume" on the right side of the library, and whether "Mute All" is on in the menu bar. Image and GIF wallpapers have no sound.

**An import failed**
The task bar at the bottom of the library window says why, for example "Unsupported file type", "Couldn’t find the web page to show (index.html)" or "This Mac can’t decode AV1 video".

**A URL wallpaper is blank**
First make sure the address opens in a browser. If the network isn't up yet when your Mac starts, DeskMotion retries automatically.

**The wallpaper on the lock screen or in Mission Control doesn't match the desktop**
Make sure "Sync with system wallpaper" is on in "Settings…". macOS can only change the system wallpaper of the current Space; other Spaces are updated when you switch to them.

**The lock screen only shows a still picture, or is black**
- Check that you're on macOS 26 or later, and that "Play wallpapers on the lock screen" is on under "Settings…" → "Lock Screen" with "Active" shown below it. If it says "DeskMotion isn't the system wallpaper yet", click "Set Up"; if it says "Choose DeskMotion in System Settings", click "Open Wallpaper Settings" and follow the hint.
- Locking from a full-screen app shows another wallpaper, or a desktop Space you created or a display you connected since then still shows your old one: quit DeskMotion and open it again, and it sets those up too as it starts; or turn lock screen playback off and on again.
- Only video wallpapers play on the lock screen; while paused, on battery, in Low Power Mode or when the Mac is too hot (with those automatic pauses on) it shows the still picture too.
- Black: most likely DeskMotion was chosen in System Settings before the switch was turned on, or DeskMotion has no wallpaper on that display. Turn the switch on, set a wallpaper and wait a few seconds.
- If it still doesn't work, look at `~/Library/Application Support/DeskMotion/WallpaperExtension/state.json`: `lastError` says what the extension last ran into (please include it when you report the problem), and `safeMode` set to `true` means the extension quit unexpectedly 3 times within 10 minutes, so it shows only still pictures for now and recovers by itself within 10 minutes (the extension restarting when you turn "Play wallpapers on the lock screen" on or off, log out or update DeskMotion doesn't count).

**DeskMotion isn't in System Settings → Wallpaper**
It needs macOS 26 or later. Put DeskMotion in the Applications folder and open it once, then reopen System Settings; if it's still missing, log out and back in.

**After turning off syncing, the system wallpaper isn't dynamic anymore**
On macOS versions other than 26, the original dynamic aerial wallpaper can only be restored as a still image (a system limitation); choose it again in System Settings → Wallpaper. On macOS 26 the aerial itself comes back; if the system wallpaper service didn't accept it at the time, the current Space comes back as a still, and the other Spaces are tried again later (the next time DeskMotion opens with syncing off, or the next time you turn syncing off or quit; after two failures in a row DeskMotion stops retrying on its own, and "Replace" in "Settings…" does it instead). To get the motion back on the current Space, choose it again in System Settings → Wallpaper.

**An audio-reactive wallpaper doesn't react**
Make sure it's a web wallpaper imported to your Mac (online URL wallpapers can't react to audio), or a scene tagged "Live" with effects or particles that react to sound, that you're on macOS 14.2 or later, that your Mac is playing sound, and that you've allowed the system audio recording permission. After updating DeskMotion you need to allow it once more.

**Buttons in a web wallpaper can't be clicked**
That's expected: web wallpapers only follow the mouse as it moves and don't receive clicks; clicking the desktop and the desktop icons works as usual.

**How do I make scene wallpapers move?**
Scene wallpapers (the Workshop items with a scene.pkg) aren't videos: they're rendered in real time. Their layers are drawn with the scene's own shaders, and many also use shared assets from Wallpaper Engine's installation folder (the `assets` folder), which DeskMotion can't ship. So to play them live, copy `steamapps\common\wallpaper_engine\assets` from a Windows PC with Wallpaper Engine and choose it in "Settings…" → "Wallpaper Engine Scenes"; see "Scenes played live (preview)" above for the steps. Without the assets, a scene shows the still picture made when it was imported (its card shows "Static").
If a scene tagged "Live" hardly moves or is missing its main content: live playback is still a preview, and DeskMotion's engine doesn't support text (clocks included), the scene's own videos and sounds, scripts, and puppet bone animation yet, so such scenes still differ quite a bit from Wallpaper Engine. For exactly the same look, there's a workaround (also the export method Wallpaper Engine itself recommends): on a Windows PC, play the wallpaper in Wallpaper Engine's windowed mode, record it to mp4 with screen recording software such as OBS, and import the video into DeskMotion. Once recorded, it's an ordinary video wallpaper: it no longer follows the mouse or the sound, and its properties can't be adjusted.
If a scene still shows "Static" although the assets are ready: make sure "Play scene wallpapers live (preview)" is on; a scene that is just one video plays as a video; a scene that failed to load, had nothing that could be drawn (only text, say), was too slow for the graphics card or didn't fit in its memory goes back to its still and is tried again after the Mac wakes from sleep, the next time DeskMotion opens, or after you choose the assets again.

**An update failed, or "Update Now" turned into "Go to Download Page"**
The "DeskMotion Update" window says why, and the old version isn't affected. Click "Try Again", or click "Go to Download Page" to download the installer and install it again. If the button says "Go to Download Page" from the start, DeskMotion is most likely not in the Applications folder (for example, it was opened straight from the installer); drag it into Applications first and open it from there.

**A playlist doesn't switch**
Check the "Next switch" time in the Displays panel. With "Let videos play to the end before switching" on, the video that's playing has to finish first; a playlist with only one usable wallpaper doesn't switch.

**The wallpaper is still there after pressing ⌘H**
That's expected: hiding DeskMotion only hides the library window, not the desktop wallpaper.

**Battery use**
Video wallpapers use hardware decoding and pause automatically on battery by default. How much power a web wallpaper uses depends on the page itself; complex 3D pages use more.

## Open-source licenses

DeskMotion's built-in video converter is [FFmpeg](https://ffmpeg.org) 9.0.2, released under the LGPL 2.1; the full license is in `DeskMotion.app/Contents/Resources/LICENSE-ffmpeg.txt`.

DeskMotion decodes animated WebP with [libwebp](https://chromium.googlesource.com/webm/libwebp) 1.6.0, released under a BSD license (with a patent grant); the full license is in `DeskMotion.app/Contents/Resources/LICENSE-libwebp.txt`.

The lock screen's system wallpaper extension uses macOS's undocumented interfaces the way [Phosphene](https://github.com/kageroumado/phosphene) (© 2026 kageroumado), [Driftwood](https://github.com/iamEvanYT/driftwood) (© 2026 iamEvan) and [Aerial](https://github.com/AerialScreensaver/Aerial) (© 2015–present Guillaume Louel and contributors) do, and parts of its code are adapted from them; all three are released under the MIT license, and their notices are in `DeskMotion.app/Contents/Resources/THIRD_PARTY_NOTICES.txt`.

DeskMotion reads Wallpaper Engine scene files (scene.pkg and .tex textures) following the file format as read by [RePKG](https://github.com/notscuffed/repkg) (MIT license, by notscuffed); none of its code is included. The format of puppet layer meshes (.mdl) is our own reading of the files.

## Download

Download the latest `DeskMotion-<version>.dmg` (or the installer package `DeskMotion-<version>.pkg`; see "Installing and opening for the first time" above) from the download page [deskmotion.jiling.chat](https://deskmotion.jiling.chat/); if the page doesn't open, it's also on GitHub under [Releases](https://github.com/Kevinnb66699/DeskMotion/releases/latest).

## Feedback

If you run into a problem or have a suggestion, please open an [issue](https://github.com/Kevinnb66699/DeskMotion/issues), ideally with your macOS version, your Mac model and the format of the wallpaper involved.

## About this repository

This repository is only for publishing the installers and collecting feedback. DeskMotion is free to use; its source code isn't public for now.

Every release and the download page come with the matching FFmpeg 9.0.2 source archive (`ffmpeg-9.0.2.tar.xz`, unmodified) and build script (`build-ffmpeg.sh`, with every build option), as the LGPL 2.1 requires. DeskMotion runs FFmpeg as a separate program and doesn't link its libraries.
