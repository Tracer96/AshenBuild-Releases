# Ashen Builds

An all-class gear and talent planner for **Turtle WoW** (1.12 client), by The Ashen Banner & Claude AI

Plan a character with any class, race and level. Equip items from an embedded database of every
equippable Turtle WoW item, add enchants, spend talents, and see character-sheet totals calculated
the same way the game server does. Share builds with the whole realm and upvote the good ones.

## Download

Get the latest **AshenBuilds-x.y.z.zip** from the [Releases page](../../releases/latest).

## Install

1. Close World of Warcraft.
2. Open the zip. It contains one folder, `AshenBuilds`.
3. Copy that folder into your game's `Interface\AddOns\` folder, so you end up with
   `...\Interface\AddOns\AshenBuilds\AshenBuilds.toc`.
4. Start the game. On the character screen, click **AddOns** and make sure Ashen Builds is ticked.
5. In game, type `/ab` or click the ember icon on the minimap.

**Updating:** close the game, delete the old `AshenBuilds` folder, and copy in the new one. Your saved
builds are kept (they live in the `WTF` folder, not the addon folder).

## Features

### Planner
- Any class, race (including High Elf and Goblin) and level 1–60.
- 19 equipment slots with item tooltips that match the game, including set pieces and set bonuses.
- **Character totals** use the real vanilla base stats for every class, race and level, plus the
  vmangos formulas that BetterCharacterStats reads back from the client: health and mana from stamina
  and intellect, level-scaled crit and dodge per agility, class base crit and dodge, 5% base parry and
  block, defense and weapon-skill bonuses, armor from agility, racials, and measurable talent effects.
- Hover any total for a breakdown of where it comes from (base, gear, talents, racials).
- **Model preview:** switch the center panel to a 3D model wearing the planned gear. Drag to turn,
  scroll to zoom. It uses your own character's race, and only items your game client has cached.
- **Saved builds** save automatically once saved the first time. Rename, delete, or use Save As to make
  a copy. Export and import builds as short codes, including talents.

<img width="990" height="912" alt="image" src="https://github.com/user-attachments/assets/b4555ee9-e21c-49be-8368-4eada29d543b" />


### Item database
- Every equippable item, searchable by name, NPC or zone.
- Dropdown filters for slot, source (dungeon, raid, quest, world boss, crafted, reputation, PvP, world
  drop, vendor), quality and sort order, plus an item level range and up to four stat filters with
  minimum values.
- Filtering is near-instant: items are indexed in the background right after login.
- Right-click an item for its full sources: drops with chances, vendors, quests and crafting recipes.

<img width="1089" height="863" alt="image" src="https://github.com/user-attachments/assets/a561d749-fc8a-41a9-b3a1-3406a1da6dd8" />


### Enchants
- 263 enchants generated from the Turtle WoW database, including Turtle's custom enchants
  (Invocations, Sigils, spell penetration and vampirism bracers, and more).
- Rings and necklaces take jewelcrafting gemstones; belts take blacksmithing buckles.
- Two-hand, shield and item-level restrictions are enforced.
- Search, filter by stat (sorted by value), and lower ranks hidden unless you ask for them.

<img width="1208" height="881" alt="image" src="https://github.com/user-attachments/assets/8f8c6a89-65ca-47ea-a9e9-11292c322243" />

### Talents
- All 27 Turtle WoW talent trees with full descriptions, rank limits, row requirements and prerequisites.
- Talents that change the character sheet are applied to your totals.

<img width="1318" height="859" alt="image" src="https://github.com/user-attachments/assets/885861ac-17c0-4844-bb14-944953094f61" />

### DPS simulator (Warrior)
- Click **SIM DPS** under the trinket slots. A progress bar fills while the fights run (spread over
  frames, so the game never freezes). Then the average DPS and its 95% confidence range appear.
- Hover the result for the full breakdown: damage by ability, attack table, rage generated, spent and
  wasted, casts, procs and buff uptimes. Shift-click it for one fight's combat log.
- The gear button next to SIM DPS holds the settings for each class: fight length, target level and
  armor, position, number of targets, iterations, reaction time, rotation preset, Heroic Strike rage
  threshold, raid buffs, consumables and target debuffs.
- Every fight uses a fixed seed, so re-simming after a gear change compares the same fights and the
  tooltip shows the exact DPS change.
- Arms, Fury (dual-wield and two-hand) and Protection rotations, including Shield Slam, Revenge
  (with the boss hitting you), Slam and Overpower. Set bonuses and weapon procs are included.
- **Accuracy** is HIGH only when every equipped effect is simulated. Anything that isn't (for example
  on-use trinkets) is listed as *SIM EFFECT NOT IMPLEMENTED* and the result is marked PARTIAL.
- Mechanics come from Turtle's server data where possible and otherwise from the maintained Turtle
  WarriorSim. The combat log window lists the source and status of each one.

<img width="725" height="793" alt="image" src="https://github.com/user-attachments/assets/109cec74-3382-4245-98a1-eb3c46b7f7d0" />

### Community builds
- Publish a saved build and every player on the realm running Ashen Builds can see, load and upvote it.
- Builds and votes are shared player-to-player over a hidden realm channel plus guild, party and raid.
  They persist while the author or voters are offline, and new players catch up when they log in.
- Builds with offensive names are not listed. Right-click a build to hide every build from that
  player (`/ab unhide <player>` shows them again).

**What is shared.** To sync, the addon joins a hidden chat channel called `AshenBuilds` and also
uses guild, party and raid addon messages. When you publish a build, your character name is sent
with it, together with the build's name, gear, enchants and talents, and your upvotes carry your
character name too. Nothing is sent until you publish or vote, apart from short "what do you have?"
sync requests. `/ab sync off` stops using the channel (useful if you are at the ten-channel limit)
and syncs over guild and party only.

<img width="945" height="702" alt="image" src="https://github.com/user-attachments/assets/0703cb20-68dd-491e-b926-4f5fba998cf3" />

## Controls

| Action | How |
|---|---|
| Open or close the planner | `/ab`, or left-click the minimap button |
| Choose an item | Click a gear slot |
| Remove an item | Right-click a gear slot |
| Choose an enchant | Click the enchant line under the item name (or Shift-click the slot) |
| Add or remove a talent point | Left-click or right-click a talent |
| Load a saved or community build | Click it in Saved Builds or Community |
| Upvote a community build | Click the arrow in the Votes column |
| Move the minimap button | Drag it around the minimap |

The top bar has five tabs: Planner, Talents, Community, Saved Builds and Item Database. They all
open inside the main window. Clicking a gear slot opens the Item Database for that slot, and picking
an item (or loading a saved build) takes you back to the Planner.

## Slash commands

| Command | Does |
|---|---|
| `/ab` | Open or close the planner |
| `/ab community` | Open community builds |
| `/ab importgear` | Load the gear you are wearing into the planner |
| `/ab minimap` | Hide or show the minimap button |
| `/ab reset` | Start a fresh build |
| `/ab sim` | Simulate the current build |
| `/ab sim settings` | Open the simulator settings |
| `/ab sim log` | One fight's combat log from the last run |
| `/ab sync on` / `off` | Use the hidden realm channel for community builds, or guild and party only |
| `/ab unhide <player>` | Show community builds from a player you hid |

## Problems or ideas

Tell us in game (The Ashen Banner) or open an issue on this repository.
