# DESTROYMC.NET Server Setup

DMC had 2 servers and 1 proxy to connect them.
1. Waiting Server - Used as a "buffer" server from the main one. Uses a captcha to prevent bots from joining the main server.
2. Main Server - The main survival server.

I used Purpur on the backend servers and Waterfall for the proxy.

## Configuration
These are the configuration files I used for the server. They will probably be outdated pretty soon.
* [Proxy](https://github.com/DESTROYMC-NET/Server-Info/tree/master/Proxy-Server)
* [Waiting Server](https://github.com/DESTROYMC-NET/Server-Info/tree/master/Waiting-Server)
* [Main Server](https://github.com/DESTROYMC-NET/Server-Info/tree/master/Main-Server)

## Plugins
I've gotten many requests to show what plugins I used, so here they are.

### Proxy Plugins
* [BungeeGuard](https://github.com/lucko/BungeeGuard) - Prevent players from joining the backend servers. Sends an extra token with players to confirm they are connecting only through the proxy.
* [DeluxeQueues](https://www.spigotmc.org/resources/deluxequeues-20-sale-titlebars-actionbars-donor-bypass-and-more.69390/) - This is the queue system the server used. However, it was never used but it was there just in case.
* [DMC-MOTD](https://github.com/DESTROYMC-NET/DMC-MOTD) - Custom MOTD plugin I wrote since I didn't like any other ones.
* [LuckPerms](https://luckperms.net/) - Permission plugin I used. I used a database to sync the perms between the backend servers.
* [PremiumVanish](https://www.spigotmc.org/resources/premiumvanish-stay-hidden-bungee-support.14404/) - The vanish plugin I used.
* [TCPShield](https://github.com/TCPShield/RealIP) - I used TCPShield for DDoS protection. This plugin forwards the real IPs of players to the server. Otherwise, it will show the proxy IP's instead.
### Waiting Server Plugins
* [BungeeGuard](https://github.com/lucko/BungeeGuard) - Prevent players from joining the backend servers. Sends an extra token with players to confirm they are connecting only through the proxy.
* ConditionalCommands - This plugin is a helper plugin for NCP.
* [Holograms](https://www.spigotmc.org/resources/holograms.4924/) - The floating text that showed information.
* [HologramsPlaceholders](https://www.spigotmc.org/resources/holograms-placeholders.19813/) - Allows placeholders in holograms.
* [LuckPerms](https://luckperms.net/) - Permission plugin I used. I used a database to sync the perms between the backend servers.
* [Mapcha](https://github.com/DESTROYMC-NET/mapcha) - My own fork of Mapcha. There were some small changes I made that are listed on the GitHub.
* [NoCheatPlus](https://www.mc-market.org/resources/475/) - An updated fork of NCP.
* [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/) - Allows placeholders to show information.
* [PremiumVanish](https://www.spigotmc.org/resources/premiumvanish-stay-hidden-bungee-support.14404/) - The vanish plugin I used.
* [Protocollib](https://www.spigotmc.org/resources/protocollib.1997/) - Library for other plugins.
* [TabList](https://www.spigotmc.org/resources/animated-tab-tablist.46229/) - The custom tab menu plugin.
* [ViaBackwards](https://www.spigotmc.org/resources/viabackwards.27448/) - Allows older versions of Minecraft to connect to newer ones.
* [ViaVersion](https://www.spigotmc.org/resources/viaversion.19254/) - Allows multiple versions of Minecraft to connect.
* [VoidGenerator](https://www.spigotmc.org/resources/voidgenerator.25391/) - Generates an empty void world.
* [WaitingServerUtilities](https://github.com/DESTROYMC-NET/WaitingServerUtilities) - My custom plugin I used to do some various things.
### Main Server Plugins
* [BungeeGuard](https://github.com/lucko/BungeeGuard) - Prevent players from joining the backend servers. Sends an extra token with players to confirm they are connecting only through the proxy.
* [ChatControl](https://www.spigotmc.org/resources/chatcontrol%E2%84%A2-the-ultimate-chat-plugin-500-000-downloads-1-2-5-1-16-2.271/) - The chat system plugin, I main used it for prefix formatting to allow colored names.
* ConditionalCommands - This plugin is a helper plugin for NCP.
* [DeathMessagesPrime](https://www.spigotmc.org/resources/deathmessagesprime.3789/) - Custom death messages.
* DestroyMC-Main - This plugin is the main "controller." However, I have split this plugin up since it was a big mess. Here are the seperate plugins:
    * [NoNetherFun](https://github.com/DESTROYMC-NET/NoNetherFun) - Block placing and breaking blocks above the Nether roof.
    * [WorldStats](https://github.com/DESTROYMC-NET/WorldStats) - The /info command that shows server age, total players, and world size.
    * [SimpleMessage](https://github.com/DESTROYMC-NET/SimpleMessage) - The messaging and ignore system.
    * [TabCompleter](https://github.com/DESTROYMC-NET/TabCompleter) - Blocks commands that are not on a list. Used to prevent random command usage.
    * [PlayerTracker](https://github.com/DESTROYMC-NET/PlayerTracker) - The /player command. It probably works fine.
* [DMPEnderCrystal](https://www.spigotmc.org/resources/dmpendercrystal.74768/) - Allows end crystals to have killers in the messages.
* [DMPHideMessages](https://www.spigotmc.org/resources/dmphidemessages.43080/) - Allows players to hide death messages for certain players.
* [FarmLimiter](https://www.spigotmc.org/resources/farm-limiter.1419/) - Limits the amount of mobs in a given area. I added this originally because someone had a spider farm that kept on spawning and killed the server.
* [FastAsyncWorldEdit](https://www.spigotmc.org/resources/fast-async-worldedit.13932/) - WorldEdit but better.
* [Inventory Restore](https://www.spigotmc.org/resources/inventory-restore-remastered.22027/) - Saves inventories on death and allows to rollback. I only used this when the anti-cheat threw people into the void.
* [Invsee](https://www.spigotmc.org/resources/invsee.60500/) - See a player's inventory.
* [LuckPerms](https://luckperms.net/) - Permission plugin I used. I used a database to sync the perms between the backend servers.
* [NuVotifier](https://www.spigotmc.org/resources/nuvotifier.13449/) - An updated version of Votifier.
* [PartyChat](https://github.com/DESTROYMC-NET/PartyChat) - My custom party chat plugin.
* [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/) - Allows placeholders to show information.
* [Plan](https://www.spigotmc.org/resources/plan-player-analytics.32536/) - Track player stats. I only added this plugin in November of 2019.
* [PremiumVanish](https://www.spigotmc.org/resources/premiumvanish-stay-hidden-bungee-support.14404/) - The vanish plugin I used.
* [Protocollib](https://www.spigotmc.org/resources/protocollib.1997/) - Library for other plugins.
* [Spark](https://www.spigotmc.org/resources/spark.57242/) - This plugin is a performance sampler. I never really used this, I used normal timings instead.
* [SuperbVote](https://www.spigotmc.org/resources/superbvote.11626/) - Gives players voting rewards. This plugin was responsible for giving players colored names.
* [TabList](https://www.spigotmc.org/resources/animated-tab-tablist.46229/) - The custom tab menu plugin.
* [Vault](https://www.spigotmc.org/resources/vault.34315/) - An API plugin. This was used for the colored names.
* [ViaVersion](https://www.spigotmc.org/resources/viaversion.19254/) - Allows multiple versions of Minecraft to connect.
* [VoidGenerator](https://www.spigotmc.org/resources/voidgenerator.25391/) - Generates an empty void world.
