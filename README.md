# munin-plugins-my
A set of Munin (http://munin-monitoring.org/) plugins for OpenConnect, I2Pd, XRay, QBittorrent, Snowflake, etc.

# I2Pd
Munin plugin for I2Pd (https://github.com/PurpleI2P/i2pd)

Filename: i2pd_

Available symlinks: i2pd_traffic, i2pd_routers, i2pd_successrate, i2pd_status, i2pd_transits

Parameters: env.host (localhost), env.port (7650), env.password (itoopie)

![Routers](docs/i2pd_routers-day.png?raw=true "Routers")

![Status](docs/i2pd_status-day.png?raw=true "Status")

![Success rate](docs/i2pd_successrate-day.png?raw=true "Success rate")

![Traffic](docs/i2pd_traffic-day.png?raw=true "Traffic")

![Transit tunnels](docs/i2pd_transits-day.png?raw=true "Transit tunnels")

# OpenConnect VPN server
Munin plugin for OpenConnect VPN server (OCsev - https://gitlab.com/openconnect/ocserv)

Files: ocserv_, ocserv_users_ ocserv_vhosts

Available symlinks (from ocserv_): ocserv_traffic, ocserv_sessions, ocserv_bans

Dependencies: jq, occtl

![Sessions](docs/ocserv_sessions-day.png?raw=true "Sessions")

![Sessions per vhost](docs/ocserv_sessions_vhosts-day.png?raw=true "Sessions per vhost")

![Sessions per user](docs/ocserv_users-day.png?raw=true "Sessions per user")

![Traffic](docs/ocserv_traffic-day.png?raw=true "Traffic")

Due to OCServ architecture specifics, it's not possible to retrieve real-time traffic data, so only the total traffic for each finished session is displayed.

# Snowflake (Tor pluggable transport)

Munin plugin for Tor pluggable transport named Snowflake (https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake)

Files: snowflake_

Available symlinks: snowflake_sessions, snowflake_traffic

Parameters: env.logfile (/var/log/snowflake.log)

![Sessions](docs/snowflake_sessions-day.png?raw=true "Sessions")

![Traffic](docs/snowflake_traffic-day.png?raw=true "Traffic")

# qBittorrent-nox

Munin plugin for qBittorrent-nox (https://github.com/qbittorrent/qBittorrent)

File: qbt_

Available symlinks: qbt_traffic, qbt_transfers

Parameters: env.host (localhost), env.port (55556)

![Transfers](docs/qbt_transfers-day.png?raw=true "Transfers (day)")

![Transfers](docs/qbt_transfers-week.png?raw=true "Transfers (week)")

![Traffic](docs/qbt_traffic-day.png?raw=true "Traffic")

# XRay-core

Munin plugin for XRay-core (https://github.com/XTLS/Xray-core). After some adaptation could also work with V2Ray-core.

File: xray_

Available symlinks: xray_user, xray_inbound, xray_outbound

Parameters: env.cmd (/opt/xray/xray api statsquery), env.server (127.0.0.1:5001),  env.config (/opt/xray/config.json)

Dependencies: jq, md5sum

![Inbounds traffic](docs/xray_inbound-day.png?raw=true "Inbounds traffic")

![Users traffic](docs/xray_user-day.png?raw=true "Users traffic")



