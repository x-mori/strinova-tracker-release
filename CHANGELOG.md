# Changelog

## 0.2.0: Discord status and live match tracking

### New

- **Discord Rich Presence:** works out of the box, with no setup. Your status shows *Playing Strinova* with the Strinova Tracker logo and a **Get Strinova Tracker** button for your friends.
  - **Details:** queue, mode and map in English, e.g. *Ranked: Demolition · Ocarnus*.
  - **State:** *Launching...*, *In Lobby*, *In Queue*, *Selecting Character*, *Locked In*, *Loading*, then the round and score in a match (*Round 6 · 3–2*) or *Watching Replay*, plus your party size *(1 of 5)*.
  - **Badge:** your character's icon during a match or replay (hover for K/D/A and damage score), or your rank otherwise. Hover the map logo to see the map.
  - **Timer:** time in the lobby, in queue (taken from the game's queue timer) or in the match.
  - Hover the game status in the tracker's top bar to preview the card.
- **Live match tracking (experimental, off by default):** turn it on in **Settings → Tracking**. While the game is in front, the tracker takes a screenshot of the game window about every 1.5 seconds, the same capture PrintScreen makes, and reads the lobby, character select, versus, loading, match, results and replay screens. It works in every client language.
  - Your character comes from character select or the versus screen. After that, the tracker learns your scoreboard icon, so it still knows a character swap at half-time.
  - The map comes from character select or the loading screen. If you missed both, it uses the zone names above the minimap.
  - The game has to run in borderless or windowed mode at a 16:9 resolution. Exclusive full screen can't be captured.
- **Close to tray:** closing the window keeps the tracker and your Discord status running in the system tray. Quit from the tray icon or **Settings → About**, or turn this off in **Settings → General**. Starting with Windows now starts in the tray.
- **Encounters avatars:** each player on the Encounters tab shows their latest in-game avatar.

### Fixed

- **Portrait alignment:** Eika's portrait now lines up with the other characters' heads, where before her flame horns pushed it down. Your existing character crops are remade the first time you start 0.2.0.
- **Performance tab:** overtime rounds are counted apart from regulation in the per-character portraits, since characters swap every overtime round.
- **Discord map:** the map stays on your status through half-time.

## 0.1.0: first public release

The first public build of Strinova Tracker.

- **Profile:** current and peak Ranked and Challenge ranks on whole-ladder strips, career stats, accuracy, top characters, maps and weapons, and the people you play with and against.
- **Rank progress:** Challenge star progress with points to the next division. Ranked shows your exact place on the division ladder.
- **Match history:** grouped by day, with filters for mode, map, character and achievements.
- **Match page:** scoreboard, performance, economy, rounds and duels, with match achievements.
- **Round theater:** 2D minimap playback with positions, vitals, weapons, utility areas, bomb state and the kill feed.
- **Maps and characters:** minimaps with callouts, kill and death heatmaps, and wiki data.
- **NOVA Impact (experimental, off by default):** per-round impact scores with animated tier emblems.
- **Replay archive:** keeps every replay before the game deletes it, and downloads your listed replays.
