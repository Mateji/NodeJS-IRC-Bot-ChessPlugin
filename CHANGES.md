12/23/2011
==========
* ADDED:
*   couchdb_log plugin -- logs all events (except privmsg to the bot) to a couchdb instance
*   coucbdb_seen plugin -- utilizes the logs from couchdb_log to generate intelligent last seen reports
*        -- Also supports formatted responses
*   freenode plugin -- identifies the bot to nickserv once connected to the network
*   trac plugin -- interfaces with trac instance over RPC for #ticket data and via scraping for [changeset] data
*
* UPDATED:
*   irc.js/user.js/channel.js Fixed problem with user tracking in memory

12/20/2011
==========
* ADDED:
*   User/Channel tracking via global hashes irc.users and irc.channels
*   User object via user.js
*   Added irc.send(target, msg) command to elimiate .raw() calls to send messages to users and channels
*   onNumeric event for plugins - triggers on any numeric response such as /WHOIS response
*
* UPDATED:
*   Channel object to support tracking users
*   Existing modules for new User/Channel objects
*
* DEPRECATED:
*   onReply - replaced by onNumeric hook -- will remove sometime after the new year
*
*
* Reformatted all the files to match my typical coding style

05/03/2011
==========
* Created a temporary onReply listener
* Added a global plugin and moved joining the main channel to the plugin

04/03/2011
==========
* Added debug to configuration