# Wichtel-App

Eine kleine, interaktive Web-App für Wichtelrunden, inklusive:

- Kinder-Wichtel-Modus (1 Erwachsener -> 1 Kind)
- Klassischer Wichtel-Generator
- Teilnehmerverwaltung mit Sperrlisten
- Auslosung und automatische Bekanntgabe per E-Mail / WhatsApp / Link
- Geheim-PIN für die Enthüllung am Gerät
- Snowfall-Animation und festlicher Stil

## Live-Vorschau

Die App ist als statische HTML-Seite direkt nutzbar. Nach dem Upload auf GitHub Pages läuft sie im Browser ohne Backend.

## Projektstruktur

- `index.html` – komplette App-Logik und UI
- `.github/workflows/pages.yml` – Deployment auf GitHub Pages

## Lokale Nutzung

Du kannst die App direkt im Browser öffnen:

- `index.html` öffnen

Oder lokal über einen kleinen Webserver:

```bash
python -m http.server 8000
```

Danach im Browser:

- `http://localhost:8000`

## Funktionen im Überblick

### Kinder-Wichtel-Modus

- 6 Erwachsene und 6 Kinder können verwaltet werden
- Jede erwachsene Person zieht genau ein Kind
- Sperrliste für Kinder, die nicht gezogen werden dürfen
- PIN-basierte Enthüllung

### Klassischer Modus

- beliebige Personenliste
- zufällige Zuordnung ohne direkte Wiederholung
- E-Mail / Link / PIN-Optionen

### Bekanntgabe

- E-Mail-Links für jeden Teilnehmer
- WhatsApp-Links
- EmailJS-Integration (optional)
- On-Site PIN-Verfahren für Feierlichkeiten vor Ort

## EmailJS konfigurieren

Falls du den automatischen E-Mail-Versand nutzen willst:

1. EmailJS-Konto erstellen
2. Public Key, Service ID und Template ID eintragen
3. Template-Variablen verwenden:
   - `{{to_name}}`
   - `{{to_email}}`
   - `{{reveal_link}}`

## GitHub Pages

Das Repository enthält bereits einen Workflow für GitHub Pages. Folge diesen Schritten:

1. In GitHub auf das Repository gehen
2. `Settings` → `Pages`
3. als Source `GitHub Actions` auswählen
4. deployment erfolgt automatisch bei Push auf `main`

## Hinweise

- Die App speichert Daten im `localStorage` des Browsers.
- Die Auslosung bleibt nur lokal im Browser gespeichert, bis sie exportiert oder neu gestartet wird.
- Für echte E-Mail-Weiterleitungen ohne Mail-Client ist EmailJS nötig.

## Lizenz

Dieses Projekt ist für den privaten / internen Gebrauch gedacht. Wenn du es für einen eigenen Anlass verwenden willst, kannst du den Code frei anpassen.
