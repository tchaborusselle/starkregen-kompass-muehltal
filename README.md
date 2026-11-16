# Starkregen-Kompass Mühltal – GitHub Pages

**Wissenschaftlicher Arbeitsprototyp. Keine amtliche Risikobewertung oder Priorisierung.**

## Online veröffentlichen (ohne Streamlit und ohne Python)

1. Auf https://github.com anmelden und ein **neues öffentliches Repository** erstellen, z. B. `starkregen-kompass-muehltal`. Hinweis: GitHub Pages einer kostenlosen persönlichen GitHub-Nutzung setzt für diese einfache Einrichtung normalerweise ein öffentliches Repository voraus; alle darin veröffentlichten Daten sind öffentlich sichtbar.
2. **Vor dem Upload die Datenfreigabe und Nutzungsrechte klären.** Projektberichte und Quellenhinweise können Freigaben benötigen.
3. Die Dateien `index.html`, `style.css`, `app.js` sowie den gesamten Ordner `daten` in das Repository-Hauptverzeichnis hochladen; die Ordnerstruktur unverändert lassen.
4. Unter **Settings → Pages → Build and deployment → Deploy from a branch** den Branch `main` und Ordner `/(root)` auswählen, dann speichern.
5. Die Webseite unter `https://BENUTZERNAME.github.io/starkregen-kompass-muehltal/` aufrufen (BENUTZERNAME ersetzen). Die Bereitstellung kann ein wenig dauern.
6. Nur du erhältst Schreibrechte im Repository; Besucher können Filter bedienen und CSV-Dateien herunterladen, aber nichts dauerhaft verändern. Beachte: Bei einem öffentlichen Repository ist der Quellcode für alle lesbar.

## Lokaler Test

`index.html` per Doppelklick kann die JSON-Dateien wegen Browser-Sicherheitsregeln nicht laden. Starte aus diesem Ordner stattdessen beispielsweise `python -m http.server 8000` und öffne `http://localhost:8000`.

## Enthaltene Module

- Dashboard mit echten Rohdaten und Herkunftshinweisen
- 59 Originalprobleme mit Original-IDs, Filter und Volltextsuche
- 85 vorläufige Maßnahmen-/Varianteneinträge mit Original-IDs, Filter und Volltextsuche
- Übersicht über die **vorläufige** Bewertungsmatrix für 13 Untersuchungseinheiten (aus dem vorhandenen Miro-Zwischenstand)
- Maßnahmen-Szenario-Labor: beliebige Einträge auswählen, kombinieren und als CSV exportieren; **keine erfundenen Kosten oder Wirksamkeiten**
- Methodik und Datenlimits
- Druck / PDF über Browser-Druckdialog

## Datenstand / Grenzen

`daten/probleme.json` wurde aus `Probleme_je_Gruppe.xlsx` (Original-ID 1–59) erzeugt; `daten/massnahmen.json` aus `Muehltal_Massnahmen_1_bis_85_fortlaufend.xlsx` (Original-ID 1–85). Die Häufigkeitsdiagramme verwenden die **unveränderten Original-Ortsangaben** der Tabellen, die teils von der späteren räumlichen Klassifizierung auf Miro abweichen. Eine automatische Gleichsetzung wäre methodisch falsch.

13 Untersuchungseinheiten stammen aus der späteren Risikobewertung, nicht aus einem neuen Geodatensatz. Es liegen keine geprüften Geokoordinaten, keine belastbaren Kosten und keine validierten Problem-Maßnahmen-Zuordnungen vor; deshalb gibt es **noch keine GIS-Punktkarte**, keine errechnete Problemabdeckung und keine Maßnahmenrangliste.

Mehrfachnennungen, Varianten und Umsetzungsansätze sind in den 85 Einträgen enthalten. Für die wissenschaftliche Auswertung müssen sie zunächst bereinigt und geprüft werden.

## Weiterentwicklungen

1. Prüfte räumliche Daten/GIS-Koordinaten und lizensierte Hintergrundkarte integrieren.
2. Bereinigten Maßnahmenkatalog mit belastbar dokumentierten Problemverknüpfungen.
3. Kosten und Wirksamkeit nur bei nachgewiesener Datengrundlage ergänzen; bei fehlenden Angaben klar kennzeichnen.
4. Sensitivitätsanalyse und Szenarienvergleich erst nach methodischer Definition und Validierung.

## Sicherheit

Die Website verwendet keine Datenbank und speichert keine Besuchereingaben; die Maßnahmenauswahl gilt nur in der aktuellen Browser-Sitzung. Statische GitHub Pages bieten keine serverseitige vertrauliche Speicherung oder Login-Verwaltung. Bitte keine personenbezogenen oder nicht freigegebenen Projektinformationen in die öffentlichen JSON-Dateien stellen.
