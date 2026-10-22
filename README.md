# Führerstand DS 301

Lern- und Übungssimulator für den Führerstand: Signale nach DS 301 (Signalbuch der DB), PZB 90 und Sifa in 15 Übungsszenarien auf fiktiven Strecken. Läuft im Browser auf Android, iOS und am PC – ohne Installation, ohne Build.

## Inhalt

- **Signalsysteme:** Ks (Ks 1, Ks 1 blinkend, Ks 2, Hp 0, Zs 3, Zs 3v), H/V (Hp 0/1/2, Vr 0/1/2, Ne 2), Lf 6/Lf 7, Ne 5, Sh 0/Sh 1, Ra 10, Ersatzsignale Zs 1, Zs 7, Zs 8
- **Signallogik:** selbsttätiger Streckenblock mit vorausfahrendem Zug, Ausfahrt nach Haltezeit, gestörte Signale mit Ersatzsignal durch den Fdl
- **PZB 90 (vereinfacht nach Ril 483):** 1000/500/2000 Hz, Zugarten O/M/U, Bremskurven, restriktive Überwachung, Wachsam/Frei/Befehl 40
- **Sifa:** 30-s-Zyklus mit Leuchtmelder, Summer und Zwangsbremsung
- **Auswertung:** Signalverstöße, Geschwindigkeitsüberschreitungen, ausgelassene Halte, Zwangsbremsungen

## Szenarien

| Nr. | Stufe | Szenario | Schwerpunkt |
|---|---|---|---|
| 1 | Leicht | Erste Fahrt | Anfahren, Lf 6/Lf 7, Zs 3, Sifa, Haltetafel |
| 2 | Leicht | Halt erwarten | Ks 2, 1000 Hz/Wachsam, 500-Hz-Prüfung, Halt vor Hp 0 |
| 3 | Leicht | H/V-Signale | Hp 0/1/2, Vr 0/1/2, Vorsignal am Mast |
| 4 | Leicht | Geschwindigkeitswechsel | Lf 6/Lf 7, Zs 3/Zs 3v, Ks 1 blinkend |
| 5 | Leicht | Rangierfahrt | 25 km/h, Sh 0/Sh 1, Ra 10 |
| 6 | Mittel | Ersatzsignal Zs 1 | Halt vor gestörtem Signal, Befehl 40 |
| 7 | Mittel | Vorsichtsignal Zs 7 | Fahrt auf Sicht, stehender Zug im Gleis |
| 8 | Mittel | Gegengleis Zs 8 | Zs 8, Weichenbereich 40 km/h |
| 9 | Mittel | Dichter Zugverkehr | Zugfolge im Blockabstand, häufig Ks 2 |
| 10 | Mittel | Nebel | 300 m Sicht |
| 11 | Schwer | Schwerer Güterzug | 550 m, Zugart U, schwache Bremse |
| 12 | Schwer | Schnellfahrt | Zugart O, 160 km/h |
| 13 | Schwer | Störungen im Betrieb | Zs 7, Zs 1, Zs 8 und Zugfolge kombiniert |
| 14 | Schwer | Nachtfahrt | nur Signallichter weit sichtbar |
| 15 | Schwer | Abschlussfahrt | Gesamtstrecke mit Rangierfahrt, ohne Lernhilfe |

Bestandene Szenarien werden im Browser gespeichert (localStorage).

## Bedienung

| Taste | Funktion |
|---|---|
| `W` / `↑` | Hebel Richtung Fahren |
| `S` / `↓` | Hebel Richtung Bremsen |
| `Q` | Wachsam |
| `E` | Frei |
| `B` (halten) | Befehl 40 |
| `Leertaste` | Sifa |
| `P` | Pause |

Auf dem Smartphone werden Hebel und Tasten per Touch bedient.

## Starten

`index.html` im Browser öffnen – fertig.

### GitHub Pages

1. Repository auf GitHub anlegen und den Inhalt dieses Ordners hochladen.
2. *Settings → Pages → Source: Deploy from a branch*, Branch `main`, Ordner `/ (root)`.
3. Nach kurzer Zeit läuft der Simulator unter `https://<benutzer>.github.io/<repo>/`.

Auf Android lässt sich die Seite im Chrome-Menü über „Zum Startbildschirm hinzufügen“ wie eine App ablegen.

## Hinweis

Vereinfachte Fahrdynamik und PZB-Logik. Ersetzt weder Signalbuch noch Ausbildung.

## Lizenz

MIT – siehe [LICENSE](LICENSE).
