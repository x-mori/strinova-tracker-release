# Changelog

## 0.3.2: a new look, richer map pages and Lilith

### New

- **Lilith:** the Crystalline joins the character list, marked as an **Outbreak character**. Her page has her skills, her Whip's damage, her health and armor by level, and her voice cast.
- **Map tools:** map pages get the theater's zoom, pan and rotate.
- **New map layers:** alongside kills and deaths, you can now show:
  - **Ability uses:** where you stood when you used your skills, ultimates included.
  - **Throwables:** where every kind landed, from bought grenades to each character's own tactical.
  - **Plants and defuses:** where you did them.
- **Map dot tooltips:** hover a dot to see the character, what happened, the kind of match (Demolition, Demolition Ranked, Team Deathmatch and so on), the date, the round and the time.
- **More on map pages:** a description of each map, your attack and defense records, and your fight ranges.
- **Weapon damage tables:** character pages show each weapon's damage at set ranges, beside its art.
- **Voice cast:** each actor has a flag for their language, a link to their page where one could be confirmed, and their name in Japanese or Chinese script.
- **Trades and Flanks** (theater): two new map layers.

### Changed

- **Profile banner:** redesigned as an operator file, with your stats on a string and your avatar fading into the banner.
- **Overview panel:** a win-loss tension line and its own set of icons.
- **Character list and pages:** reworked in the same style, with a shorter dossier, skills and awakenings in even rows, and skill values tagged with icons, units and a colour for each kind.
- **Portraits:** every character is framed to the same size with their head at the same height.
- **Map pages and Profile tabs:** map pages are reworked in the same style, and the Characters, Weapons and Maps tabs on your profile are restyled to match.
- **Settings:** reworked with a side menu and setting tiles.
- **Credits and loading screen:** both reworked. The loading screen has a turning logo and a string that shows real progress.
- **Taskbar:** clicking the app on the taskbar while it's open now minimizes it with the normal Windows animation.
- **Theater:**
  - HP and armor bars ease the way the damage numbers do.
  - The in-hand arrow only makes room on the held weapon, and slides between rows.
  - The map pill is darkened all the way to its edges.
  - The bomb popup stays up after the round ends.
  - The planted bomb flashes on the map with no circle behind it.
- **Rounds tab:** the kill feed scrolls.

### Fixed

- **Match list:** Team Arena and Team Deathmatch rows left an empty gap where NOVA Impact would be, which pushed the details onto extra lines. The map, details and score now use that space.
- **Weapons tab:** weapons with no hits no longer draw grey blocks.

### Note

- Character data and portraits refresh once the first time you open 0.3.2, which can take a few minutes. Your matches aren't read again.

## 0.3.1: Team Arena and Team Deathmatch get their own match pages

### New

- **Team Arena and Team Deathmatch pages:** these modes have no rounds or credits, so their match page now fits how they play. **Equipment** and **Replay** take the place of Economy and Rounds, and the columns, pages and panels that only make sense with rounds or a bomb are gone.
- **Equipment tab:** every player's final upgrades, then each change with its time: the build picked at spawn, swaps during the match, and changes made in the warmup.
- **Replay tab:** the whole match as one playback, with the final results, the full kill feed and the minimap. Open it in the theater for the full view:
  - **Live score:** the team scores tick up in the header as the replay plays.
  - **Live cards:** each player's kills, deaths, damage and upgrades update as the match goes on.
  - **Respawns:** death marks fade after 10 seconds and trails restart at each respawn, so the map stays readable for the whole match.
- **Teams A, B and C:** Team Deathmatch's three teams of five each get their own scoreboard section and score, with the second enemy team in its own colour. The match list, match header, theater, Performance and Duels tabs all follow them.
- **Bot detection:** players the replay flags as bots get a **Bot** tag, and the match list and match header count them. They're left out of *people you play with and against*. Rank averages use real players, and a team of only bots averages the bots' ranks.
- **Scope zoom** (theater): a tiny pill on the primary weapon's art shows its zoom while that player is scoped in. Weapons that switch zoom show their range with the current level lit, like Dawn at 1.5–2.5×, Champion and Calibrator at 1.25–2×, and Finale and Quasar at 2.5–4× with their High-zoom scope upgrade.
- **Fire modes** (theater): a pill beside it shows the current mode on weapons that have more than one, like Polaris (Auto or 3-burst), Judge and Maple Resonance (Auto or Semi), or Rainveil's 5-burst upgrade. Replays record each press of the switch key but not its result, so zoom and fire mode follow the presses since that player last spawned.

### Changed

- **Match list:** Team Arena and Team Deathmatch rows show your damage and headshot rate instead of ADR and KAST, how many players were bots, and no NOVA Impact. Team Deathmatch rows show all three team scores.
- **Scoreboard:** Team Arena and Team Deathmatch show the Combat stats that apply to them, without the Skill and Synergy pages.
- **Performance tab:** Team Deathmatch's player picker has a VS between each of the three teams.
- **Damage numbers** (theater): floating numbers, duel totals and the damage on team cards count up smoothly, and read exactly when paused.
- **Bomb panel** (theater): one bar fills over the fuse and a running defuse takes it over. Defused and Detonated now look the same, with the result beside the bomb icon and the defuser's avatar on it after a defuse.
- **Distance travelled** (theater): switches to kilometres past 1000 m.
- **Ultimates** (theater): Team Deathmatch has none, so player cards show only the active skill.
- **Theater footer:** the keyboard hints and map legend share one line, and the legend drops keys that don't apply to the mode.
- **Smoother theater:** playback only touches the feed rows, death marks and skill markers that changed, so a whole match plays as smoothly as a round.

### Fixed

- **Warmup kills:** Team Deathmatch's warmup was counted in kills, deaths and damage breakdowns. Totals now match the in-game scoreboard, and Team Arena and Team Deathmatch replays start when play goes live.
- **Day totals:** ADR and delta per round divided damage from Team Arena and Team Deathmatch by Demolition rounds only, which inflated them. They now use matches with rounds, and days without any show total damage and delta.
- **Discord status:** a Team Deathmatch result could show the wrong score. It now shows your team's score against the best other team.

### Note

- Your archived matches are read again after updating, so bots, teams, equipment and scope timings fill in for older matches too. This takes a few minutes the first time you open 0.3.1.

## 0.3.0: a scoreboard like the game's and a theater camera

### New

- **Scoreboard pages:** the scoreboard now has **Combat**, **Skill** and **Synergy** pages, like the game's own post-match screen.
  - **Combat:** the stats you know, with the score shown to two decimals as the game keeps it.
  - **Skill:** skill points, tactical and E uses, ultimates, damage dealt with character skills, and health and armor restored to teammates.
  - **Synergy:** synergy points, damage taken as the game counts it, plants, defuses and teammates rescued.
- **Halves:** buttons above the scoreboard switch between the **Full game**, the **1st half**, the **2nd half** and **Overtime**. Each shows your team's result in it and whether you were on attack or defense. Kills, damage, KAST, first kills, the game's scores and NOVA Impact all follow the half you pick, and so do the characters beside each name.
- **Open a player from the scoreboard:** click any row to jump to that player on the Performance tab.
- **Follow camera** (round theater): press **F** or the new button, and the map glides after the pinned player, or after you when no one is pinned. It snaps straight to them when you seek.
- **Map rotation** (round theater): turn the map a quarter at a time with **[** and **]**, and press **N** or click the compass to bring north back up. The map swings round smoothly instead of jumping.
- **Defuse progress:** the bomb panel shows the defuser, a progress bar and the seconds left. A defuse that stops part-way stays up with how far it got.
- **Fragrans' Aroma Surge:** fields now show their mode, **HP recovery** or **Speed boost**.
- **Backgrounds:** pick an app wallpaper in **Settings → Appearance**: the default, **Global Promotional** or **Season 26SP4**, both from the Strinova Wiki, under a dark wash so pages stay readable.

### Changed

- **Skill areas:** a skill's area now grows with the range upgrade its caster bought that round, like Fragrans' Aroma Surge. Hover the area to see the upgrade.
- **Copies of one skill:** several of the same object, like Mirage clones or Pawtectors, share one segmented health bar on the player card.
- **Zoom:** the theater's zoom slider moves evenly from 1× to 8×, and the map controls are grouped into zoom, rotation and camera.
- **Full screen:** the theater in full screen now covers always-on-top desktop widgets too, but only while it's the active window. Switching to another app drops it back behind.
- **Duels tab:** headline match-ups face off over a split bar, and the head-to-head grid uses tiles coloured by the net result, with totals for every player.
- **Economy tab:** each player's build shows as fixed upgrade slots (weapon, skills, defense), with this round's buys highlighted and A or B on each slot. Credits read as start → end with what was spent and earned, and the chart lines are smoother.
- **Performance tab:** *Versus opponents* shows kills and deaths as a tug bar, *Characters played* gets character art and ADR, and damage against each opponent is one dealt / received bar.
- **Spectators:** the spectator popup draws each person's watching sessions on a timeline of the replay.
- **NOVA Impact:** the card splits momentum into one bar by category, draws round impact as columns above and below zero, and has its own icon for every kind of play.
- **Icons:** the match tabs and the minimap legend have new icons that match the map's own markers.
- **Faster pages:** the profile page is kept between visits and only rebuilt when your matches, filters or game data change. Round theater playback redraws only the parts of a player card that changed, so it runs smoother.

### Fixed

- **Ammo glitches:** a replay glitch could briefly move rounds from the reserve into the magazine and back, which showed as a fake reload and could inflate the magazine size. These are now ignored.
- **Missing reloads:** a gun far from the player who recorded the replay could skip its reload entirely, so the magazine just jumped up. These reloads now show, timed like that gun's usual reload.
- **Kill causes:** a knocked player who bled out was listed as killed by *other*. The kill now goes to whatever knocked them down.

### Note

- Your archived matches are read again after updating, so the Skill and Synergy pages, halves and rescues fill in for older matches too. This takes a few minutes the first time you open 0.3.0.

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
