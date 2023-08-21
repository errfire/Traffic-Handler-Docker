# Traffic Handler Docker

## BETA Version. Bitte aktuell nur zu Testzwecken nutzen. Nicht Produktiv schalten.

## Informationen
Der Traffic Handler von ERR-Fire verkörpert ein innovatives System, das dazu konzipiert ist, Verkehrsbeeinträchtigungen, langfristige Baustellen und vergleichbare Hindernisse zu erfassen und transparent darzustellen. Durch die umfassende Dokumentation dieser Faktoren ermöglicht das System eine optimierte Routenplanung bereits im Vorfeld der Anfahrt zur Einsatzstelle.
Ein essentieller Aspekt dieses Systems ist die Benutzerverwaltung, welche eine präzise Steuerung der Zugriffsrechte ermöglicht. Diese differenzierten Berechtigungen erlauben es, einzelnen Nutzern spezifische Schreib- oder ausschließlich Leserechte zuzuweisen. Hierdurch wird die Integrität der hinterlegten Daten gewährleistet und ein Höchstmaß an Sicherheit erreicht.


Die Daten werden zentral in einer lokalen Datenbank gespeichert, wodurch Ihnen uneingeschränkte Kontrolle über Ihre Daten gewährt wird.


### Environment

Die Ausführung dieses Containers erfordert eine "echte" Linux-Umgebung (entweder physisch oder virtuell, siehe unten).

:star: Wir haben seit vielen Jahren gute Erfahrungen mit  [DeinServerHost](https://deinserverhost.de/store/aff.php?aff=3919) und ihre Root- und V-Server-Angebote gemacht.

Sie Suchen einen vServer oder Root-Server, dann bestellen Sie über den u.g. Link und unterstützen Sie uns. Vielen Dank.

[![DeinServerHost](https://deinserverhost.de/tca/600x150_transparent.png)](https://deinserverhost.de/store/aff.php?aff=3919)

Wir empfehlen einen Ubuntu oder CentOS Distribution.

Bitte nutzen Sie folgende Versionen:

- Docker version 20.10.23
- docker-compose version 1.29.2


Docker Desktop für Windows (Windows Linux Subsystem (WSL2)) wird ebenfalls unterstützt.

### Upgrades

Sobald es eine neue Version gibt, werden Sie auf der Hauptseite des Traffic Handlers darüber informiert mit einem Pop-Up.
Sollten Sie ein Update durchführen wollen, gehen Sie wie folgt vor:

Bitte wechseln Sie in den traffichandler-docker Ordner und führen Sie dann folgendes aus:

Downloaden Sie sich unter GitHub oder auf unserer Projektseite die neuste Version herunter.
Führen Sie folgende Kommandos aus:

`docker-compose down`

Platzieren Sie die neue docker-compose.yml.

Führen Sie folgende Kommandos aus:

`docker-compose up -d`



## 🔐 SSL

Grundsätzlich wird der Container mit dem Port 443 und 80 exposed. Darüber hinaus ist ein Self Sign Zertifikat integriert. 
Wahlweise kann auch der Port 80 verwendet werden. Hierfür passen Sie die settings.cfg Datei an.

Für den Zugriff auf den Traffic Handler nach außen, empfehlen wir das Vorschalten eines reverse Proxy. (NGINX)

Wir planen in einer der nächsten Versionen, das ganze einzubinden. Aktuell ist aber die Community gefragt.
Eure Konfigurationen nehmen wir gerne unter info@err-fire.de entgegen. :-)

## Erster Start
- Installiere Docker und Docker Compose in der letzten Version
- Platziere den Ordner `traffichandler-docker` in dein `/opt` Verzeichniss
- Führe die `docker-compose.yml` innerhalb des Ordners `traffichandler-docker`, wie folgt aus `docker-compose up -d`
- Öffnen Sie den Webbrowers und rufen Sie folgendes aus: `https://FQDN`


## Hinweise

`Deine Stadt` lässt sich über die `settings.cfg` innerhalb von `data\conf` ändern.

`ALERTKEY` wird bei jedem neuen deploy, neu generiert.

Das erstellen von Koordinaten hat sich hierüber bewehrt (https://www.gpskoordinaten.de/)

## 📷 Screenshots
![alt text](https://github.com/muffti-112/Traffic-Handler-Docker/blob/main/img/login.png)

![alt text](https://github.com/muffti-112/Traffic-Handler-Docker/blob/main/img/mainview.png)

![alt text](https://github.com/muffti-112/Traffic-Handler-Docker/blob/main/img/entry.png)

![alt text](https://github.com/muffti-112/Traffic-Handler-Docker/blob/main/img/delte.png)

![alt text](https://github.com/muffti-112/Traffic-Handler-Docker/blob/main/img/usermanagment.png)

## Wir sagen Danke

Diese Anwendung ist ein Freizeit Projekt, um ein Problem zu lösen und einfach mal tiefer in die Entwicklung einzusteigen.
Jetzt ist das Feedback der Community gefragt. Ihr habt Bugs gefunden oder habt eine coole Idee zur Optimierung? Ihr habt ein Feature was ihr unbedingt in der Anwendung wieder finden wollt? 
Dann teilt mir das gerne im GitHub Issuer-Tracker mit oder via Mail an info@err-fire.de

Ihr wollt Danke sagen und das Projekt weiterleben lassen? Gerne hier:

<a href="https://www.buymeacoffee.com/errfiretraffichandler" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>
