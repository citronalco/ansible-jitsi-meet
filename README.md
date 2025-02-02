# Jitsi-Meet

Set up a Jitsi Meet server on Debian.

Supports multiple domain names, with GUI customizations for each domain.
By default everyone can start a meeting, but there are options to only allow authenticated users to create and/or join meetings 

Jibri (to record meetins) does not get installed.

### Installation
1. Enter server name, IPv4 and IPv6 addresse in `hosts`
2. Apply your settings in `host_vars/SERVERNAME`
3. Start installation with `ansible-playbook -i hosts jitsi-meet.yml`

### GUI customizations
In `/etc/jitsi/meet/DOMAINNAME/nginx-override.conf` you can include your own logos, icons and your own interface_config.js to customize the Jitsi Meet web GUI.

In `/etc/jitsi/meet/DOMAINNAME/config-custom.js` you can customize settings for the meetings (i.e. if meetings start with all microphones muted and webcams disabled).

Put your logos and icons into the directory `/etc/jitsi/meet/DOMAINNAME/branding/`
This directory is accessible via https://DOMAINNAME/branding/

Customizations are kept when running this playbook again and when updating Jitsi Meet.

__Customizations for für meet.bingo-ev.de are here: https://git.bingo-ev.de/infrastructure/jitsi-meet/jitsi-meet-config__
