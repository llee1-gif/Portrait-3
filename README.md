# Living Portrait

When the iPad's front camera detects motion, the portrait wakes up. She blinks, looks toward the person, and speaks while her mouth moves.

Files:
- `index.html`: the whole app
- `queen.jpg`: the portrait image

## 1. Host it over HTTPS (required)
Safari only allows the camera on **https://** pages. It will not work if you open the file directly from Files, AirDrop, or a local network address such as `http://192.168.x.x`.

- **Netlify Drop** (easiest): drag the `portrait` folder onto https://app.netlify.com/drop and you get an https link.
- **GitHub Pages**: push both files to a repo, then turn on Settings → Pages.

To test on a Mac without hosting, use Chrome or Safari at `http://localhost:<port>`. Localhost counts as secure.

## 2. iPad setup
1. Open the https link in Safari. Tap Share → **Add to Home Screen**.
2. Launch it from the home screen icon, tap **Start**, then tap **Allow** for the camera.
3. If the camera was denied, go to Settings → Apps → Safari → Camera → **Allow**.
4. Go to Settings → Display & Brightness and set **Auto-Lock to Never**.
5. Go to Settings → Accessibility → **Guided Access** and turn it on. Then triple-click the side button inside the app to lock it.
6. Turn off Silent mode, turn up the volume, and keep the iPad plugged in.

## 3. Tuning
**Tap the top-left corner 5 times** to open Settings.

- **Sensitivity**: turn on **Show debug** and walk past the iPad. When the purple bar crosses the yellow line, she wakes. When it crosses the orange line, she says a long line.
- **Gaze direction**: if her eyes look away from people, turn on **Flip gaze direction**.
- **Recordings**: tap **🎙 Record** or **📁 File** on a line to use a real voice instead of text-to-speech. Recordings are stored only on this iPad.

## Sequence
1. Still portrait, slightly dimmed.
2. Motion is detected.
3. Chime, purple aura, and a blink.
4. She speaks a line.
5. She keeps watching for a few seconds.
6. She goes still again.
7. Motion is ignored during the cooldown.
