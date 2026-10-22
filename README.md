# SCIO

**Wissenspoker:** Statt um Karten pokert ihr um euer Wissen. Jede Runde gibt es eine Schätzfrage. Jeder schreibt seine Antwort geheim auf und setzt Chips darauf, wie nah er wohl dran ist. Nach und nach kommen zwei Tipps und die Lösung dazu. Am Ende gewinnt, wer am nächsten liegt.

Das Handy liegt in der Mitte des Tisches und zeigt Fragen, Tipps und Lösungen an.

## Material

- Pokerchips (oder Spielgeld, Streichhölzer …)
- Zettel und Kuli für jeden Spieler
- ein Handy mit SCIO

## Ablauf einer Runde

| Schritt | Was passiert | danach |
|---|---|---|
| Frage | Jeder schreibt seine Antwort verdeckt auf | 1. Setzrunde |
| Tipp 1 | Erster Hinweis | 2. Setzrunde |
| Tipp 2 | Zweiter Hinweis | 3. Setzrunde |
| Lösung | Richtige Antwort, die Zettel bleiben verdeckt | 4. Setzrunde |
| Showdown | Alle Zettel aufdecken | Pot geht an die nächste Antwort |

Gesetzt wird wie beim Poker: schieben, setzen, mitgehen, erhöhen oder aussteigen. Nach der Lösung kennt jeder seine eigene Treffsicherheit, aber nicht die der anderen. Jetzt lohnt sich Bluffen. Bei Gleichstand wird der Pot geteilt.

**Vorschlag für zwei Spieler:** Jeder startet mit 30 Chips und legt pro Frage 1 Chip als Einsatz in den Pot. Pro Setzrunde setzt man 0–5 Chips und darf nur einmal erhöhen. Wer zuerst setzt, wechselt mit jeder Frage.

## Bedienung

- **Großer Knopf:** Er führt durch die Runde, von der Frage über die Tipps und die Lösung zum Showdown und dann zur nächsten Frage.
- **‹** geht einen Schritt zurück.
- **↻** zieht eine andere Frage, zum Beispiel wenn jemand die Antwort schon kennt.
- **Fokus / Tisch:** In der Ansicht *Fokus* steht nur die aktuelle Info groß im Bild. In der Ansicht *Tisch* gibt es zwei gegenüberliegende Karten, damit von beiden Tischseiten gelesen werden kann.

Ein Spiel hat 5 zufällige Fragen aus dem Fragenpool. Wiederholungen gibt es erst, wenn alle Fragen einmal dran waren. Der Spielstand wird im Browser gespeichert.

## Auf dem iPhone installieren

1. Die GitHub-Pages-Adresse in **Safari** öffnen: `https://ux3257.github.io/scio/`
2. **Teilen → Zum Home-Bildschirm** antippen.

SCIO startet dann im Vollbild mit eigenem Icon.

## Fragen ergänzen

Die Fragen stehen in der `index.html` im Array `Q`. Jede Frage ist eine Zeile:

```js
["Kategorie", "Frage?", "Tipp 1", "Tipp 2", "Antwort", "Zusatz (optional)"],
```

Die Antwort sollte eine Zahl oder Jahreszahl sein, damit sich der Abstand vergleichen lässt. Wie viele Fragen ein Spiel hat, legt `const ROUNDS = 5;` fest.

## Dateien

| Datei | Inhalt |
|---|---|
| `index.html` | das komplette Spiel |
| `manifest.webmanifest` | App-Name, Farben und Icons für den Home-Bildschirm |
| `apple-touch-icon.png`, `icon-192.png`, `icon-512.png` | App-Icons |

Die Seite ist für Suchmaschinen gesperrt (`noindex`). Sie ist aber für jeden aufrufbar, der die Adresse kennt.
