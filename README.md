# Hypixel 2020

# This will not receive updates or fixes, and is deprecated for a proper version you can view at https://discord.gg/6n4JvYsbFH Developed by quite a few notable figures in the community such as Auth, Billionaire, Shadowocto, Trol

A recreation of Hypixel **SkyWars** and **Bed Wars** as they were in summer 2020, all in one Spigot plugin.

- **Lightweight.** About 140 MB on disk after building, and about 1.6 GB of RAM and 1.2 CPU cores with around 80 bots online, you are able to host it locally.
- **20 maps from 2020** for SkyWars and Bed Wars are included. The real Hypixel lobby is not.
- **Made in about 1–2 hours with Claude.** The anticheat may not be fully accurate, so fix it yourself or somehow source the "accurate" one billionaire is making.

## Features

- **Bed Wars:** Solo, Doubles, 3v3v3v3 and 4v4v4v4. Includes the item shop, team upgrades and traps,
  generators, beds, bed bugs and dream defenders, fireballs/TNT/bridge eggs, `/shout`,
  using mid-2020 (v1.6) prices.
- **SkyWars:** Solo/Teams, Normal/Insane. Includes cages, kits, loot tables, refills, Doom/end phases and
  spectators.
- **Bots:** each bot is a perfectly emulated serverside player, bots are also checked by the anticheat. Bots have human-like aim and CPS,
  bridging styles, looting, chat, and 2020-style names and skins. A configurable share of bots can cheat.
- **Watchdog:** a packet-level anticheat modelled on NoCheatPlus's check set (moving, fight, block place/break,
  inventory, net). It uses Hypixel-2020 presentation: delayed bans, `[WATCHDOG ANNOUNCEMENT]`, "A player has been
  removed from your game.", `/report`.

## What you need

- **Java 17 or newer**, to build the plugin: [download](https://adoptium.net/temurin/releases/?version=21)
- **Java 8**, to run the server: [download](https://adoptium.net/temurin/releases/?version=8)

## How to run it

The easiest way: paste this repo's link into Claude and tell it to set it up for you. Or do it yourself:

1. **Download** this repo (green **Code** button → **Download ZIP**, then unzip it) or `git clone` it.
2. **Start the server:**
   - **Windows:** double-click `start-server.bat`.
   - **Mac / Linux:** run `bash start-server.sh` in the project folder.
3. **Accept the Minecraft EULA** when it asks (type `y`). This only happens the first time.
4. **Wait** until the window says `Done`. The first start takes a minute or two.
5. **Join** `localhost` in Minecraft 1.8.9. You're made admin automatically.

To stop the server, type `stop` in its window.

## Commands

Use the compass or the NPCs in the lobby to join a game. Settings are in `run/plugins/Hypixel2020/config.yml`.

| Command | What it does |
|---|---|
| `/play <mode>` | Join a game: `solo_normal`, `solo_insane`, `teams_normal`, `teams_insane`, `bedwars_eight_one`, `bedwars_eight_two`, `bedwars_four_three`, `bedwars_four_four` |
| `/lobby` | Back to the lobby |
| `/h2020 create <mode> [map]` | Start a game on a specific map |
| `/h2020 games` / `/h2020 watch <id>` | List games / spectate one |
| `/h2020 fillspeed <x>` | How fast bots fill games (1 = real 2020 queue times) |
| `/h2020 cheaters <percent>` | Share of bots that cheat; Watchdog catches them |
| `/h2020 rank <player> <rank> [color]` | Set a rank, e.g. `/h2020 rank YourName MVP_PLUS RED` |
| `/h2020 date today` | Show today's date on scoreboards instead of a 2020 one |
| `/bot spawn [name] [cheat]` / `/bot list` | Spawn a bot / see what every bot is doing |
| `/wd alerts` | Anticheat alerts on or off for you (off by default; everything is logged to `watchdog.log`) |
| `/report <player>` | The 2020 report menu |


## Troubleshooting

- **"Java 8 not found":** install Java 8 from the link above, or set `JAVA8_HOME` to its folder.
- **Build failed:** make sure Java 17+ is installed and is the `java` on your PATH (`java -version`).
- **Can't connect:** use Minecraft **1.8.9** and join `localhost` while the server window is open.
