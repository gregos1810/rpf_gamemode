# rpf_gamemode
RPF STUDIO DEVELOPEMENT

Game mode pour serveur Fivem comme gta 5 online sur base vrp version Beta 1.5 WIP

https://github.com/ImagicTheCat/vRP/releases/tag/0.5

SERVER.CFG ----------------------------------------------------------------------------------------

# Only change the IP if you're using a server with multiple network interfaces, otherwise change the port only.
# Only change the IP if you're using a server with multiple network interfaces, otherwise change the port only.
endpoint_add_tcp "0.0.0.0:30120"
endpoint_add_udp "0.0.0.0:30120"

set mysql_connection_string "server=localhost;database=vrp;userid=root;password="

# These resources will start by default.
start baseevents
start mapmanager
start sessionmanager
start hardcap
start rconlog

#RPF_GAMEMODE_SCRIPT

start rpf_main
start rpf_notif
start rpf_baseapps
start rpf_phone
start rpf_police
start rpf_garages
#start rpf_missions Ne pas mettre en route ! Dont use for now !
start rpf_sync
start rpf_utils

#VRP_SCRIPT

start vrp_mysql
start vrp

set discord_reporting_url "RPF Studio 1.5 Beta" 

# This allows players to use scripthook-based plugins such as the legacy Lambda Menu.
# Set this to 1 to allow scripthook. Do note that this does _not_ guarantee players won't be able to use external plugins.
sv_scriptHookAllowed 0

# Uncomment this and set a password to enable RCON. Make sure to change the password - it should look like rcon_password "YOURPASSWORD"
rcon_password "tuning"

# A comma-separated list of tags for your server.
# For example:
# - sets tags "drifting, cars, racing"
# Or:
# - sets tags "roleplay, military, tanks"
sets tags "freeroam, rpf, libre, mod, map, france, arenawar, mission, pis"

# Set an optional server info and connecting banner image url.
# Size doesn't matter, any banner sized image will be fine.

sets banner_detail "https://i.ytimg.com/vi/AtqAoHEoox0/maxresdefault.jpg"

sets banner_connecting "https://i.ytimg.com/vi/AtqAoHEoox0/maxresdefault.jpg"

# Set your server's hostname
sv_hostname "RPF Studio ^81.5 | ^9Beta 1.5"

# Nested configs!
#exec server_internal.cfg

# Loading a server icon (96x96 PNG file)
load_server_icon logo.png

# convars which can be used in scripts
set temp_convar "hey world!"

# Uncomment this line if you do not want your server to be listed in the server browser.
# Do not edit it if you *do* want your server listed.
#sv_master1 ""

# Add system admins
add_ace group.admin command allow # allow all commands
add_ace group.admin command.quit deny # but don't allow quit
add_principal identifier.steam:110000100000000 group.admin # add the admin to the group

# Hide player endpoints in external log output.

set sv_authMaxVariance 1
set sv_authMinTrust 5
set sv_endpointprivacy true
set sv_maxclients 32
set con_disableNonTTYReads 1


# Server player slot limit (must be between 1 and 32, unless using OneSync)
sv_maxclients 32

# License key for your server (https://keymaster.fivem.net)
sv_licenseKey 

set pause_menu_title "RPF Studio RP Libre 1.5"
set discord_reporting_url ""
