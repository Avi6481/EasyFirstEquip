# Easy First Equip

Easy First Equip plays a weapon's first equip animation on later draws too, not just the first time.

Works on console.

## Settings

With [Easy Mod Settings](https://github.com/Avi6481/EasyModSettings) installed, these are under Pause Menu > Mod Settings > Easy First Equip. Without it, the mod uses the defaults.

- Enabled
- Chance, how often a draw plays it
- Cooldown, seconds before it can play again
- Same Weapon, every draw or new weapon only
- Weapon Types, turn each type on or off
- Clear Cooldown and Reset to Defaults

Settings are saved per save file.

## How it talks to Mod Settings

Everything is in `ModSettings/ModSettings.script`. It's the template from Easy Mod Settings with First Equip's options in it, so if you want your own mod in there, that's the file to look at.

The wrap on `FirstEquipSystem` can't find First Equip's own system from inside the wrap, so First Equip hands itself over through an `@addField` when the player loads in. That's in `Core/Hooks.script`.
