# CMD-Befehle – Übersicht

Diese Liste enthält wichtige CMD-Befehle und administrative Windows-Befehle mit kurzer Beschreibung, logisch gruppiert für IT-Support, Diagnose und Administration.

---

## Schnellübersicht

### Benutzer, Anmeldung & Domäne

| Befehl | Bereich | Kurzbeschreibung |
|--------|--------|-----------------|
| whoami /fqdn | Benutzer / Domäne | Gibt den vollqualifizierten Benutzerprinzipalnamen aus, z. B. `benutzername@contoso.local`. |
| echo %userdomain% | Benutzer / Domäne | Zeigt die Domäne an, zu der das aktuelle Benutzerkonto gehört. |
| echo %userdomain%\%username% | Benutzer / Domäne | Zeigt den vollständigen Anmeldenamen des aktuellen Benutzers. |

---

### Computername, System & Hardware

| Befehl | Bereich | Kurzbeschreibung |
|--------|--------|-----------------|
| hostname | System | Zeigt den Namen des Computers an. |
| systeminfo | System | Zeigt detaillierte Systeminformationen wie Windows-Version, Hotfixes, RAM und BIOS-Daten an. |
| msinfo32 | System | Öffnet die grafische Systeminformationsübersicht von Windows. |
| ver | System | Zeigt die installierte Windows-Version an. |
| wmic | System | Zeigt Systeminformationen über die WMI-Schnittstelle an; veraltet, aber teils noch nützlich. |
| wmic bios get serialnumber | System / Hardware | Zeigt die Seriennummer des BIOS bzw. Geräts an. |
| driverquery | Treiber | Listet installierte Gerätetreiber und deren Status auf. |
| driverquery /v | Treiber | Zeigt detaillierte Informationen zu installierten Gerätetreibern an. |

---

### Gruppenrichtlinien, Sicherheit & Registry

| Befehl | Bereich | Kurzbeschreibung |
|--------|--------|-----------------|
| gpresult /r | Gruppenrichtlinien | Zeigt eine Zusammenfassung der angewendeten Gruppenrichtlinien für Benutzer und Computer an. |
| secpol.msc | Sicherheit | Öffnet die lokale Sicherheitsrichtlinie, z. B. für Kennwortrichtlinien, Kontosperren und Benutzerrechte. |
| reg query | Registry | Liest Werte und Schlüssel aus der Windows-Registrierung aus. |
| reg query HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion | Registry | Beispiel zum Auslesen eines Registry-Pfads unter `HKLM`. |

---

### Systemreparatur, Integrität & Datenträger

| Befehl | Bereich | Kurzbeschreibung |
|--------|--------|-----------------|
| sfc /scannow | Systemreparatur | Überprüft geschützte Systemdateien und repariert beschädigte Dateien automatisch. |
| dism /online /cleanup-image /restorehealth | Systemreparatur | Prüft und repariert das Windows-Komponentenstore-Abbild. |
| chkdsk | Datenträger | Überprüft ein Laufwerk auf Dateisystemfehler. |
| chkdsk C: /f | Datenträger | Prüft Laufwerk `C:` und repariert gefundene Fehler. |

---

### Netzwerk – Grunddiagnose

| Befehl | Bereich | Kurzbeschreibung |
|--------|--------|-----------------|
| ipconfig | Netzwerk | Zeigt die aktuelle IP-Konfiguration des Computers an. |
| ipconfig /all | Netzwerk | Zeigt detaillierte Netzwerkinformationen inklusive MAC-Adresse, DHCP und DNS an. |
| ipconfig /release | Netzwerk | Gibt die aktuelle vom DHCP vergebene IP-Adresse frei. |
| ipconfig /renew | Netzwerk | Fordert eine neue IP-Adresse vom DHCP-Server an. |
| ipconfig /flushdns | Netzwerk | Leert den lokalen DNS-Resolver-Cache. |
| ping <ziel> | Netzwerk | Prüft Erreichbarkeit und Antwortzeit eines Hosts per ICMP. |
| tracert <ziel> | Netzwerk | Zeigt die Route der Pakete zu einem Zielhost inklusive Hops an. |
| pathping <ziel> | Netzwerk | Kombiniert `ping` und `tracert` und liefert zusätzliche Statistiken zu Paketverlusten. |
| nslookup <ziel> | DNS | Fragt DNS-Server ab, um Namen in IP-Adressen aufzulösen oder umgekehrt. |
| arp | Netzwerk | Zeigt oder löscht die ARP-Cache-Tabelle. |
| arp -a | Netzwerk | Listet alle bekannten IP-/MAC-Zuordnungen im ARP-Cache auf. |
| route print | Netzwerk | Zeigt die lokale Routingtabelle und vorhandene Netzrouten an. |

---

### Netzwerk – Verbindungen, Ports & Freigaben

| Befehl | Bereich | Kurzbeschreibung |
|--------|--------|-----------------|
| netstat | Netzwerk | Zeigt aktive Netzwerkverbindungen und offene Ports an. |
| netstat -ano | Netzwerk | Zeigt alle Verbindungen inklusive PID zur Prozesszuordnung an. |
| net share | Freigaben | Zeigt freigegebene Ordner des Computers an und unterstützt deren Verwaltung. |
| net use | Freigaben | Zeigt verbundene Netzlaufwerke oder verbindet neue Netzwerkressourcen. |
| net use Z: \\Server\Freigabe | Freigaben | Verbindet das Netzlaufwerk `Z:` mit einer Freigabe. |
| net session | Freigaben | Zeigt aktive SMB-Sitzungen zu deinem Rechner an. |
| net view | Freigaben / Netzwerk | Zeigt andere Computer im Netzwerk oder Freigaben eines bestimmten Rechners an. |
| net time | Netzwerk / Zeit | Zeigt die aktuelle Uhrzeit eines entfernten Computers oder synchronisiert die Zeit. |
| net time \\server01 | Netzwerk / Zeit | Zeigt die Uhrzeit des Servers `server01` an. |

---

### Benutzer, Gruppen & Kontenverwaltung

| Befehl | Bereich | Kurzbeschreibung |
|--------|--------|-----------------|
| net user | Benutzer | Listet lokale Benutzerkonten auf oder verwaltet Benutzer. |
| net user testuser /add | Benutzer | Erstellt einen neuen lokalen Benutzer mit dem Namen `testuser`. |
| net group | Gruppen / Domäne | Verwaltet globale Domänengruppen in Active Directory. |
| net localgroup | Gruppen | Verwaltet lokale Gruppen und zeigt deren Mitglieder an. |

---

### Dienste, Prozesse & Taskverwaltung

| Befehl | Bereich | Kurzbeschreibung |
|--------|--------|-----------------|
| tasklist | Prozesse | Listet alle aktuell laufenden Prozesse auf. |
| taskkill /PID <id> /F | Prozesse | Beendet einen Prozess anhand seiner PID; `/F` erzwingt das Beenden. |
| taskmgr | Prozesse | Öffnet direkt den Windows-Task-Manager. |
| sc query | Dienste | Zeigt den Status eines Windows-Dienstes an. |
| sc query spooler | Dienste | Zeigt den Status des Druckerspooler-Dienstes an. |
| net start | Dienste | Listet laufende Dienste auf oder startet einen bestimmten Dienst. |
| net start spooler | Dienste | Startet den Druckerspooler-Dienst. |
| net stop | Dienste | Stoppt einen Windows-Dienst. |
| net stop spooler | Dienste | Stoppt den Druckerspooler-Dienst. |

---

### Remote, Sitzungen & Terminalserver

| Befehl | Bereich | Kurzbeschreibung |
|--------|--------|-----------------|
| query user | Remote / Sitzungen | Zeigt alle angemeldeten Benutzer auf dem System oder Server an. |
| qwinsta | Remote / Sitzungen | Zeigt RDP- bzw. Terminalserver-Sitzungen mit Status wie aktiv oder getrennt an. |
| logoff <ID> | Remote / Sitzungen | Rennt eine Benutzersitzung (z. B. RDP) auf einem lokalen oder entfernten System. |

---

### Windows-Verwaltung & grafische Systemtools

| Befehl | Bereich | Kurzbeschreibung |
|--------|--------|-----------------|
| control | Verwaltung | Öffnet die klassische Windows-Systemsteuerung. |
| control printers | Drucker | Öffnet direkt die Druckerverwaltung bzw. Druckerübersicht. |
| printmanagement.msc | Drucker | Öffnet die erweiterte Druckerverwaltung in Windows. |
| sysdm.cpl | System | Öffnet die Systemeigenschaften, z. B. Computername, Hardware, Erweitert, Systemschutz und Remote. |
| systempropertiesadvanced | System | Öffnet direkt den Reiter **Erweitert** in den Systemeigenschaften. |
| ncpa.cpl | Netzwerk | Öffnet die Übersicht aller Netzwerkverbindungen. |
| perfmon | Monitoring | Öffnet den Leistungsmonitor zur Analyse von Systemleistung und Ressourcen. |

---

### Herunterfahren, Neustart & Systemaktionen

| Befehl | Bereich | Kurzbeschreibung |
|--------|--------|-----------------|
| shutdown | Systemaktion | Fährt den Computer herunter, startet ihn neu oder meldet Benutzer ab. |
| shutdown /r /t 0 | Systemaktion | Startet den PC sofort neu. |
| shutdown /s /t 60 | Systemaktion | Fährt den PC in 60 Sekunden herunter. |
