
# Fake Mute & Deafen (Vencord Plugin)

A plugin for [Vencord](https://github.com/Vencord/Vencord) that lets you **pretend** to mute or deafen in Discord.
When enabled, others will see you as muted/deafened while you can still hear and speak.

⚠️ This is a **fake client-side effect**. Do not rely on it for privacy/security.

---

## Features

* Adds **Fake Mute** and **Fake Deafen** toggles to the right-click context menu on the Mute/Deafen buttons.
* Bright yellow button highlighting while fake mode is active.
* Suppresses UI sound effects during silent toggles.
* Hooks WebSocket events to swallow unwanted state updates.
* Auto-cleans fake states when changing voice channels.
* Toast notifications to confirm toggle actions.

---

## Installation

### Prerequisites

Before bypassing into custom plugins, ensure:

* You have a working **Vencord development build**, including installing from source with `git`, `Node.js`, and `pnpm` installed.([Vencord Docs][1], [GitHub][2])
* You’ve cloned the Vencord repository, installed dependencies via `pnpm install --frozen-lockfile`, then built (`pnpm build`) and injected (`pnpm inject`) it.([Vencord Docs][1])

### Adding Custom (“User”) Plugins

1. **Create the `userplugins` directory**:
   Inside your Vencord project folder, navigate to `src/` and create a new folder named `userplugins`.([Vencord Docs][3])

2. **Add your plugin**:
   Copy your plugin—in this case, the `Fake Mute & Deafen` plugin—into `src/userplugins/`. It can be either:

   * A single file:

     ```
     src/userplugins/FakeMuteDeafen.ts
     ```
   * Or a folder with an `index.ts` or `index.tsx` entry:

     ```
     src/userplugins/fakeMuteDeafen/index.ts
     ```

([Vencord Docs][3], [Vencord Docs][4])

3. **Rebuild Vencord**:
   After placing the plugin file or folder, run:

   ```
   pnpm build
   ```

   Restart Discord afterward—your plugin should now appear under the Vencord Plugins list.([Vencord Docs][3])

---

## Usage

* Open Discord with Vencord loaded.
* Navigate to **User Settings → Vencord → Plugins**.
* Find **Fake Mute & Deafen** in the list and turn the toggle **on**.
* Right-click the **Mute** or **Deafen** button in the Discord UI and select **Fake Mute** or **Fake Deafen**.
* The buttons glow yellow when fake mode is active.
* Changing voice channels or real state changes will automatically clear fake status.

---

## Auto-Cleanup

* Moving between voice channels or performing a real undeafen will clear or adjust fake mode to avoid inconsistent states.

---

## Disclaimer

This plugin is strictly for **educational and entertainment purposes** only.
It does **not** provide real privacy or security. Use responsibly.

---

## Author

* **gastrophobic** (Discord: `1225242988716757052`)

---

### Summary of Installation Steps (Table)

| Step | Action                                                             |
| ---- | ------------------------------------------------------------------ |
| 1    | Ensure Vencord is installed from source and working (build/inject) |
| 2    | Create `src/userplugins` directory in the Vencord repo             |
| 3    | Add your plugin file or folder inside `userplugins`                |
| 4    | Run `pnpm build`, then restart Discord                             |
| 5    | Enable plugin from Vencord settings in Discord                     |

---

Let me know if you'd like further tweaks—maybe clearer developer instructions, code templates, or even a visual guide!

[1]: https://docs.vencord.dev/installing/?utm_source=chatgpt.com "Installing Vencord | Vencord Docs"
[2]: https://github.com/chunkbanned/VCUserPluginsInstaller?utm_source=chatgpt.com "This script will help people install custom plugins to Vencord."
[3]: https://docs.vencord.dev/installing/custom-plugins/?utm_source=chatgpt.com "Installing custom plugins - Vencord Docs"
[4]: https://docs.vencord.dev/intro/?utm_source=chatgpt.com "Introduction - Vencord Docs"
