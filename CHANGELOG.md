# Changelog

## 0.2.2: player details and a new look

### New

- **Player details:** click anyone on the Encounters tab to open a popup with a spider chart of seven traits.
  - **Traits:** Synergy (or Rivalry for opponents), Firepower, Survival, Entry, Consistency, Assistance and Cooperation. Each is a percentile against the other players in your selection, so 50 is the middle. Hover a trait to see the number behind it.
  - **Stats:** their K/D, KDA, ADR, average score, KAST, headshot rate and more, your record with or against them, their most played characters and your recent shared matches.
- **Weapon links:** clicking a signature weapon on the Weapons tab opens its character's page.

### Changed

- **Encounters:** players are now cards with their full banner fading out at the bottom, like the character pages.
- **Mode names:** Challenge matches now read *Demolition*, since Challenge has several modes. Ranked matches read *Demolition* with a small *Ranked* tag beside it.
- **Top characters:** the top 3 portraits are bigger and zoomed in, with a glowing halo on hover.
- **Navigation:** the top bar has animated icons, with Settings moved to a gear on the right. The profile tabs now spread across the page with their own icons.

### Fixed

- **Encounters filters:** the mode and season buttons did nothing on this tab. They now filter the players shown.
- **Discord map names:** one misread zone name could hide the map for a whole match or show the wrong one, which affected maps like Lebrun City. Zones now take a vote, and a wrong guess can correct itself during the match.
- **Discord characters:** a character whose name couldn't be read before the match can now be learned from that match's replay, so it shows from then on. A new skin no longer clears your character at the start of a match.
- **Discord updates:** a one-character misread map name could make Discord reject the whole status update. Character icons are also scaled down before Discord loads them, since some were over 1 MB.
- **Challenge points:** *latest change* showed 0 after a Ranked match, and now shows your last real change. Replays save your score from when a match starts, so a Challenge match's result only appears with your next replay. The Challenge card now says when your last match hasn't been counted yet.

## 0.2.1: map names on Discord and round viewer icons

### Fixed

- **Discord map names:** live match tracking now reads the map on more loading, character select and results screens. Area 88 never showed on your status before, and other maps were missed now and then. Short titles like Area 88's are matched even when they're partly misread.
- **Dormitory status:** going back to the dormitory after a match no longer shows *Loading* with the map set to *DORMITORY*.
- **Round viewer icons:** skill and grenade markers showed only a letter if you opened a match before the game data finished downloading. They now get their icons as soon as the download finishes, with no restart.
- **Game data download:** images that fail to download (network errors, rate limits) are now listed in the finish message and fetched again the next time you start the tracker. Before, they were skipped silently and their icons stayed blank.

### Changed

- **First launch:** the tracker downloads character, map and item data from the Strinova Wiki by itself the first time you open it. You no longer have to start it by hand. Icons, map art and Discord map names all need this data.

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
