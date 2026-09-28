# Ashen Builds

An all-class gear and talent planner for **Turtle WoW** (1.12 client), by The Ashen Banner & Claude AI.

Plan a character with any class, race and level: equip items from a database of every equippable
Turtle WoW item, add enchants, spend talents, and see your character-sheet totals. Warriors can also
simulate their DPS against raid bosses.

## Download

Get the latest **AshenBuilds-x.y.z.zip** from the [Releases page](../../releases/latest).

## Install

1. Close World of Warcraft.
2. Open the zip. It contains one folder, `AshenBuilds`.
3. Copy that folder into your game's `Interface\AddOns\` folder, so you end up with
   `...\Interface\AddOns\AshenBuilds\AshenBuilds.toc`.
4. Start the game. On the character screen, click **AddOns** and make sure Ashen Builds is ticked.
5. In game, type `/ab` or click the ember icon on the minimap.

**Updating:** close the game, delete the old `AshenBuilds` folder, and copy in the new one. Your
saved builds are kept (they live in the `WTF` folder, not the addon folder).

## Features

- **Planner** – every equippable item (searchable by name, NPC or zone, with source details),
  enchants including Turtle's custom ones, set bonuses, and accurate character-sheet totals.
- **3D model preview** of the gear on your character.
- **Talents** – all 27 Turtle WoW talent trees.
- **Saved builds** – save, rename and share builds as short codes.
- **Community builds** – publish a build for everyone on the realm running Ashen Builds, browse and
  upvote other players' builds.
- **Warrior DPS simulator** – click **SIM DPS** under the trinkets. Choose the boss, buffs, debuffs and
  rotation with the gear button next to it; hover the result for the full breakdown.

## Commands

| Command | Does |
|---|---|
| `/ab` | Open or close the planner |
| `/ab importgear` | Load the gear you are wearing |
| `/ab sim` | Simulate the current build (Warrior) |
| `/ab minimap` | Hide or show the minimap button |
| `/ab sync off` / `on` | Share community builds over guild and party only / also the realm channel |
| `/ab unhide <player>` | Show community builds from a player you hid |

## What the addon shares

To sync community builds, Ashen Builds joins a hidden chat channel called `AshenBuilds` and also uses
guild, party and raid addon messages. When you publish a build, your character name is sent with it,
together with the build's name, gear, enchants and talents; your upvotes carry your character name
too. Nothing else about you is sent. `/ab sync off` stops using the channel.

## Problems or ideas

Tell us in game (The Ashen Banner) or open an issue on this repository.
