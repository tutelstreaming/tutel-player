# tutel-player
Minimalistic WebRTC streaming webpage utilizing OvenMediaPlayer

We are new to GitHub and Open Source licenses. If we have done something incorrectly, please let us know. It is not our intention to violate any licenses.

For reference, please see https://airensoft.gitbook.io/ovenmediaengine/ and https://airensoft.gitbook.io/ovenplayer/ for additional configurations

This is a configuration guide on how to setup your own instance of OvenMediaEngine and OvenMediaPlayer.  You can then utilize our custom made HTML/Javascript solution that interacts with OME and OMPlayer to provide a minimalistic and easy to use 4-screen streaming solution.

Please reference this github post if using or modifying our solution.  Thank You.

Our Webpage: https://tutelstreaming.com

Our Discord: https://discord.gg/z7G7vf5kQX

--------------------

TutelPlayer.html
* HTML/Javascript that parses a GoogleSheets containing stream keys. Can be used as a executed web-app, or hosted as a server such as Apache.

Server.xml
* Configuration file that needs to be placed in /opt/ovenmediaengine/bin/origin_conf/ directory for the OvemMediaEngine container.

--------------------

OME Docker Run Command

`docker run -d --restart unless-stopped -p 1935:1935/tcp -p 3334:3334/tcp -p 3334:3334/udp  -p 3478:3478/tcp -p 3478:3478/udp -p 10000:10000/udp -p 10001:10001/udp -p 10002:10002/udp -p 10003:10003/udp -p 10004:10004/udp -p 10005:10005/udp -p 10006:10006/udp -v /path/to/Server.xml:/opt/ovenmediaengine/bin/origin_conf/Server.xml airensoft/ovenmediaengine:latest`

Example Apache Docker Run Command (rename TutelPlayer.html to index.html and place in a folder named htdocs)

`docker run -d --restart unless-stopped -p 80:80 -p 443:443 -v /path/to/htdocs/:/app httpd:latest`

--------------------

OBS Setup
Please follow the guide "OBS-Setup.md" above.
