# Jitsi-Meet

Set up a Jitsi Meet server on Debian.

Supports multiple domain names, with GUI customizations for each domain.
By default everyone can start a meeting, but there's an option to only allow authenticated users to create and/or join meetings.

Jibri (to record meetings) is included.

### Installation
1. Enter server name, IPv4 and IPv6 addresse in `hosts`
2. Apply your settings in `host_vars/SERVERNAME`
3. Start installation with `ansible-playbook -i hosts jitsi-meet.yml`

### GUI customizations
You may override the default settings for each domain separately.

Do your customizations in the following files in `/etc/jitsi/meet/DOMAINNAME/`:
- config.local.js
- branding/branding.json
- interface_config.local.js
- nginx-override.conf

The directory `/etc/jitsi/meet/DOMAINNAME/branding/` is accessible via https://DOMAINNAME/branding/.

Customizations are kept when running this playbook again and when updating Jitsi Meet.

__Customizations for für meet.bingo-ev.de are here: https://git.bingo-ev.de/infrastructure/jitsi-meet/jitsi-meet-config__
