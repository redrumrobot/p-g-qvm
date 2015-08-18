# 1.6x #
## 1.6.5 ##
  * Damage done to self does not raise bleed counter. ([Issue 157](https://code.google.com/p/p-g-qvm/issues/detail?id=157))
  * BleedingSpree goes down when damage is done to other team, but at 1/3 the damage done ([Issue 157](https://code.google.com/p/p-g-qvm/issues/detail?id=157))
  * Admitdefeat votes cannot be spammed anymore by players, can't be called before `g_admitDefeatTime`, or by admin ([Issue 159](https://code.google.com/p/p-g-qvm/issues/detail?id=159))
  * Fixed bug in listplayers and lockname ([Issue 161](https://code.google.com/p/p-g-qvm/issues/detail?id=161))
  * Cleans up build near doors code ([Issue 163](https://code.google.com/p/p-g-qvm/issues/detail?id=163))
  * Adds `/devolve` command for aliens. Does not give credits back, player must have full health, and is cvar controlled by `g_allowDevolve` ([Issue 166](https://code.google.com/p/p-g-qvm/issues/detail?id=166))
  * Added silent specme, when `!specme s` is done by an admin (anyone with kick flag k), they are put to spec team, but it is not announced. ([Issue 168](https://code.google.com/p/p-g-qvm/issues/detail?id=168))
  * Increase max registered players. ([Issue 177](https://code.google.com/p/p-g-qvm/issues/detail?id=177))
## 1.6.2 ##
  * Teamstatus now flood limited, via cvar `g_teamStatusTime`, and updated quite a bit ([Issue 121](https://code.google.com/p/p-g-qvm/issues/detail?id=121))
  * New Marauder obituary (toggled via cvar `g_maraObituary`) ([Issue 125](https://code.google.com/p/p-g-qvm/issues/detail?id=125) and seperate cvar)
  * Added `!fireworks` command, flag `Y` ([Issue 126](https://code.google.com/p/p-g-qvm/issues/detail?id=126))
  * Added nobuild series of commands, `!nobuild` and `!nobuildsave`, flag `L` ([Issue 128](https://code.google.com/p/p-g-qvm/issues/detail?id=128))
  * Added /allstats command, cvar `g_allStats` controls who can see it (0=off, 1=teammates only, 2=serverwide) and `g_allstatsTime` controls the rate at which players can repeat command. ([Issue 123](https://code.google.com/p/p-g-qvm/issues/detail?id=123)) ([Issue 139](https://code.google.com/p/p-g-qvm/issues/detail?id=139))
  * Cleaned up name sanitize to filter ALL non-visible ascii characters (boxes) ([Issue 131](https://code.google.com/p/p-g-qvm/issues/detail?id=131))
  * Added `!grab` command ([Issue 135](https://code.google.com/p/p-g-qvm/issues/detail?id=135)) ([Issue 135](https://code.google.com/p/p-g-qvm/issues/detail?id=135)) ([Issue 138](https://code.google.com/p/p-g-qvm/issues/detail?id=138))
  * Removed `!mix`, `!switch`, `!trade`, `!steal`, `!explode` ([Issue 138](https://code.google.com/p/p-g-qvm/issues/detail?id=138))
  * Added `!bring` command, brings the admin who ran it as a spectator to another spectators point of view. ([Issue 138](https://code.google.com/p/p-g-qvm/issues/detail?id=138))
  * Added cvar controlling many wallwalk hovel glitches, `g_wwNoHovelBuild` ([Issue 136](https://code.google.com/p/p-g-qvm/issues/detail?id=136))
  * Hardcoded `!info credits` into qvm, now server operators dont have to upload 2 files. ([Issue 140](https://code.google.com/p/p-g-qvm/issues/detail?id=140))
## 1.6.1 ##
  * Added Teamstatus command `/teamstatus`. Shows you the status of your base (nodes/eggs, om/reac, etc). Cvar `g_teamStatus` to toggle ([Issue 120](https://code.google.com/p/p-g-qvm/issues/detail?id=120))
  * Added Welcome Messages feature. Sends welcome messages to connecting players. `g_welcomeMsg` is message sent to players (supports \n), `g_welcomeMsgTime` is the duration of display. ([Issue 118](https://code.google.com/p/p-g-qvm/issues/detail?id=118))
  * Increased `!listmaps` display to 256. ([Issue 117](https://code.google.com/p/p-g-qvm/issues/detail?id=117))
  * Fixed Medi-Radioactive Rets glitch ([Issue 116](https://code.google.com/p/p-g-qvm/issues/detail?id=116))
  * Fixed vote math issues with 50%. ([Issue 115](https://code.google.com/p/p-g-qvm/issues/detail?id=115))
  * Added instant build, `g_instantBuild`. ([Issue 112](https://code.google.com/p/p-g-qvm/issues/detail?id=112))
  * Changed `qvm_version` appearance, removed website, added time.
## 1.6 ##
  * Major cleanup to code
  * Added semi mark fix and designate fix, now, on aliens reload works as protect when designated, and if not designated on either team reload is mark. ([Issue 84](https://code.google.com/p/p-g-qvm/issues/detail?id=84))
  * Added medi-stat shove control, `g_healShove` 1=can be shoved, 0=cant ([Issue 85](https://code.google.com/p/p-g-qvm/issues/detail?id=85))
  * `g_modHumanStamina` now affects jumps ([Issue 86](https://code.google.com/p/p-g-qvm/issues/detail?id=86))
  * Added high turret angles, `g_modTurretAngles` ([Issue 87](https://code.google.com/p/p-g-qvm/issues/detail?id=87))
  * Changed `!demo` flag to match adminchat flag ?
  * Added patch to allow chat messages in messagemode, similar to /m ([Issue 92](https://code.google.com/p/p-g-qvm/issues/detail?id=92))
  * Added patch to fix medi slow heals ([Issue 90](https://code.google.com/p/p-g-qvm/issues/detail?id=90))
  * Reduced feeding spree near base ([Issue 89](https://code.google.com/p/p-g-qvm/issues/detail?id=89))
  * Added `!practice` command, allows for temporary clan practice, based on tag. Flag [ ([Issue 94](https://code.google.com/p/p-g-qvm/issues/detail?id=94))
  * Changed `/builder` flag to )
  * Fixed class changes
  * Added `!tklog` flag t
  * Added `!outlaw` (flag O) commands, punishes bleeders and tkers, cvar `g_bleedingSpree` ([Issue 97](https://code.google.com/p/p-g-qvm/issues/detail?id=97))  ([Issue 99](https://code.google.com/p/p-g-qvm/issues/detail?id=99)) ([Issue 100](https://code.google.com/p/p-g-qvm/issues/detail?id=100))
  * Added PTRC abuse prevention, complete with admin warning
  * Added `qvm_version` cvar, this qvm is part of the `qvm_` cvar initiative
  * Radioactive turrets off by default now
  * People who are affected by `g_newbieNamePrefix` can have building disabled for them via `g_newbieNoBuild`. Message to players can be changed via `g_newbieNoBuild` ([Issue 107](https://code.google.com/p/p-g-qvm/issues/detail?id=107))
  * Fixed feeding spree ([Issue 108](https://code.google.com/p/p-g-qvm/issues/detail?id=108))
  * Fixed typo in !l0 print output ([Issue 109](https://code.google.com/p/p-g-qvm/issues/detail?id=109))
  * Added sanitise name fix ([Issue 111](https://code.google.com/p/p-g-qvm/issues/detail?id=111))
  * Added random maprotation slot ([Issue 106](https://code.google.com/p/p-g-qvm/issues/detail?id=106))
  * Added fix for vote math, no more annoying (66 percent) needed 66 percent to pass ([Issue 110](https://code.google.com/p/p-g-qvm/issues/detail?id=110))
# 1.5x #
## 1.5.2x ##
### 1.5.2 ###
  * Changed !demo flag to ~ (to match adminchat flag.)
  * Fixed box characters that occasionally appear with line endings in !info
  * Added Chat channels, see [[Chat](Chat.md)] for more information
  * Added console check to !demo
  * Added `g_deconTime` to prevent deconning at beginning of match
  * Added !flag command, see [[flag](flag.md)] for more information
  * Added Killing/Feeding spree. Kill a lot, and the price on your head goes up. Feed a lot, and you wait before spawning.
    * `g_killingSpree` is amount of kills to be considered a spree. 0 disables
    * `g_feedingSpree` is amount of feeds. 0 disables
## 1.5.1x ##
### 1.5.1 ###
  * Added improved mark deconstruct, adds a second mode (2) to `g_markDeconstruct`, allowing use of regular decon as well as `/mark` command. ([Issue 61](https://code.google.com/p/p-g-qvm/issues/detail?id=61))
  * Added `g_adminMaxBan`, when set, only allows admins to ban up to a certan number of days. If !ban is run without a duration, it matches `g_adminMaxBans`. Admins with flag `8` are immune. ([Issue 65](https://code.google.com/p/p-g-qvm/issues/detail?id=65))
  * Added layout votes. Can be called with `/callvote layout layoutname`. Follows same restrictions as map votes ([Issue 66](https://code.google.com/p/p-g-qvm/issues/detail?id=66))
  * `!listlayouts` flag changed to `j`, as with `!listmaps` ([Issue 66](https://code.google.com/p/p-g-qvm/issues/detail?id=66))
## 1.5.0x ##
### 1.5.0.4 ###
  * Added bugfixes for builder, now much more useful command. (See [Issue 64](https://code.google.com/p/p-g-qvm/issues/detail?id=64))
  * Added extreme mod
    * `g_modBuildableHealth`: Buildable health **(Percent)**
    * `g_modBuildableSpeed`: Buildable fire rate **(Percent)**
    * `g_modHumanStamina`: Human stamina **(Percent)**
    * `g_modHumanHealth`: Human health **(Percent)**
    * `g_modAlienHealth`: Alien health **(Percent)**
    * `g_modHumanRate`: Human fire rate **(Percent)**
    * `g_modAlienRate`: Alien fire rate **(Percent)**
    * `g_modWeaponAmmo`: Weapon ammo per clip **(Percent)**
    * `g_modWeaponReload`: Adjust's Weapon reload time **(Percent)**
### 1.5.0.3 ###
  * Added /builder command, flag +. Shows the builder of a building.
  * Increased amount of flags and commands to 128
### 1.5.0.2 ###
  * Added !demo command
### 1.5.0.1 ###
  * Added fixes for !denyweapon
### 1.5 ###
  * Prevented purchase of bsuit when crouched, prevents bsuit crouch glitch
  * Added cvar `g_devmapVotes`, switches map votes to devmap votes
  * Added proxemity mines (grenades), `g_proximityMines`
  * Added !denyweapons/!alloweapons
  * Added search to !listmaps
  * Added maplog fixes, adds devmap info
  * Improved black name filter
  * Added timed messages, `g_msg` controls the message, `g_msgtime` controls the repeat rate
  * Added feature to echo cp to player consoles
  * Added newline support to !cp
  * Added vote logging to !adminlog
  * Added location data to say\_area, `g_sayAreaLocations`
  * Added `g_specASpec`, allows spectators to follow other spectators
# 1.4x #
## 1.4.5 ##
  * Long awaited `!credits` function finally here
  * Indentation fixed for admin commands
## 1.4.4.2 ##
  * Added Vote CP messages and percent notice on vote pass
## 1.4.4.1 ##
  * Fixed ugly bug with prefix.
## 1.4.4 ##
  * Added color to chat team prefixes
  * Added Logfile decolor
  * Removed normal property from customgrav, now !customgrav playername without any argument for gravity sets gravity to zero
  * Removed console prevention of commands (!drug, !explode, !customgrav), now console can actually run them on other players.
  * Added flood protect to share and donate
## 1.4.3.1 ##
  * Fixed !drop, now supports spaces.
  * Fixed !trade and !steal, players can no longer go above their own health max.
## 1.4.3 ##
  * Poll votes now start with 0 yes and 0 no (and no divide by 0 error)
  * Teamvotes now only pass if 50% of team votes, and of that 50%, majority wins
  * Admitdefeat votes now have percentage `(g_admitDefeatVotePercent)`
  * Map bounds spawn fix, now players cant mess up spawn cue by falling out of map (not in any stock maps, but in a few betas this is a problem)
  * Enhanced register: Register can be set up to have a password that sets players to a specific level:
    * New syntax for register: !register _[level](level.md) [password](password.md)_
    * !register 0 sets you back to level 0
    * `g_adminRegisterAdminLevel` new setting, sets how high a level can be set with password
    * `g_adminRegisterAdminPass` new setting, password required to get up above _g\_adminRegisterAdminLevel_. Blank by default, disables
    * `g_adminRegisterLevel` new setting, sets how high an unpassworded register can get.
    * **WARNING: PASSWORDS CAN BE SEEN IN PUBLIC CHAT IF ADMIN MESSES UP, OR g\_adminSayFilter IS NOT ENABLED. ESCAPE COMMAND WITH /!register.
  * Credit overflow is back, but in a much cleaner form.
    * `g_creditOverflow`
      ***0**: Disabled
      ***1**: Overflow to every teammate, cycles in slot order.
      ***2