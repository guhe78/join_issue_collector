# Join Issue Collector

Join ist ein webbasiertes Aufgabenmanagement-Projekt, das im Rahmen eines Gruppenprojekts entstanden ist. Diese Anwendung bietet eine gemeinsame Oberflaeche, um Aufgaben und Kontakte zu verwalten. Die Anwedung wurde zu Join - Issue Collector erweitert. Es können Task per Email hinzugefügt werden. Das hinzufügen wird mittels n8n und einer KI realisiert.

## Funktionen

- Benutzerregistrierung und Anmeldung sowie Gastzugang
- Aufgaben erstellen, bearbeiten und nach Status auf dem Board organisieren
- Kontakte verwalten und Aufgaben Personen zuweisen
- Zusammenfassung der Aufgaben auf der Uebersichtsseite
- Hinzufügen von Aufgaben per Email mittels KI

## Technologie

- HTML
- CSS
- JavaScript
- Supabase als vorgesehene Datenbank fuer die E-Mail-Task-Erweiterung
- n8n und KI fuer die automatisierte Verarbeitung von E-Mail-Anfragen

## Geplante Erweiterung: Aufgaben per E-Mail

Nutzer sollen Aufgaben direkt per E-Mail anlegen koennen. Eine eingehende E-Mail wird automatisiert mit n8n und KI verarbeitet. Die erkannten Aufgabeninformationen werden anschliessend als Task in Supabase gespeichert und stehen in der Anwendung zur Verfuegung.

Pro Nutzer sind maximal 10 E-Mail-Anfragen pro Tag erlaubt. Weitere Anfragen werden abgelehnt, sobald dieses Tageslimit erreicht ist.

Der Ablauf ist vorgesehen als:

1. Nutzer sendet eine E-Mail mit einem Aufgabenwunsch.
2. n8n nimmt die Anfrage entgegen und startet den Automationsablauf.
3. Eine KI extrahiert die Aufgabeninformationen aus dem E-Mail-Text.
4. Die Anfrage wird geprueft, insbesondere auf das Tageslimit von 10 Anfragen.
5. Bei gueltiger Anfrage wird die Aufgabe in Supabase gespeichert.

Die E-Mail-Automation ist eine Erweiterung des Projekts und muss eingerichtet werden. Dazu gehoeren der n8n-Workflow, die KI-Anbindung, die Supabase-Verbindung sowie eine zuverlaessige Umsetzung des Tageslimits.

## Projektstruktur

- `index.html`: Anmeldung und Einstieg in die Anwendung
- `pages/`: Seiten fuer Board, Aufgaben, Kontakte, Uebersicht und weitere Inhalte
- `scripts/`: Anwendungslogik, UI, Services und Hilfsfunktionen
- `styles/` und `style.css`: Layout und Gestaltung
- `assets/`: Bilder, Schriften und Favicons

## Starten

Das Frontend besteht aus statischen HTML-, CSS- und JavaScript-Dateien. Oeffne das Projekt ueber einen lokalen Webserver, damit Seiten und Skripte korrekt geladen werden. Fuer die laufende Anwendung muessen ausserdem die benoetigten Backend-Konfigurationen eingerichtet sein.
