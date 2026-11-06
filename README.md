# Rauchstopp

Wie viel ich rauche, und wie es sich entwickelt. Eine Seite fürs Handy, im Stil von [Tagesgeld](https://github.com/AlbrechtBuehler/tagesgeld).

Ein Knopf «+1 Zigarette» erfasst die Uhrzeit. Darunter stehen heute, gestern, der Schnitt der letzten 7 Tage und der Woche davor, der Verlauf über 4 Wochen und die letzten 14 Tage zum Korrigieren.

- Gezählt wird ab dem Tag, an dem die App zum ersten Mal offen war. Tage danach ohne Eintrag sind echte Nuller und zählen im Schnitt mit.
- Ein Tag ist der Kalendertag: eine Zigarette um 00:30 gehört zum neuen Tag.
- **Ø 7 Tage** = Zigaretten von gestern und den 6 Tagen davor ÷ 7. Heute zählt nicht mit, weil der Tag noch läuft. Gibt es noch keine 7 Tage, wird über die vorhandenen geteilt.
- **Rückgängig** steht 10 Sekunden nach dem Tippen und nimmt genau diesen Eintrag zurück. Später korrigiert man über die Tage-Liste: Uhrzeit antippen und löschen, oder eine vergessene nachtragen.
- Fassung 1 zählt nur. Tageslimit und Stopptag kommen, wenn das Ziel steht.

## Daten

Nur auf dem Gerät (`localStorage`). In dieses Repo gehört nie ein echter Eintrag.

«Als Tabelle sichern» gibt eine CSV-Datei mit einer Zeile pro Tag (Datum, Wochentag, Anzahl, Uhrzeiten). «Alles zurücksetzen» löscht nach einer Rückfrage alle Einträge; danach zählt die App ab heute neu.

## Dateien

| Datei | Was |
| --- | --- |
| `index.html` | die App, Schrift Jost eingebettet |
| `sw.js` | hält die App für den Start ohne Netz; bei jeder neuen Fassung `FASSUNG` hochzählen |
| `manifest.webmanifest`, `icon-*.png` | Installation auf dem Startbildschirm |
