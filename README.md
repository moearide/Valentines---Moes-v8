# 💘 Valentine Interactive Experience

A mobile-first, interactive Valentine webpage built with pure HTML, CSS, and JavaScript.

Designed for emotional UX, touch interaction, and a cinematic “Yes” moment.

---

## 🌐 Live Site

Host `index.html` using:
- GitHub Pages
- Netlify / Vercel (drag + drop or connect repo)
- Any static host (S3, Surge, Firebase Hosting, etc.)

Quick GitHub Pages:
1. Push the repo to GitHub.
2. In repository Settings → Pages, select branch `main` (or `gh-pages`) and root `/` (or `/docs`).
3. Wait a minute and open the provided URL.

---

## ✨ Core Experience

### 📱 Mobile-First
- Touch optimized
- Finger-tracking Yes button
- Tap-safe interactions
- Haptic vibration feedback (where supported)

### 💖 Interaction Flow
1. User tries to tap **No**
2. No button runs away
3. “Are you sure?” prompts appear
4. Yes button grows + follows finger
5. No eventually disappears

### 🎉 YES Celebration
When Yes is tapped:
- Background music plays (optional)
- Camera-flash animation
- Center confetti burst
- Massive floating hearts
- Animated reveal: **“Mya ❤️ Moe”**
- Final message appears
- Auto redirect to invite page

---

## 🎵 Music Setup

Add an audio file in the repo root (or same folder as `index.html`) and name it `music.mp3` (or update the `src` in the HTML).

Recommended:
- Files: `music.mp3` (fallback) — you can also include `music.ogg` and add a second `<source>` element for broader browser support.
- Duration: ~10–60s (short loop is fine)
- Keep file size small for mobile (use ~128–192 kbps MP3 or optimized OGG).
- Example file path: `./music.mp3`

Autoplay note: modern browsers only allow audio playback after a user gesture. This project plays audio in response to the "Yes" click, which satisfies autoplay policies on most browsers/devices.

---

## 🖼️ Social Preview / OG Image

Replace the placeholder OG image referenced in the HTML meta tag:

<meta property="og:image" content="https://raw.githubusercontent.com/<your-username>/<your-repo>/main/og-card.jpg" />

Steps:
1. Create an OG image (recommended: 1200×630px, JPG/PNG).
2. Add it to your repo (e.g. `og-card.jpg` in repository root or `assets/`).
3. Update the `og:image` meta tag in `index.html` to point to the raw GitHub URL:
   `https://raw.githubusercontent.com/<owner>/<repo>/main/og-card.jpg`
4. Give GitHub/GTM some minutes for caching; use Facebook/Twitter debugger to refresh preview.

---

## ⚙️ Customization

- DATE_URL: edit the top of the inline script in `index.html`:
  const DATE_URL = "https://example.com/date-invite";
  Replace with the invite/landing page you want to redirect to.

- Reveal Text: change the reveal text shown on success by editing:
  document.getElementById('revealText').textContent = "Mya ❤️ Moe";

- Colors & look: tweak CSS variables at top of `<style>`:
  :root { --bg1:#ffe6f2; --bg2:#fff6fb; --text:#1f1f1f; --pink:#ff4da6; }

- Motion / Accessibility: the enhanced version respects `prefers-reduced-motion`. To disable that behavior or tune animation intensities, edit JS and CSS where reduction is checked.

---

## ♿ Accessibility

- Buttons are keyboard-focusable and support Enter/Space activation.
- Messages use `role="status"` and `aria-live="polite"` so screen readers announce updates.
- Uses `prefers-reduced-motion` to reduce/confine animations and vibration when requested.
- If you need stricter accessibility (contrast, large text, screen-reader-only instructions), I can add:
  - visible focus outlines, larger hit targets, or an explicit “keyboard mode” instruction.

---

## 🧪 Testing

- Test on real devices (iPhone Safari, Android Chrome) to verify touch, haptics, and audio behavior.
- Use Chrome DevTools device toolbar for quick checks, but prefer an actual phone for vibration/audio autoplay behavior.

---

## 📁 Files

- `index.html` — core interactive page
- `music.mp3` — optional background music (add this)
- `og-card.jpg` — optional social preview image
- (Optional) `assets/` — place images or additional media here

---

## 🔐 Privacy / Safety

- No analytics or external trackers included.
- Audio and redirect behavior are local to the page; no data is sent externally unless you add APIs or tracking.
- If you include remote images (e.g. hotlinking OG image), those requests go to GitHub or your image host — be mindful of privacy for recipients.

---

## 🧾 License & Attribution

Use this project freely or adapt for personal use. If you’d like a license file added:
- MIT is a simple permissive option: create a `LICENSE` file with MIT text.
- If the design or assets are not yours (icons, music), ensure you have the rights to distribute them.

---

## Need help?

Tell me which of the following you'd like me to do next:
- Create or update the `index.html` file with your custom names and DATE_URL.
- Add `music.mp3` / `og-card.jpg` to the repo and prepare a commit (I can generate a patch).
- Convert the page to a React component (TSX) or a small npm build.
- Improve accessibility further (WCAG contrast, focus management, screen-reader copy).
- Provide a minimal GitHub Pages deployment guide (branch, DNS, custom domain).

Happy to make the exact edits and produce the commit/patch for you — tell me which files to output and any custom text (names, date link, music filename, og image).