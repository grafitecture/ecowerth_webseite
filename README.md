# ecowerth Website-Prototyp

Klickbarer Prototyp der neuen Website der ecowerth GmbH, gestaltet von Grafitecture. Ausgeliefert über Vercel; jeder Push auf `main` geht automatisch live.

## Inhalt

| Datei | Zweck |
|---|---|
| `public/index.html` | Der Prototyp hinter einer Login-Seite. Der Seiteninhalt ist verschlüsselt (AES-256-GCM, Schlüssel per PBKDF2-SHA-256) und wird erst im Browser mit dem Passwort entschlüsselt. |
| `public/impressum.html`, `public/datenschutz.html` | Impressum und Datenschutzerklärung, ohne Passwort erreichbar unter `/impressum` und `/datenschutz` (Deutsch/Englisch). Inhalt identisch mit den Rechtsseiten im Prototyp. |
| `public/robots.txt`, `vercel.json` | Keine Indexierung durch Suchmaschinen, statische Auslieferung aus `public/`, Adressen ohne `.html` (`/impressum.html` leitet auf `/impressum` weiter), Function Region Frankfurt (`fra1`). |

Das Passwort steht bewusst nirgends in diesem Repository. Es wird separat weitergegeben.

## Datenschutz

- Keine Anfragen an fremde Server: Schriften (Archivo, IBM Plex, SIL Open Font License) sind eingebettet, kein Google Fonts, keine Karten, Videos oder Plugins.
- Keine Cookies, kein Tracking. Vercel Web Analytics und Speed Insights sind nicht eingebunden und dürfen es auch nicht werden, ohne die Datenschutzerklärung anzupassen.
- Hosting bei Vercel Inc. (USA). Die Datenschutzerklärung nennt den Anbieter, die Datenübermittlung (EU-U.S. Data Privacy Framework, Standardvertragsklauseln) und den Auftragsverarbeitungsvertrag (Vercel DPA, gilt für Pro- und Enterprise-Teams).

## Änderungen

Dieses Repository ist öffentlich. Deshalb liegen die lesbare Quelle, die Vorlagen und die Build-Skripte nicht hier, sondern im Claude-Projekt „ECOWERTH WEBSEITE“. Nach einer Änderung werden `public/index.html` (`protect.mjs … --standalone`) und die beiden Rechtsseiten (`legal.mjs`) dort neu gebaut und hierher gepusht.

Abmelden im Browser: `#abmelden` an die Adresse hängen.

Ein geteiltes Passwort ist ein Sichtschutz, keine Zugriffskontrolle.

## Vor dem Livegang auf ecowerth.de / ecowerth.com

1. Offene Angaben im Impressum und in der Datenschutzerklärung ergänzen (rot markierte Platzhalter: Handelsregister, USt-IdNr., ggf. Datenschutzbeauftragter).
2. Domains im Vercel-Projekt hinzufügen und die DNS-Einträge beim Domain-Anbieter setzen.
3. Login entfernen, `robots.txt` und den Header `X-Robots-Tag` freigeben.
4. Kontaktformular erst mit Formulardienst und ergänzter Datenschutzerklärung in Betrieb nehmen.
