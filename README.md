# Summit.

**Budget für die Schweiz.** Ein Ausgaben-Tracker fürs iPhone, der Karte, Apple Pay, TWINT, Online-Käufe und Bargeld an einem Ort zusammenführt, ohne Bankzugangsdaten.

## Inhalt

| Ordner | Was |
|---|---|
| `landing/` | Landingpage mit Warteliste (eine HTML-Datei, kein Build nötig) |
| `ios/` | iOS-App (folgt, braucht Xcode) |

## Landingpage lokal starten

```bash
python3 -m http.server 4321 --directory landing
```

Dann <http://localhost:4321> öffnen.

**Offen:** Das Wartelisten-Formular speichert noch nur im Browser (`localStorage`). Vor dem Schalten von Ads an einen echten Dienst anbinden (z. B. Formspree, Tally oder Supabase). Die Stelle ist im Code mit `TODO` markiert. Impressum, Datenschutz und Kontakt-Adresse im Footer sind Platzhalter.

## Animations- und UX-Prinzipien

| # | Prinzip | Wo auf der Seite |
|---|---|---|
| 1 | Squash & Stretch | Buttons und Kategorie-Chips stauchen beim Drücken, die fliegende Betrags-Pille dehnt sich unterwegs |
| 2 | Anticipation | Pfeil-Button holt aus, Mitteilung schwingt vor dem Einrasten über |
| 3 | Staging | Bei den Kanälen bleibt nur die Karte unter der Maus im Fokus, die Schritte leuchten einzeln auf |
| 4 | Pose to Pose | Akzentwort im Hero wechselt zwischen klaren Zuständen |
| 5 | Follow-through | Nach dem Tipp federt die Kategorie-Zeile nach, Zahl und Donut ziehen hinterher |
| 6 | Slow in & Slow out | Überall Ease-Kurven, nie linear |
| 7 | Moving in Arcs | Der Betrag fliegt auf einem Bogen in die Kategorie |
| 8 | Secondary Action | Funken bei jedem Einordnen und beim Eintragen |
| 9 | Snappy Timing | UI-Reaktionen 160–280 ms |
| 10 | Exaggerated Feedback | Falsche E-Mail lässt das Feld schütteln und rot aufleuchten |
| 11 | Solid Drawing (3D) | Telefone und Kacheln neigen sich mit der Maus |
| 12 | Appeal | Ruhige Farbwelt, weiche Schatten, klare Typografie |
| 13 | Fitts | Grosse Haupt-Buttons (56 px) |
| 14 | Bigger Hit Areas | Pager-Punkte haben eine unsichtbar vergrösserte Trefferfläche |
| 15 | Hick | Drei Kategorie-Vorschläge, ein empfohlener Preisplan |
| 16 | Miller | Drei Schritte, Beträge mit Tausendertrennung (1'487.20) |
| 17 | Doherty | Warteliste bestätigt sofort, Speichern läuft danach |
| 18 | Postel | E-Mail wird grosszügig angenommen (Leerzeichen, Grossbuchstaben) und sauber gespeichert |
| 19 | Jakob | Vertraute Muster: Navigation, Akkordeon-FAQ, Preis-Karten |
| 20 | Frequency of Use | Scroll-Animationen laufen pro Element nur einmal |

`prefers-reduced-motion` wird respektiert.
