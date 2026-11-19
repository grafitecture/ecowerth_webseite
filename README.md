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
- Hosting bei Vercel Inc. (USA). Die Datenschutzerklärung nennt den Anbieter, die Datenübermittlung (EU-U.S. Data Privacy Framework, Standardvertragsklauseln) und den Auftragsverarbeitungsvertrag (Vercel DPA). Den DPA gibt es nur für Pro- und Enterprise-Teams; das Team läuft derzeit im Hobby-Tarif, der Satz ist deshalb als Platzhalter markiert.

## Grafitecture-Feld

Ganz unten in Impressum und Datenschutz steht das Grafitecture-Feld (Lime-Fläche mit Logo, „Marken mit KI.“, Link auf https://www.grafitecture.de/ in neuem Fenster), auf Deutsch und Englisch: auf `/impressum` und `/datenschutz` und in den Rechtsseiten des Prototyps. Quelle ist das Kit `kit/grafitecture-credit/` aus `grafitecture/lannee_webseite` (Version 1.2); Markup aus `grafitectureCredit(sprache)`, das CSS des Kits steht unverändert am Ende des Stylesheets. Beides setzen die Build-Skripte im Claude-Projekt ein.

**Ausnahme von den Farbregeln:** Farben und Größe des Feldes (Fläche #dafd55, Schrift und Logo #435960, Linie Weiß, höchstens 403 px breit) gehören Grafitecture, nicht ecowerth. Sie bleiben so, auch wenn die Website sonst nur die ECOWERTH-Farben verwendet. Am Feld nichts anpassen; Änderungen nur im Kit.

## Logovarianten (entfernt am 14.11.2026)

Die Präsentation der Logovarianten nach dem Footer ist seit 14.11.2026 gelöscht (Auftrag Martin); `/#/logovarianten` führt zur Startseite.

## ECOLOGICON-Unterseiten, ECOACADEMY und ECOVENTURES (14.11.2026)

- **ECOLOGICON** hat eine eigene Unternavigation (Übersicht · Referenzen · Portfolio · Projekte · News · Über uns · Kontakt) und Unterseiten: Portfolio mit zehn Leistungsfeldern, Pflichtenmatrix und Zielgruppen; acht Referenzen (Fallbeispiele); Projekte mit Regionsfilter und sieben Projektseiten (BattPro in Vorbereitung); News mit Kategoriefilter (zwei Beiträge als Detailseite, die übrigen öffnen bis zur Übernahme den Beitrag auf ecologicon.com); Über uns mit Unternehmen, Vision & Mission, Netzwerk & Kooperationen, Jobs, Expertenregistrierung und Kontakt.
- **ECOACADEMY** (Wissen & Weiterbildung, Violett #6D41A9) und **ECOVENTURES** (Green Start-ups & Beteiligungen, Orange PANTONE 151 C #FF8200, Text #A25500) sind zwei untergeordnete Themengruppen mit eigenen Seiten und je einem Balken auf der Startseite.
- Adressen nach dem Login: `/#/ecologicon/referenzen`, `/#/ecologicon/projekte`, `/#/ecologicon/news`, `/#/ecologicon/ueber-uns`, `/#/ecoacademy`, `/#/ecoventures`.

## Logos final, Navigation, ohne Kreisanimation (14.11.2026)

- Alle Logos stammen seit 14.11.2026 (zweite Lieferung) aus `LOGO_ECOWERTH_LOGO_FINAL1` (Illustrator, CMYK, ECOVENTURES in PANTONE 151 C, Schrift in Pfaden) und liegen als SVG in den Markenfarben vor: ECOWERTH (im Footer weiß), ECOLOGICON, ECORELOOP, ECOINVEST, ECOACADEMY, ECOVENTURES, jeweils mit Unterzeile. Sie stehen im Kopf, im Footer, auf der Login-Seite, in Impressum und Datenschutz und überall, wo bisher Markenlogos standen. Unter 1280 px ist das Kopflogo etwas kleiner.
- Die Kreisanimation im Hero der Startseite und auf der Login-Seite ist entfernt; die Login-Seite ist dunkel wie der Footer (#043751) mit weißem Logo, das Formular steht als helle Karte mittig. Mobil zeigt der Hero dafür die ruhige, helle Hallenseite des Fotos hinter dem Text.

## Neue Bilder (14.11.2026)

Generiert mit Higgsfield (GPT Image 2.6), ruhige Nahaufnahmen, Motiv rechts, links Ruhe für die Schrift.

- Startseite-Hero: Hände sortieren Altbatterien. Ab 901 px Querformat; bis 900 px ein eigenes Hochformat, das unten bündig in voller Breite sitzt und nach oben ausläuft – die Hände liegen unter dem Text, nie dahinter.
- ECOACADEMY und ECOVENTURES: Kopfbereich mit Foto (Menschen im Gespräch) unter einem Schleier in der Bereichsfarbe; darunter je eine Bildreihe (ACADEMY: Gruppe, Flipchart, Frage und Antwort; VENTURES: Pitch, Team am Board).
- Alle Bilder als WebP im verschlüsselten Inhalt eingebettet (zusammen ca. 390 KB).

Startseite: Balken ECOACADEMY und ECOVENTURES luftiger – mehr Innenabstand (64–112 px statt 40 px), größere Spaltenabstände, mehr Luft zwischen Kicker, Logo, Claim, Text und Punkten (14.11.2026).
- Navigation: ECOLOGICON, ECORELOOP und ECOINVEST als Wortmarke aus dem Logo (Farben wie im Logo, ohne Signet und Unterzeile); ECOACADEMY und ECOVENTURES als Untermenü unter „Über uns“ (eigene Seiten `/#/ecoacademy`, `/#/ecoventures`). Bis 1199 px Breite Menü-Knopf statt Navigationsleiste.

## LinkedIn-Kanal (Präsentation unter dem Footer, 18.11.2026)

Unter dem Footer steht ein klar abgesetzter Präsentationsbereich (Farbleiste, „Ende der Website“, „Neuer Bereich · Präsentation“), der nicht zur Website gehört und vor dem Livegang entfernt wird:

- Simulation der LinkedIn-Unternehmensseite ECOWERTH in drei Ansichten (Desktop, Tablet, Smartphone, einzeln oder alle drei), mit klickbaren Reitern, Dokumenten und Beitragsliste; simulierter Stand 02.04.2027.
- Kanalstrategie, Seitenaufbau (alle Felder zum Kopieren), Fokusseiten, Umstellung der bisherigen ECOLOGICON-Seite.
- Redaktionsplan: 2 Vorlauf-Beiträge (Dez. 2026), 35 Beiträge in zwölf Wochen ab 12.01.2027, 5 Reserve-Beiträge – alle ausformuliert.
- Direktlink nach dem Login: `/#/linkedin`. Auf Impressum und Datenschutz ausgeblendet. Bilder und Logos stammen aus der Website selbst (keine zusätzlichen Dateien, keine fremden Server).

## Dunkle Ansicht, Wissen & Wachstum, Sachverständigenbüro (19.11.2026)

- **Hell / Dunkel:** Die Website öffnet in der dunklen Ansicht in #043751 wie ECOWERTH CAMPUS (Abstimmung mit Florian Werthmann, 18.11.2026). Ein dezenter Schalter in der Kopfzeile (auch auf dem Telefon sichtbar) wechselt zur hellen Ansicht; die Wahl merkt sich der Browser (`ecowerth-theme`). In der dunklen Ansicht stehen die Logos in Weiß, die Wortmarken der Navigation mit aufgehellten Markenfarben. Der LinkedIn-Bereich unter dem Footer bleibt hell.
- **ECOACADEMY und ECOVENTURES** in #043751 und Abstufungen statt Violett/Orange: Balken und Seitenköpfe als dunkelblaue Flächen, Logos in Dunkelblau bzw. Weiß. Unterschieden werden die beiden gleichwertigen Bereiche durch je eine dezente Zusatzfarbe (ECOACADEMY Salbei #85B8A5, ECOVENTURES Sand #C1A681) an Kante, Linien, Punkten und Chips.
- **Sachverständigenbüro Florian Werthmann** als eigene kleine Website unter „Über uns“ (`/#/sachverstaendiger`): Übersicht, Florian Werthmann, Leistungen, Herstellerverantwortung (OfH), Anfrage – Deutsch und Englisch, Inhalte aus dem Masterdokument vom 18.11.2026. Später zusätzlich unter florianwerthmann.com vorgesehen.

## Änderungen

Dieses Repository ist öffentlich. Deshalb liegen die lesbare Quelle, die Vorlagen und die Build-Skripte nicht hier, sondern im Claude-Projekt „ECOWERTH WEBSEITE“. Nach einer Änderung werden `public/index.html` (`protect.mjs … --standalone`) und die beiden Rechtsseiten (`legal.mjs`) dort neu gebaut und hierher gepusht.

Abmelden im Browser: `#abmelden` an die Adresse hängen.

Ein geteiltes Passwort ist ein Sichtschutz, keine Zugriffskontrolle.

## Vor dem Livegang auf ecowerth.de / ecowerth.com

1. Offene Angaben im Impressum und in der Datenschutzerklärung ergänzen (rot markierte Platzhalter: Handelsregister, USt-IdNr., ggf. Datenschutzbeauftragter).
2. Vercel-Team auf Pro umstellen: nur dann gilt der DPA, und Hobby ist laut Vercel ausschließlich für nicht-kommerzielle Nutzung. Danach den Platzhalter zum DPA entfernen.
3. Domains im Vercel-Projekt hinzufügen und die DNS-Einträge beim Domain-Anbieter setzen.
4. Login entfernen, `robots.txt` und den Header `X-Robots-Tag` freigeben.
5. Formulare (Kontakt ecowerth, Kontakt ECOLOGICON, Expertenregistrierung mit Lebenslauf-Upload) erst mit Formulardienst und ergänzter Datenschutzerklärung in Betrieb nehmen.
