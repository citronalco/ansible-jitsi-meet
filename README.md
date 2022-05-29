# Jitsi-Meet

Jitsi-Meet-Server auf Debian 11 für Bingo.

Es können mehrere Domainnamen für den Server verwendet werden. Für jede Domain kann die Jitsi-Meet-GUI einzeln angepasst werden.
Standardmäßig kann jeder Meetings starten. Es kann aber auch eingestellt werden, dass nur angelegte Benutzer Meetings starten und/oder betreten können.

Nicht installiert wird die Videoaufnahmekomponente Jibri.

### Installation
1. Servername, IPv4- und IPv6-Adresse in `hosts` eintragen
2. Einstellungen in host_vars/SERVERNAME vornehmen
3. Ausrollen mit `ansible-playbook -i hosts jitsi-meet.yml`

### Anpassungen
Mit `/etc/jitsi/meet/meet.bingo-ev.de/DOMAINNAME/nginx-override.conf` können eigene Logos, Icons und eine eigene interface_config.js zum Anpassen der Jitsi-Meet-Weboberfläche eingebunden werden.

Mit `/etc/jitsi/meet/meet.bingo-ev.de/DOMAINNAME/config.js` können Standardeinstellungen für die Meetings festgelegt werden (z.B. ob am Anfang alle Mikros stumm sind und alle Kameras aus).

