# KMctrl

**KMctrl** lets one Mac control another Mac's **keyboard and mouse over the local network** —
no cloud, no accounts. Built for bridging a locked-down / MDM work Mac to a personal one:
**window mode needs no permissions**, so it works without admin rights.

Source code: [github.com/jbull79/kmctrl](https://github.com/jbull79/kmctrl). Builds are also published there under [Releases](https://github.com/jbull79/kmctrl/releases); this repo hosts the latest zip.

## Download

### ▶︎ [Download KMctrl 0.8.14 (.zip)](https://github.com/jbull79/kmctrl-releases/raw/main/KMctrl-0.8.14.zip)

Requires macOS 13+, Apple Silicon. Install on **both** Macs.

## Install

1. Unzip and move **KMctrl.app** to `/Applications`.
2. First launch (unsigned beta) — a downloaded copy is quarantined and Gatekeeper blocks it.
   **The right-click → Open trick no longer works on macOS 15+.** Clear the flag once:

   ```sh
   xattr -dr com.apple.quarantine /Applications/KMctrl.app
   ```

   …or **System Settings → Privacy & Security → Open Anyway**. If a Keychain prompt appears,
   click **Always Allow**.

## Use

1. On the Mac you want to **be controlled**: turn on **Allow this Mac to be controlled**.
2. On the **controlling** Mac: pick the other Mac under *Control a device* → **Control** →
   **Start controlling**. The first time, the other Mac asks you to allow it (and remembers).
   Drive it with your keyboard/mouse; press **⌃⌥⌘** to release.

- **Window mode** (default) needs no permissions — works on a locked-down MDM Mac.
- **Edge mode** (bump a screen edge to hand off) needs Accessibility + Input Monitoring.

Runs from the Dock, the menu bar, or both (Settings → Show KMctrl in).

## New in 0.8

- **Clipboard sync** — text and images copied on either Mac appear on the other during a session.
- **Layout-independent typing**, **media keys** (volume, brightness, playback) and a **mouse speed** slider.
- **⌃⌥⌘K** starts controlling again from any app (no permissions needed).
- **Wake screen** for the remote Mac, a **daily update check**, and a fix so a Magic Mouse swipe no longer drops control.
