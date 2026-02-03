# **Eingabeaufforderung**

##### 

##### **whoami** /**fqdn**  --> `gibt den vollqualifizierten Benutzerprinzipalnamen z. B. benutzername@contoso.local`



##### **echo %userdomain%** --> `zeigt die Domäne an, zu der dein aktuelles Benutzerkonto gehört`



##### **echo %userdomain%\\%username%** --> `zeigt den vollständigen Anmeldenamen`



##### <b>hostname</b> --> `zeigt einfach den Namen des Computers an`



##### **net share** --> `zeigt alle freigegebenen Ordner (Shares) des Computers an und ermöglicht deren Verwaltung`



##### **gpresult /r** --> `zeigt eine Zusammenfassung der angewendeten Gruppenrichtlinien für den aktuellen Benutzer und Computer an`



##### **sfc /scannow** --> `überprüft alle geschützten Systemdateien und repariert beschädigte Dateien automatisch`



##### **dism /online /cleanup-image /restorehealth** --> `überprüft und repariert das Windows-Komponentenstore-Abbild (WinSxS), wenn Systemdateien beschädigt sind`



##### **tracert <ziel>** --> `die Route (Hops) an, die Pakete zu einem Zielhost im Netzwerk/Internet nehmen, inklusive Laufzeit je Hop`



##### **pathping <ziel>** --> `kombiniert die Funktionen von ping und tracert, liefert zusätzlich Statistiken zu Paketverlusten entlang des Pfads`



##### **ping <ziel>** --> `sendet ICMP-Echoanforderungen, um die Erreichbarkeit und Antwortzeit eines Hosts zu prüfen`



##### **ipconfig** --> `zeigt die aktuelle IP-Konfiguration des Computers an (IP-Adresse, Subnetz, Gateway, DNS-Server`



##### **ipconfig /all** --> `detaillierte Anzeige der IP-Konfiguration inkl. MAC-Adressen und DHCP-Informationen`



##### **ipconfig /release** --> `gibt die aktuelle IP-Adresse des DHCP-Clients frei`



##### **ipconfig /renew** --> `fordert eine neue IP-Adresse vom DHCP-Server an`



##### **nslookup <ziel>** --> `fragt DNS-Server ab, um Hostnamen in IP-Adressen aufzulösen und umgekehrt`



##### **systeminfo** --> `zeigt detaillierte Systeminformationen wie Betriebssystemversion, Hotfixes, RAM, BIOS-Daten an`



##### **tasklist** --> `listet alle aktuell laufenden Prozesse auf, ähnlich dem Task-Manager`



##### **taskkill /PID <id> /F** --> `beendet einen Prozess über dessen PID (Prozess-ID), /F erzwingt das Beenden`



##### **control** --> `öffnet die klassische Systemsteuerung`



##### **control printers** --> `öffnet direkt die Druckerverwaltung`



##### **sysdm.cpl** --> `öffnet die Systemeigenschaften (Computername, Hardware, Erweitert, Systemschutz, Remote`


##### **net user** --> `listet alle lokalen Benutzerkonten auf`
##### **net user testuser /add** --> `erstellt einen neuen Benutzer namens testuser`

##### **net group** --> `Verwaltet Domänen-(globale) Gruppen in Active Directory. Für lokale Gruppen verwende stattdessen net localgroup.`

##### **net localgroup** --> `Verwaltet lokale Gruppen und zeigt deren Mitglieder an`

##### **netstat** --> `Zeigt aktive Netzwerkverbindungen und offene Ports an`
##### **netstat -ano** → `zeigt alle Verbindungen mit PID (hilfreich zur Zuordnung zu Prozessen`

##### **arp** --> `Zeigt oder löscht die ARP-Cache-Tabelle, die IP-Adressen mit MAC-Adressen verknüpft.`
##### **arp -a** --> `listet alle bekannten IP/MAC-Zuordnungen auf`

##### **net use** --> `Zeigt verbundene Netzlaufwerke oder verbindet neue.`
##### Beispiel:
##### **net use** --> `listet alle aktiven Netzverbindungen`
##### **net use Z: \\Server\Freigabe** --> `verbindet Netzlaufwerk Z: mit einer Freigabe`

##### **net start** --> `Listet alle laufenden Windows-Dienste auf oder startet einen bestimmten Dienst.`
##### Beispiel:
##### **net start** --> `zeigt alle laufenden Dienste`
##### **net start spooler** --> `startet den Druckerspooler`

##### **net stop** --> `Stoppt einen Windows-Dienst.`
##### Beispiel:
##### **net stop spooler** --> `beendet den Druckerspooler-Dienst`

##### **chkdsk** --> `Überprüft ein Laufwerk auf Dateisystemfehler und repariert sie.`
##### Beispiel:
##### **chkdsk C: /f** --> `überprüft Laufwerk C und repariert gefundene Fehler`

##### **wmic** --> `Zeigt Systeminformationen über eine WMI-Schnittstelle an (veraltet, aber noch nützlich).`
##### Beispiel:
##### **wmic bios get serialnumber** --> *zeigt die Seriennummer des BIOS an*

##### **shutdown** --> `Fährt den Computer herunter, startet ihn neu oder meldet Benutzer ab.`
##### Beispiel:
##### **shutdown /r /t 0** --> `startet den PC sofort neu`
##### **shutdown /s /t 60** --> `fährt den PC in 60 Sekunden herunter`

##### **driverquery** --> `Listet alle installierten Gerätetreiber und deren Status auf.`
##### Beispiel:
##### **driverquery /v** --> `detaillierte Treiberinformationen`

##### **sc query** --> `Zeigt den Status eines Windows-Dienstes an.`
##### Beispiel:
##### **sc query spooler** --> `zeigt den Status des Druckerspooler-Dienstes`

##### **net time** --> `Zeigt die aktuelle Uhrzeit eines entfernten Computers oder synchronisiert die Zeit.`
##### Beispiel: 
##### **net time \\server01** --> `zeigt die Zeit auf dem Server server01`

##### **systempropertiesadvanced** --> `Öffnet direkt den Reiter Erweitert in den Systemeigenschaften (Alternative zu sysdm.cpl).`

##### **ncpa.cpl** --> `Öffnet die Übersicht aller Netzwerkverbindungen im Explorer. (Steht zwar in deiner Beschreibung, aber ohne Erklärung.)`

##### **msinfo32** --> `Startet die grafische Systeminformationsübersicht (ähnlich systeminfo, aber GUI-basiert).`

##### **taskmgr** --> `Öffnet direkt den Task-Manager.`

##### **perfmon** --> `Öffnet den Leistungsmonitor, um Systemleistung und Ressourcen zu analysieren.`

##### **reg query** --> `Zeigt Werte aus der Windows-Registrierung an.`
##### Beispiel:
##### **reg query HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion**

##### **net session** --> `Zeigt aktive SMB-Sitzungen (freigegebene Verbindungen) zu deinem Rechner.`

##### **net view** --> `Zeigt andere Computer im Netzwerk oder Freigaben eines bestimmten Rechners.`

##### **query user** --> `Zeigt alle angemeldeten Benutzer auf dem Server (du siehst, ob noch jemand drin ist).`

##### **qwinsta** --> `Zeigt RDP/Terminalserver-Sitzungen (aktiv/getrennt). Hilft, „vergessene“ Sitzungen zu finden.`

##### **route print** --> `Zeigt, ob es eine Route zum Netz 192.168.2.0/24 gibt und über welches Gateway geroutet wird.`

##### **secpol.msc** --> `Dort stellt man Sicherheitsregeln für den lokalen PC ein (z. B. Passwort-Regeln, Kontosperren, Benutzerrechte, Audit/Protokollierung).`





















