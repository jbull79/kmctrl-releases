# KMctrl — Releases

**KMctrl** lets one Mac control another Mac's **keyboard and mouse over the local network** —
no cloud, no accounts. Built for bridging a locked-down / MDM work Mac to a personal one:
**window mode needs no permissions**, so it works without admin rights.

The source repo is private; notarized/signed builds and notes live here.

## Install (on both Macs)

1. Download `KMctrl-x.y.z.zip` from [**Releases**](../../releases/latest) and unzip.
2. Move **KMctrl.app** to `/Applications`.
3. First launch (unsigned beta) — a downloaded copy is quarantined and Gatekeeper blocks it.
   **The right-click → Open trick no longer works on macOS 15+.** Clear the flag once:

   ```sh
   xattr -dr com.apple.quarantine /Applications/KMctrl.app
   ```

   …or **System Settings → Privacy & Security → Open Anyway**. If a Keychain prompt appears,
   click **Always Allow**.

Requires macOS 13+.

## Use

1. On the Mac you want to **be controlled**: turn on **Allow this Mac to be controlled**.
2. On the **controlling** Mac: pick the other Mac under *Control a device* → **Control** →
   **Start controlling**. The first time, the other Mac asks you to allow it (and remembers).
   Drive it with your keyboard/mouse; press **⌃⌥⌘** to release.

- **Window mode** (default) needs no permissions — works on a locked-down MDM Mac.
- **Edge mode** (bump a screen edge to hand off) needs Accessibility + Input Monitoring.

Runs from the Dock, the menu bar, or both (Settings → Show KMctrl in).
