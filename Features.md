The p-g-qvm has the largest featureset of any qvm, and as such, can be quite exhausting to hunt down and find each feature. Here is a list of all the features.

# Admin Commands #
QVM uses lakitu7's patch, and therefore has all admin and Lakitu7 commands.
  * **!flag and !unflag** (f): Adjust per-user flags on the fly. Very powerful command, see [[flag](flag.md)] for information
  * **!seen** (D): Shows the last time a (registered) player was on the server. Prints out 10 name matches. (Saved in chat.dat)
  * **!demo** (~): Allows admins to toggle sending of admin warnings to themselves. Designed for demo recording
  * **!denyweapon** (d): Allows you to deny or allow a weapon for someone to use. If they are holding that weapon, it removes it from them, and repays them. Works with alien classes too
  * **!adminlog:** (A): Shows a log of reciently run admin commands.
  * !**forcespec/!unforcespec** (F): Disable the ability of a player to join any team. If the player is playing the game, they are removed and forced to spectator.
  * **!pause/!unpause** (S): Freeze a player where they are currently positioned. The freezed player cannot take any damage, give any damage, die, or move. They may rotate their view though. Works on spectators. _Note: Pause whole game feature removed due to [Bug 1](http://code.google.com/p/p-g-qvm/issues/detail?id=1)_
  * **!buildlog** (U): Displays a list of recent builds. Running the newest version, with advanced syntax.
  * **!revert** (U): Reverts a build action. Latest action. Uses advanced syntax.
  * **!slap** (x): Does damage to a player, and sends them flying.
  * **!l0** (l): Removes the admin of a level 1 admin. Used shares !l1 flag.
  * **!switch** (X): swaps places with any other player in the game, even spectators.
  * **!mix** (X): Mixes any other player into yourself. If both players are members of a team, you will generally get a bastard creature that cannot move, but can damage each other. If run on a spectator, it will force a spectator to look at the player (not follow, but look)
  * **!steal** (T): Lets you steal health from another player. Does health in increments of 5.
  * **!trade** (t): Lets you trade health with another player. They get yours and you get theirs. You cannot exceed your maximum health. Health is by number, and not percent, so if a full hp human trades with a dretch, the dretch will remain the same, but the human will only have 25 hp.
  * **!drug** (Q): Applies a poison effect to a player, like basilisk gas.
  * **!drop** (o): Drops a player from the server, without any log, any temporary ban, or any reason. Client sees server disconnected. Useful for ejecting laggers from server. Specify a reason by adding reason after name.
  * **!cp** (Z): Center prints a message to all players. This works exactly like the cp console command, except that this does not support \n newlines.
  * **!customgrav** (Q): Sets the gravity for ONE player. Run without a gravity paramiter to match server gravity.
  * **!explode** (Q): Causes a player to instantly explode, as if they blew up a grenade. Does same amount of damage as grenade, with same radius of splash. Affects structures or close players too.
  * **!listmaps** (j): Displays a listing of ALL the maps on the server, by the name the server calls them.
  * **!maplog** (j): Shows a list of the 5 most recently played maps.
  * **!immunity** (I): Gives a player immunity from an IP ban. Player must have GUID and be registered with the server. Does nothing against GUID bans. Uses same flag as !ban.
  * **!suspendban** (J): Suspends a ban in !showbans for up to 14 days.
  * **!register** (R): Registers a player with the server. Supports advanced register features. !register 0 sets a player to level 0. !register [level](level.md) [pass](pass.md) sets a player to a level, if the proper password is given.
    * _g\_adminRegisterLevel_: Level to which a normal register sets to. Default 1
    * _g\_adminRegisterAdminPass_: Password required to get to levels set by `g_adminRegisterAdminLevel`. Blank is default, and disabled
    * _g\_adminRegisterAdminLevel_: Level to which password registrations go. Default is 0.
    * **WARNING: IF PASSWORDS ARE TYPED IN CHAT, AND `g_adminSayFilter` IS OFF, THEN PASSWORD WILL BE DISPLAYED IN CHAT. TO OVERCOME THIS, USE ESCAPED SYNTAX (/!register)
  ***!credits**(u): Add or remove credits from a player (good for paying back that poor sap who you just !explode'd). Anti-abuse prevents players from modifying their own credit amount.**

# Other Features #
  * Chat channels: Multiple chat channels in tremulous! This is a huge feature, so see [[Channels](Chat.md)] for information.
  * /mark: When `g_markDeconstruct` is set to `2`, allows use of `/mark` command, marking or unmarking a building for deconstruction.
  * Layout votes: adds new vote type `layout`. Called by `/callvote layout LAYOUTNAME`. Subject to same restrictions as all other map votes.
  * /builder (+): shows the builder of a structure and its buildlog number.
  * Force mapvotes to be devmapvotes `g_devmapVotes`
  * CP messages logged to console
  * Repeating messages, `g_msg` and `g_msgTime`
  * Players cant crouch as bsuit, or buy a bsuit while crouching
  * NO BLACK IN NAMES, PERIOD
  * !listmaps search
  * Votes logged in !adminlog
  * !Maplog shows devmap
  * Decolor log files, controlled by `g_decolorLogfiles`
  * Poll vote caller can vote no
  * Players that fall out of map die instantly, and cannot mess up spawn cue
  * Credit overflow
  * Teamvotes much more fair now, and admitdefeat has percent control.
  * FF percent retribution
  * Newline for console cp. Use \n to insert line breaks in
  * Extend votes, controlled by cvars beginning with `g_extend`
  * Buy anything, allows you to buy buildings and alien classes. `g_buyAll`
  * Multiple weapon slots allow players to hold more than one weapon. `g_multipleWeapons`
  * Control over poll votes. `g_pollVotes`
  * Faster, more powerful granger spit. Does same damage as blaster, at same repeat rate
  * Reasons for Mute and Kick votes are required
  * Search for !showbans, let you look for a name or IP
  * Adminchat warnings. Know when a player tries to do something they shouldnt be able to, or a banned player tries to connect.
  * Killer HP. When someone kills someone else, it tells you the killer's remaining HP. Cvar controlled, `g_killerHP`
  * Radioactive turrets feature. Does damage to camping humans. Controlled by cvars beginning with `g\_radiation'
  * Teamvotes accept normal yes/no if no other vote in progress
  * Vote connect time prevents players from connecting and calling a vote within g\_voteMinTime, or call a map vote within g\_mapvoteMinTime

# Cvars #
  * `g_killingSpree`: Amount of kills considered a spree. When a user gets a spree, the price on their head goes up, awarding the killer more. 0 disables. **(Integer)**
  * `g_feedingSpree`: Amount of feeds before player is made to wait longer to spawn. 0 disables. **(Integer)**
  * `g_chat`: Chat.dat file, controlling the chat user channel information **(String ending in .dat)**
  * `g_deconTime`: Time in which a player must wait to decon reactor/overmind at start of map. -1 makes it so 2/3 of all players must be connected, otherwise it is amount of seconds. **(Seconds Integer or -1)**
  * `g_markDeconstruct`: Added mode 2, allows use of `/mark` command. **(Bitmask)**
  * `g_adminMaxBan`: Allows the maximum ban length of admins without `8` flag to be limited. Cvar is in days. **(Number)**
  * `g_modBuildableHealth`: Buildable health **(Percent)**
  * `g_modBuildableSpeed`: Buildable fire rate **(Percent)**
  * `g_modHumanStamina`: Human stamina **(Percent)**
  * `g_modHumanHealth`: Human health **(Percent)**
  * `g_modAlienHealth`: Alien health **(Percent)**
  * `g_modHumanRate`: Human fire rate **(Percent)**
  * `g_modAlienRate`: Alien fire rate **(Percent)**
  * `g_modWeaponAmmo`: Weapon ammo per clip **(Percent)**
  * `g_modWeaponReload`: Adjust's Weapon reload time **(Percent)**
  * `g_decolorLogfiles`: Enables/disables removal of color tags from log files. **(Boolean)**
  * `g_devmapVotes`: Forces mapvotes to be devmapvotes **(Boolean)**
  * `g_specASpec`: Allows speccing of other spectators **(Boolean)**
  * `g_proximityMines`: Turns grenades into mines **(Boolean)**
  * `g_msg`: Sets message to be repeated **(String)**
  * `g_msgTime`: Sets message repeat rate in minutes **(Integer)**
  * `g_sayAreaLocations`: Adds location data to say\_area **(Boolean)**
  * `g_admitDefeatVotePercent`: Sets the percentage at which admitdefeat teamvotes must have to pass **(Integer)**
  * `g_creditOverflow`: Overflows the credits of full players to others. 0 disables, 1 gives to teammates in slot order, 2 gives to highest scoring teammates. **(Bitmask)**
  * `g_adminRegisterLevel`: Level to which a normal register sets to. Default 1 **(Integer)**
  * `g_adminRegisterAdminPass`: Password required to get to levels set by `g_adminRegisterAdminLevel`. Blank is default, and disabled **(String)**
  * `g_adminRegisterAdminLevel`: Level to which password registrations go. Default is 0. **(Integer)**
  * `g_killerHP`: Shows a victim how much health their killer had. **(Boolean)**
  * `g_pollVotes`: Control if poll votes are enabled or disabled. **(Boolean)**
  * `g_extendVotePercent`: Percent for extend votes to pass. **(Float)**
  * `g_extendVote`: Controls if extend votes are enabled. **(Boolean)**
  * `g_extendVotesPercent`: Controls the percent extend votes must have to pass. **(Float)**
  * `g_extendVotesTime`: Controls the amount of time extend votes push the time limit back by. **(Float)**
  * `g_extendVotesCount`: Controls how many extend votes may be called and passed during a game. **(Float)**
  * `g_buyAll`: Allows the purchase of any item while on the human team. **(Boolean)**
  * `g_multipleWeapons`: Allows humans to carry more than one main weapon. **(Boolean)**
  * `g_radiationDamage`: Amount of damage given by radiation. **(Float)**
  * `g_radiationTime`: The amount of time spent camping near turrets to engage irradiation. **(Float)**
  * `g_radiationCredits`: Amount of credits a player must have to be damaged. **(Float)**
  * `g_radiationCreditsCount`: Way the game counts credits. 0 for only current equipment, 1 for players account, 2 for both account and current equipment. **(Bitmask)**
  * `g_voteMinTime`: Amount of time a player must be connected to server to call a vote. **(Integer)**
  * `g_mapvoteMinTime`: Amount of time a player must be connected to call a mapvote. **(Integer)**

There are many other features that i cant name off the top of my head, so feel free to update this page as you find them.

Thank you