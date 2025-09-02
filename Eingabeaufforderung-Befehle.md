# **Eingabeaufforderung**

##### 

##### **whoami** /**fqdn** -> gibt den vollqualifizierten Benutzerprinzipalnamen, z. B. benutzername@contoso.local



##### **echo %userdomain%** -> *zeigt die Domäne an, zu der dein aktuelles Benutzerkonto gehört*



##### **echo %userdomain%\\%username%** -> *zeigt den vollständigen Anmeldenamen*



##### <b>hostname</b> -> *zeigt einfach den Namen des Computers an*



##### **net share** -> *zeigt alle freigegebenen Ordner (Shares) des Computers an und ermöglicht deren Verwaltung*



##### **gpresult /r** -> *zeigt eine Zusammenfassung der angewendeten Gruppenrichtlinien für den aktuellen Benutzer und Computer an*



##### **sfc /scannow** -> *überprüft alle geschützten Systemdateien und repariert beschädigte Dateien automatisch*



##### **dism /online /cleanup-image /restorehealth** -> *überprüft und repariert das Windows-Komponentenstore-Abbild (WinSxS), wenn Systemdateien beschädigt sind*



##### **tracert <ziel>** -> *zeigt die Route (Hops) an, die Pakete zu einem Zielhost im Netzwerk/Internet nehmen, inklusive Laufzeit je Hop*



##### **pathping <ziel>** -> *kombiniert die Funktionen von ping und tracert, liefert zusätzlich Statistiken zu Paketverlusten entlang des Pfads*



##### **ping <ziel>** -> *sendet ICMP-Echoanforderungen, um die Erreichbarkeit und Antwortzeit eines Hosts zu prüfen*



##### **ipconfig** -> *zeigt die aktuelle IP-Konfiguration des Computers an (IP-Adresse, Subnetz, Gateway, DNS-Server)*



##### **ipconfig /all** -> *detaillierte Anzeige der IP-Konfiguration inkl. MAC-Adressen und DHCP-Informationen*



##### **ipconfig /release** -> *gibt die aktuelle IP-Adresse des DHCP-Clients frei*



##### **ipconfig /renew** -> *fordert eine neue IP-Adresse vom DHCP-Server an*



##### **nslookup <ziel>** -> *fragt DNS-Server ab, um Hostnamen in IP-Adressen aufzulösen und umgekehrt*



##### **systeminfo** -> *zeigt detaillierte Systeminformationen wie Betriebssystemversion, Hotfixes, RAM, BIOS-Daten an*



##### **tasklist** -> *listet alle aktuell laufenden Prozesse auf, ähnlich dem Task-Manager*



##### **taskkill /PID <id> /F** -> *beendet einen Prozess über dessen PID (Prozess-ID), /F erzwingt das Beenden*



##### **control** -> *öffnet die klassische Systemsteuerung*



##### **control printers** -> *öffnet direkt die Druckerverwaltung*



##### **sysdm.cpl** -> *öffnet die Systemeigenschaften (Computername, Hardware, Erweitert, Systemschutz, Remote)*


