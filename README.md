# 📺 YouTube Ad-Free Desktop (FMHY Edition)

A high-performance, ad-free desktop YouTube client powered by the privacy and adblocking techniques recommended on [FMHY (FreeMediaHeckYeah)](https://fmhy.net/privacy).

---

## 🚀 Features

1. **Triple-Layer Adblocking:**
   - **Layer 1 (Ghostery / uBlock Engine):** Uses `@ghostery/adblocker-electron` to block network ads, trackers, and analytics with full prebuilt EasyList and filter rules.
   - **Layer 2 (Dedicated Host Interception):** Explicitly cancels requests to `doubleclick.net`, `googleads`, `adservice`, and internal YouTube ad break telemetry endpoints.
   - **Layer 3 (FadBlock Fallback):** If YouTube ever attempts server-side video ad stitching, the player immediately mutes, speeds up playback to 16x, jumps to the end in under 50ms, and clicks skip buttons automatically.

2. **Built-in SponsorBlock Integration:**
   - Automatically queries the public [SponsorBlock API](https://sponsor.ajay.app) for the current video.
   - Seamlessly skips sponsored segments, intros, outros, subscription reminders, and self-promos.
   - Shows a clean floating notification toast when a segment is skipped (`⏩ Skipped Sponsor [01:20 - 02:45]`).

3. **Anti-Adblock Popup & Backdrop Neutralizer:**
   - Neutralizes YouTube's `"Ad blockers violate YouTube's Terms of Service"` dialogs and automatically restores smooth video playback.

4. **Privacy & Google Login Compatible:**
   - Masks User-Agent as standard Google Chrome on Windows so Google Account login works without `"This browser or app may not be secure"` restrictions.

5. **Clean Aesthetic UI:**
   - Removes homepage banner ads, promotional mealbars, and merch shelves.
   - Dark mode background with sleek custom scrollbars.

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
| :--- | :--- |
| **`F11`** | Toggle Fullscreen |
| **`Ctrl + R`** | Reload Current Page |
| **`Alt + Left`** | Go Back in History |
| **`Alt + Right`** | Go Forward in History |
| **`Ctrl + H`** | YouTube Home |
| **`Ctrl + S`** | Subscriptions Feed |
| **`Ctrl + L`** | Library / History |
| **`Ctrl + Shift + I`** | Open Developer Tools |

---

## 🛠️ How to Run

Ensure Node.js is installed on your computer, then navigate to this folder and run:

```bash
# 1. Install dependencies (if not already installed)
npm install

# 2. Launch the desktop application
npm start
```

---

## 📦 Building Standalone Windows `.exe`

If you'd like to package this into a standalone executable:

```bash
npm install --save-dev electron-builder
npx electron-builder --win
```
The generated `.exe` file will be created in the `dist/` directory.
