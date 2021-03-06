# AngularJS & Tooling für Embedded-Geräte

## Intention

Dieses Projekt kann als Grundlage verwendet werden um eine AngularJS Single-Page-Webanwendung für den Einsatz als Benutzeroberfläche in einem Embedded-Gerät zu entwickeln.

## Einleitung

AngularJS ist ein JavaScript Framework zu Erstellung von Single-Page-Webanwendungen. Eine Single-Page-Webanwendungen ist eine Webanwendung, die nur aus einem HTML-Dokument besteht. Alle weiteren Inhalte werden dynamisch per JavaScript nachgeladen. Wird beispielsweise die Ansicht gewechselt, wird das dazugehörige HTML und CSS aus dem Anwendungscache geladen. Der WebServer muss zu diesem Zeitpunkt nur noch die benötigten Daten liefern. Initial dauert das Laden der Anwendung ein wenig länger, danach wird der Server aber entlastet.

In einem Projekt der Firma MixedMode wurde diese Technologie erfolgreich zur Entwicklung einer Benutzerschnittstelle für ein Gerät mit Embedded-System eingesetzt. Die wichtigsten Gründe dieses Framework im Kontext von Embedded-System zu verwenden sind folgende.

- Die hauptsächlich clientseitige Ausführung entlastet das ressourcenbeschränkte Gerät.
- Die Benutzeroberfläche wird vom Gerät selbst ausgeliefert und muss daher nicht zuvor installiert werden.
- Die Benutzeroberfläche kann bei einem Firmwareupdate erneuert werden. Somit wird nur ein Update-Mechanismus benötigt.
- Die Applikation bleibt im Browser geladen, dadurch können langlebige bidirektionale Kommunikationsverbindungen (WebSocket) zum Gerät aufrechterhalten werden.
- Die Applikation kann auf verschiedenen Endgräten ausgeführt werden z.B. Smartphones.

## Das Beispielprojekt

Das Beispielprojekt soll die Oberfläche eines Smart Home Managers darstellen. Am Smart Home Manager kann man verschiedene Geräte (Sensoren, Schalter, Steuereinheiten etc.) über unterschiedliche Verbindungen (USB, WLAN, Serielle Schnittstelle etc.) anschließen. Die Oberfläche soll einen Überlick über den Zustand der Smart Home Geräte geben und die Konfiguration der Interaktion zwischen den Geräten ermöglichen.

## Starten der Applikation

```
npm install -g http-server
cd SmartHomeManager
npm install
http-server app/
```

## Ausführen der Tests

1. Installation von `protractor` und `webdriver-manager`. Siehe hierzu https://www.protractortest.org/#/tutorial#setup.
2. Start der Applikation.
3. Neues Terminal: `webdriver-manager update && webdriver-manager start`
4. Neues Terminal: `protractor protractor.conf.js`
