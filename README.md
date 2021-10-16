# Plex-Tools
Plex - Monitoring and Stats
Monitoring of PLEX application using zabbix or graphane.

### Monitored
Plex transcode folder size
Plex size of shared libraries
Plex Media Server Subzero Logs
Plex Media Server Logs
Errors present in Plex Media Server log
Plex - Websocket messages per second
Plex - Transcode streams
Plex - Total streams
Plex - Server port status
Plex - Server port performance
Plex - Number of web threads
Plex - Errors per second in Plex Media Server logs
Plex - Direct stream
Plex - Direct play streams
Plex - Conversions


# Requirements for zabbix version:
- Plex Media server (linux)
- Zabbix 5.4+
- Tautulli - A Python based monitoring and tracking tool for Plex Media Server
- Vnstat
- 
# Requirements with grafana version:
- Plex Media server (linux)
- Zabbix 5.4+
- Grafana
- GeoLite2 Free Geolocation Data (for maps)
- Python 3.6.7+
- Python3-pip
- InfluxDB 1.8.x
- Tautulli - A Python based monitoring and tracking tool for Plex Media Server.
- Varken

# Key Features
- Zabbix Agent (Active)
- Bandwidth by Day/Month/All Time
- Bandwidth by Receive/Transmit/Total
- Graphs For each Day/Month/All Time per Receive/Transmit/Total/Stacked
- Triggers


# Install 
apt-get update
apt-get install vnstat
service vnstat restart
service zabbix-agent restart

#Instal and Upgrade requirements
apt update && apt upgrade -yf
apt install pv -y
pip install -r requirements.txt

#Link and copy scripts
ln -s /opt/plex-tools/scripts/* /usr/sbin/
cp /opt/plex-tools/systemd-config/* /lib/systemd/system/

#restart deamon
systemctl daemon-reload
systemctl enable plex-tools-thread-logger.service
systemctl enable plex-tools-socket-logger.service
systemctl start plex-tools-thread-logger.service
systemctl start plex-tools-socket-logger.service

#create folder for logs
mkdir /var/log/plex-tools/

#pip uninstall websocket-client
#pip uninstall websocket
#pip install websocket-client
#pip install websocket-client
#---------------------------------------------------------
# Potential requirements.
# pip install -r requirements.txt
#---------------------------------------------------------
requests
websocket
websocket-client
xmltodict

#Import Template
Import the plex-tools.yaml template into Zabbix.


# Last Update
October 16, 2021

# Contact
Twitter: @KRelkci
Github: @nobody3400

# Special Thanks
- 
