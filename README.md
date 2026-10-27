# ecowerth Website-Prototyp

Klickbarer Prototyp der neuen Website der ecowerth GmbH, gestaltet von Grafitecture. Ausgeliefert über Vercel; jeder Push auf `main` geht automatisch live.

## Inhalt

| Datei | Zweck |
|---|---|
| `public/index.html` | Der Prototyp hinter einer Login-Seite. Der Seiteninhalt ist verschlüsselt (AES-256-GCM, Schlüssel per PBKDF2-SHA-256) und wird erst im Browser mit dem Passwort entschlüsselt. |
| `public/robots.txt`, `vercel.json` | Keine Indexierung durch Suchmaschinen, statische Auslieferung aus `public/`. |

Das Passwort steht bewusst nirgends in diesem Repository. Es wird separat weitergegeben.

## Änderungen

Dieses Repository ist öffentlich. Deshalb liegen die lesbare Quelle, die Login-Vorlage und das Build-Skript nicht hier, sondern im Claude-Projekt „ECOWERTH WEBSEITE“. Nach einer Änderung wird `public/index.html` dort neu gebaut und hierher gepusht.

Abmelden im Browser: `#abmelden` an die Adresse hängen.

Ein geteiltes Passwort ist ein Sichtschutz, keine Zugriffskontrolle.
