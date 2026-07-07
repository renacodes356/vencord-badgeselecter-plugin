# BadgeSelector

A [Vencord](https://vencord.dev/) plugin that lets you add, remove, or hide profile badges on any Discord user — **visual only**, client-side, doesn't touch anyone's actual account.

## Credits

Originally created by:

- **.q1**
- **Jelly**
- **Sami**

This version includes stability fixes built on top of their original plugin.

## What it does

- Add any real Discord badge (Nitro badges, HypeSquad, Bug Hunter, Boost tiers, etc.) to a user's profile, as seen only on your own client.
- Hide a badge someone actually has.
- Restore/reset everything back to how it really is.
- Works on your own profile and anyone else's.

This is purely cosmetic on your end, it does not grant real badges, does not modify anyone's actual Discord account, and other people will **not** see the changes unless they also install and configure this plugin themselves.

## Installation

1. Make sure you have [Vencord](https://github.com/Vendicated/Vencord) installed and set up for development (i.e. you can build from source). This plugin is not part of the official Vencord plugin list, so it needs to be added as a user plugin.
2. Locate your Vencord source folder, then go to:
   ```
   src/userplugins/
   ```
   (create the `userplugins` folder if it doesn't exist yet)
3. Inside `userplugins`, create a new folder, e.g.:
   ```
   src/userplugins/badgeSelector/
   ```
4. Place `badgeSelector.tsx` inside that folder.
5. Rebuild Vencord:
   ```
   pnpm build
   ```
  
6. Inject the new build:
   ```
   pnpm inject
   ```
7. Restart Discord
8. Open Discord settings → **Vencord → Plugins**, find **BadgeSelector**, and enable it.

## How to use it

1. **Right-click any user** — their name or avatar in a server member list, a message they sent, or in a DM. (Right-clicking your own name works the same way, in the same spots.)
2. In the context menu, click **Manage Badges**.
3. You'll see a checklist of every supported badge. Click any of them to toggle it on/off:
   - Checking a badge the user doesn't actually have → adds it (visually, for you).
   - Unchecking a badge they DO actually have → hides it (visually, for you).
4. At the bottom of that submenu:
   - **Give All Badges** — adds every supported badge to that user at once.
   - **Remove All Badges** — hides all of a user's real badges and clears any you've added.
   - **Reset to Original** — clears all your customizations for that user, back to their real, unmodified badge list.

Changes apply immediately — no reload needed.

## Notes & limitations

- This only changes what **you** see. It is not a way to fake badges to other people.
- Badge icons are pulled from Discord's own CDN (`cdn.discordapp.com/badge-icons/`), so only badges Discord actually has art for will display properly.
- Your customizations are saved locally (via Vencord's DataStore) and persist across restarts.

## Disclaimer

This plugin modifies client-side rendering only. Use of client mods like Vencord may be against Discord's Terms of Service — use at your own risk.
