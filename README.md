# SCIO-Family 

**SCIO-Family (SF) ist Wissenspoker für die ganze Familie:** Statt um Karten pokert ihr um euer Wissen. Jede Runde gibt es eine (Schätz)frage. Jeder schreibt seine Antwort geheim auf und setzt Chips darauf, wie nah er wohl dran ist. Nach und nach kommen zwei Tipps und die Lösung dazu. Am Ende gewinnt, wer am nächsten liegt.

Die Fragen sind für Kinder ab 10 Jahren geeignet und vermitteln Wissen aus ganz unterschiedlichen Bereichen. Nebenbei lernt man die Abläufe beim Poker: Geber, Blinds, Setzrunden und Showdown. Das Handy liegt in der Mitte des Tisches und führt durch das Spiel.

## Material

- 4 Spieler (Standard)
- Pokerchips: 50 pro Spieler
- Zettel und Kuli für jeden Spieler
- ein Geber-Knopf, zum Beispiel eine Münze oder ein besonderer Chip
- ein Handy mit SCIO

## Geber und Blinds

Vor jeder Frage, also noch *blind* ohne die Frage zu kennen, setzen zwei Spieler einen Pflichteinsatz:

- **Small Blind:** Der Spieler links vom Geber legt **1 Chip** in den Pot.
- **Big Blind:** Der Spieler links daneben legt **2 Chips** in den Pot.

Zu Beginn wird ein Geber ausgelost. Nach jeder Frage wandert der Geber-Knopf einen Platz im Uhrzeigersinn weiter, damit jeder mal die Blinds zahlt. Den Geber regelt ihr am Tisch. Die App erinnert euch nur daran, wann die Blinds fällig sind.

## Ablauf einer Runde

| Schritt | Was passiert | danach |
|---|---|---|
| Blinds | Geber-Knopf weitergeben, Small Blind und Big Blind setzen | – |
| Frage | Jeder schreibt seine Antwort verdeckt auf | 1. Setzrunde |
| Tipp 1 | Erster Hinweis | 2. Setzrunde |
| Tipp 2 | Zweiter Hinweis | 3. Setzrunde |
| Lösung | Richtige Antwort, die Zettel bleiben verdeckt | 4. Setzrunde |
| Showdown | Alle, die noch dabei sind, decken ihre Zettel auf | Pot geht an die nächste Antwort |

## Setzen

- **1. Setzrunde:** Sie beginnt beim Spieler links vom Big Blind. Wer weiterspielen will, muss mindestens 2 Chips bringen (*mitgehen*) oder *erhöhen*, sonst steigt er aus. Hat niemand erhöht, darf der Big Blind zum Schluss noch *schieben* oder selbst erhöhen.
- **2. bis 4. Setzrunde:** Es beginnt der erste Spieler links vom Geber, der noch dabei ist. Solange niemand gesetzt hat, darf man *schieben*.
- **Limits:** Man darf höchstens um 5 Chips erhöhen und in jeder Setzrunde höchstens dreimal.
- **Aussteigen:** Wer aussteigt, verliert alles, was er bis dahin eingesetzt hat. Bleibt nur ein Spieler übrig, bekommt er den Pot, ohne seinen Zettel zu zeigen. Mit **Nächste Frage** geht es dann direkt weiter.
- **All-in:** Wer nicht mehr genug Chips hat, setzt alles. Er kann dann von jedem Mitspieler höchstens so viel gewinnen, wie er selbst eingesetzt hat.
- **Gleichstand:** Der Pot wird geteilt. Ein Chip, der übrig bleibt, wandert in den Pot der nächsten Frage.

Nach der Lösung kennt jeder seine eigene Treffsicherheit, aber nicht die der anderen. Jetzt lohnt sich Bluffen.

**Spielende:** nach 10 Fragen. Wer dann die meisten Chips hat, gewinnt. Wer keine Chips mehr hat, scheidet vorher aus.

## Bedienung

- **Großer Knopf:** Er führt durch jede Runde, von den Blinds über die Frage, die Tipps und die Lösung zum Showdown.
- **‹** geht einen Schritt zurück.
- **Nächste Frage »** springt sofort zur nächsten Frage, zum Beispiel wenn alle bis auf einen ausgestiegen sind.
- **↻** zieht eine andere Frage, zum Beispiel wenn jemand die Antwort schon kennt.
- **Fokus / Tisch:** In der Ansicht *Fokus* steht nur die aktuelle Info groß im Bild. In der Ansicht *Tisch* gibt es zwei gegenüberliegende Karten, damit von beiden Tischseiten gelesen werden kann.

Ein Spiel zieht 10 zufällige Fragen aus einem Pool von 200. Wiederholungen gibt es erst, wenn alle Fragen einmal dran waren. Der Spielstand wird im Browser gespeichert.

## Auf dem iPhone installieren

1. Die GitHub-Pages-Adresse in **Safari** öffnen: `https://ux3257.github.io/scio/`
2. **Teilen → Zum Home-Bildschirm** antippen.

SCIO startet dann im Vollbild mit eigenem Icon.

## Fragen ergänzen

Die Fragen stehen in der Datei `fragen.js`. Jede Frage ist eine Zeile:

```js
["Kategorie", "Frage?", "Tipp 1", "Tipp 2", "Antwort", "Zusatz (optional)"],
```

Regeln für SF-Fragen:

- **Kindgerecht** und lehrreich, aus möglichst verschiedenen Kategorien.
- **Exakte Antworten:** eine Zahl oder Jahreszahl, nie „ca.“.
- **Tipps nicht ausrechenbar:** Ein Tipp darf sich auf etwas anderes beziehen, aber dessen Zahl nicht mitliefern. „10 Jahre vor der Mondlandung“ ist erlaubt, „10 Jahre vor der Mondlandung (1969)“ nicht.

Wie viele Fragen ein Spiel hat, legt `const ROUNDS = 10;` in der `index.html` fest.

## Dateien

| Datei | Inhalt |
|---|---|
| `index.html` | das Spiel |
| `fragen.js` | der Fragenpool mit 200 Fragen |
| `manifest.webmanifest` | App-Name, Farben und Icons für den Home-Bildschirm |
| `apple-touch-icon.png`, `icon-192.png`, `icon-512.png` | App-Icons |

Die Seite ist für Suchmaschinen gesperrt (`noindex`). Sie ist aber für jeden aufrufbar, der die Adresse kennt.
