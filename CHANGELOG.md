# Changelog

## 0.2.3: round theater upgrades and in-app updates

### New

- **In-app updates:** the tracker checks for new versions when it starts and every few hours, and shows a reminder when one is out. Click **Update now** on the reminder, or go to **Settings → Updates**, to download it inside the app. The installer then opens by itself, with no trip to GitHub.
  - **Safe downloads:** each installer is checked against the SHA-256 checksum published on its release before it runs, and only comes from GitHub's own download servers.
  - **Settings → Updates:** shows your version, **Check now** and the release notes. Turn reminders off, or have new versions download in the background so installing takes one click. Installing always asks first.
- **Damage numbers** (round theater, off by default): numbers float up beside each player as it happens. Red is HP lost, blue is armor lost, green is healing and pink is a shield gained, like Celestia's temporary armor. Quick hits of one kind add up in one number that counts up.
- **Duels** (round theater, off by default): a line joins two enemies trading damage, in both players' colours, with each side's total for that fight in the middle. The side that just landed a hit flashes, and the line fades a few seconds after the shooting stops.
- **Player cards in the round theater:**
  - **Magazine size:** ammo reads like `30(30) / 220`, with the magazine size in small print. It goes up when a player buys a bigger magazine.
  - **Gun in hand:** a small arrow marks the gun the player is holding.
  - **Melee:** each player's melee weapon now has a pill next to their grenades and skills, up to five pills in all.
  - **In hand:** a grenade, skill or melee weapon lights up while the player holds it, aims it or has just used it, like aiming Celestia's Guardian Star.
  - **Elevation:** a new pill under the distance travelled shows how high a player is, from `0 lv` (the lowest floor anyone stood on that match) to `12 lv` (the highest point anyone reached).
  - **Knocked down:** a red pill counts down the 15 seconds a knocked player has before they're eliminated. It hides while a teammate revives them, since the game pauses the clock, and picks up where it left off if the revive fails.
  - **Name dot:** a glowing dot in the player's map colour sits before their name. Knocked and dead now show as icons.
- **View cones flash:** with view cones on, a player's cone flashes white whenever they fire or swing a melee weapon.
- **Audrey's Onslaught:** with her third awakening, Audrey's Champion never reloads, so her ammo shows as one number that counts down, like `450`.

### Changed

- **Player colours:** the gun arrow, the in-hand highlights, the movement icons and the name dot follow each player's map colour, so they match **Multi-colored** trajectories too.
- **Trajectory colours:** switching between Multi-colored and Team-colored in the theater now lasts for that session, without changing your saved setting or showing a notification.
- **Upgrades and loadout:** a player's upgrade counts and their grenades and skills now fit on one row, and the cooldown timer sits neatly under its skill icon.
- **Round result icons:** the elimination, defuse, time-expired and detonation icons share one badge design.
- **Hovering players:** hovering a player on the theater map now always shows their card. A skill that follows the player keeps its own tooltip on its small icon beside the player.
- **Kill feed weapons:** secondary weapons, melee weapons and grenades now point at the victim like primary weapons do.

### Fixed

- **Reload timers:** *Reloading* showed without its countdown after a game update. Every gun shows the time left again, and *Reloading* ends when the magazine is full instead of lasting until the next shot.
- **Missing reloads:** back-to-back reloads were read as one, so many mid-match reloads didn't show. Every magazine change now shows.
- **Shooting while reloading:** a player's shooting icon could stay lit while they reloaded.
- **Outdated round data:** opening a match while the tracker was still reading replays could keep showing older data until you restarted. The theater now refreshes when reading finishes.
- **Melee weapons:** only players who swung their melee weapon showed it. Every player's melee weapon now shows.
- **Distance travelled:** long distances were cut off in their pill.

### Note

- Your archived matches are read again after updating, so reload times, elevation and melee weapons fill in for older matches too. This takes a few minutes the first time you open 0.2.3.

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
- **Match page header:** the *Ranked* tag ran under the map name. The mode now sits above the map.
- **Rank progress animation:** the glow on the star and division panels cut off partway and restarted. It now crosses the panel in one smooth sweep. The *At peak* badge's shimmer had a similar jump.

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
