# Führerstand DS 301

Lern- und Übungssimulator für den Führerstand: Signale nach DS 301 (Signalbuch der DB), PZB 90 und Sifa auf einer fiktiven Übungsstrecke. Läuft im Browser auf Android, iOS und am PC – ohne Installation, ohne Build.

## Inhalt

- **Signalsysteme:** Ks (Ks 1, Ks 1 blinkend, Ks 2, Hp 0, Zs 3, Zs 3v), H/V (Hp 0/1/2, Vr 0/1/2, Ne 2), Lf 6/Lf 7, Ne 5, Sh 0/Sh 1, Ra 10, Ersatzsignale Zs 1, Zs 7, Zs 8
- **Signallogik:** selbsttätiger Streckenblock mit vorausfahrendem Zug, Ausfahrt nach Haltezeit, gestörte Signale mit Ersatzsignal durch den Fdl
- **PZB 90 (vereinfacht nach Ril 483):** 1000/500/2000 Hz, Zugarten O/M/U, Bremskurven, restriktive Überwachung, Wachsam/Frei/Befehl 40
- **Sifa:** 30-s-Zyklus mit Leuchtmelder, Summer und Zwangsbremsung
- **Auswertung:** Signalverstöße, Geschwindigkeitsüberschreitungen, ausgelassene Halte, Zwangsbremsungen

## Strecke

RB 3807 Lindenau – Bergheim – Waldheim – Tannau (≈ 20 km), danach Rangierfahrt ins Abstellgleis bis vor die Ra 10.

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
