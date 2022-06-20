# Chatbot_Raumbuchung

![Screenshot](https://livinglab-essigfabrik.eu/wp-content/uploads/2022/02/EFBO-1_Screenshot.png)

## About

Zur Realisierung eines Chatbot-gestützten Buchungssystem wurde sowohl ein Frontend,
das mit den Nutzer:innen kommuniziert, sowie ein Backend entwickelt, welches
im Hintergrund die Anfragen der Nutzer:innen verarbeitet und entsprechend
reagieren kann. Als Frontend dient eine webbasierte, über jeden Browser erreichbare,
geografische Karte mit einem aktivierbaren Feld zur Kommunikation mit der
Chatbot-Softwareinfrastruktur. In diesem Bereich können Nutzer:innen ihr Anliegen
dem Chatbot per Texteingabe mitteilen und so ein Dialog-Gespräch beginnen. Die
Karte kann interaktiv bewegt und herein- und herausgezoomt werden. Die dreidimensionalen
Kartenoberfläche wurde mit der Javascript-Bibliothek iTowns realisiert,
die ihrerseits auf der three.js-Bibliothek basiert. Die iTowns-Bibliothek ermöglicht es
Gebäudemodelle im Browser darzustellen, sowie Kartendaten per Web Mab Services
(WMS) oder Web Feature Services (WFS) von anderen Datenanbietern wie z.B
OpenStreetMap abzurufen. Die 3D-Gebäudedaten sind im City-GML-Format frei auf
dem Datenportal open.NRW der Landesregierung NRW verfügbar. Diese mussten
vor der Weiterverarbeitung in iTowns noch in das B3DM-Format konvertiert werden.
Das Backend setzt sich zum einen aus dem Chatbot selbst, zur Kommunikation mit
den Nutzer:innen, sowie einer Datenbankinfrastruktur, zur Hinterlegung von Informationen
über Räume, Fotos etc., zusammen. Für den Chatbot kommt die freie Software
von Botpress zum Einsatz. Dieses KI-basierte Framework ermöglicht es, sowohl
regelbasiert auf Aktionen von Nutzer:innen in Echtzeit zu reagieren und auch
das Antwortverhalten durch fortwährende Dialoge weiter zu trainieren.

Zum jetzigen Zeitpunkt wurde der Chatbot so eingerichtet, dass er auf Anfragen
nach dem Angebot des Quartierszentrums reagiert sowie auch als ein räumliches
Buchungssystem verwendet werden kann. Maßnahmen wie Lärmschutz, Sicherheit
etc., die aufgrund der Art einer Veranstaltung getroffen werden müssen, konnten im
Rahmen der Projektlaufzeit noch nicht in den Katalog des Dialogverhaltens aufgenommen
werden, sind aber zukünftig vorgesehen. Standardmäßig werden für die
Sprachmodelle, sowie für die Umwandlung von umgangssprachlichen Ausdrücken
wie ‘übermorgen’, die der Chatbot nicht direkt versteht, externe Server verwendet.
Da diese ggf. außerhalb der EU stehen und damit evtl. datenschutzrechtlich bedenklich
sein können, wurden die entsprechenden Services auf dem eigenen Server des
LivingLabs selbst aufgesetzt. Als Datenbankinfrastruktur kamen die bereits bestehenden
Geodaten-Services GeoServer, angebunden an eine PostGIS-Datenbank
zum Einsatz. Da während der Projektlaufzeit noch keine Informationen über die
zukünftig vorhandenen Räume für das geplante Quartier Deutzer Hafen existierten,
wurden eigene, behelfsmäßige Testdaten generiert und in die Datenbank eingepflegt.

## Demo

[Hier zum Live Demo]([https://pages.github.com/](https://ar.livinglab-essigfabrik.online/itowns_chatbot/index.html))

## Diagram

![Diagram](https://livinglab-essigfabrik.ids-research.de/wp-content/uploads/2022/06/Flowcharts-fuer-Publikation-1.1.-KI-gestuetzter-Chatbot-zur-Unterstuetzung-eines-digitalen-Raumbuchungsvorgangs.jpg)
