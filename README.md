
````
# Fake Mute & Deafen (Vencord Plugin)

A plugin for [Vencord](https://github.com/Vencord/Vencord) that lets you **pretend** to mute or deafen in Discord.  
When enabled, others will see you as muted/deafened while you can still hear and speak.

⚠️ This is a **fake client-side effect**. Do not rely on it for privacy/security.  

---

## ✨ Features
- Adds **Fake Mute** and **Fake Deafen** toggles to the right-click context menu on the Mute/Deafen buttons.
- Bright yellow button highlighting while fake mode is active.
- Suppresses UI sound effects during silent toggles.
- Hooks WebSocket events to swallow unwanted state updates.
- Auto-cleans fake states when changing voice channels.
- Toast notifications to confirm toggle actions.

---

## 📥 Installation (Custom Vencord Userplugin)

1. **Clone Vencord** (if not already):
   ```bash
   git clone https://github.com/Vendicated/Vencord
   cd Vencord
   pnpm install --frozen-lockfile
   pnpm build
````

2. **Create the `userplugins` folder** if it doesn’t exist:

   ```
   Vencord/src/userplugins/
   ```

3. **Add this plugin** inside the `userplugins` folder:

   * As a single file:

     ```
     Vencord/src/userplugins/FakeMuteDeafen.ts
     ```
   * Or in its own folder with `index.ts`:

     ```
     Vencord/src/userplugins/fakeMuteDeafen/index.ts
     ```

   ✅ Correct

   ```
   src/userplugins/FakeMuteDeafen.ts
   src/userplugins/fakeMuteDeafen/index.ts
   ```

   ❌ Incorrect

   ```
   src/userplugins/somefolder/FakeMuteDeafen.ts
   src/userplugins/nested/folder/FakeMuteDeafen/index.ts
   ```

4. **Rebuild Vencord**:

   ```bash
   pnpm build
   ```

5. **Inject Vencord**:

   ```bash
   pnpm inject
   ```

6. **Restart Discord**.
   You’ll now find **Fake Mute & Deafen** in the Vencord Plugins tab. Enable it and you’re ready to go.

---

## 🎮 Usage

* Right-click the **Mute** or **Deafen** button in the Discord UI.
* Select **Fake Mute** or **Fake Deafen** from the menu.
* When active:

  * Others will see you muted/deafened.
  * You will still be able to hear/speak.
  * Buttons glow **yellow** to indicate fake status.

---

## 🧹 Auto-Cleanup

* Changing voice channels automatically clears fake states.
* Real undeafen will bounce fake mute back to keep consistency.

---

## 🛑 Disclaimer

This plugin is for **educational and entertainment purposes only**.
Use responsibly, don’t abuse it, and remember: this doesn’t give you real privacy.

---

## 👤 Author

* **gastrophobic** (Discord: `1225242988716757052`)

```

Do you also want me to give you the **raw `.gitignore`** and **raw LICENSE** files so the whole repo is ready to push?
```
