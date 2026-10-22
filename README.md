# Führerstand DS 301

Lern- und Übungssimulator für den Führerstand: Signale nach DS 301 (Signalbuch der DB), PZB 90 und Sifa in 17 Übungsszenarien auf fiktiven Strecken und 5 Szenarien auf der AVG-Linie S4 nach Buchfahrplan. Läuft im Browser auf Android, iOS und am PC – ohne Installation, ohne Build.

## Inhalt

- **Signalsysteme:** Ks (Ks 1, Ks 1 blinkend, Ks 2, Hp 0, Zs 3, Zs 3v), H/V (Hp 0/1/2, Vr 0/1/2, Ne 2), Lf 6/Lf 7, Ne 1 (Trapeztafel), Ne 3 (Vorsignalbaken), Ne 4 (Schachbretttafel an links stehenden Hauptsignalen der S4), Bü 4 (Pfeiftafel vor Bahnübergängen der S4), Ne 5, Ne 6 (Haltepunkttafel), Sh 0/Sh 1, Ra 10, Ersatzsignale Zs 1, Zs 7, Zs 8, Hektometertafeln alle 100 m, Bezeichnungstafeln an den Tunnelportalen (Name, Tunnelsymbol, Länge)
- **Gegengleis:** Mit Zs 8 fährt der Zug über die Weichenverbindung auf das Gegengleis (Weichenbereich 40 km/h), dort wirken die Gleismagnete des Regelgleises nicht; vor der nächsten Betriebsstelle zurück auf das Regelgleis. Am Gegengleis steht in Höhe des Einfahrsignals die Trapeztafel Ne 1 mit Kilometerangabe und 2000-Hz-Magnet – Vorbeifahrt nur mit Zustimmung des Fdl und Befehl, sonst Zwangsbremsung
- **Signallogik:** selbsttätiger Streckenblock mit vorausfahrendem Zug, Ausfahrt nach Haltezeit, gestörte Signale mit Ersatzsignal durch den Fdl
- **PZB 90 nach Ril 483 und AVG-Schulungsunterlage Modul 17:**
  - Gleismagnete 1000/500/2000 Hz, Doppelgleismagnet 1000/2000 Hz am Mehrabschnittssignal, 500 Hz vor Zs 3 bis Kennziffer 3
  - Geschwindigkeitsprüfabschnitt (GPA) an Lf 6 Kennziffer 8/9, Geschwindigkeitsüberwachungsabschnitt (GÜ, 2000 Hz) vor Lf 7 ab Kennziffer 10
  - Zugarten O/M/U, Bremskurven, Wachsam binnen 4 s, Wachsam auch an Signalen in Warnstellung ohne wirksamen Magnet
  - Restriktive Überwachung (Wechselblinken), Startprogramm, Befreien mit Prüfung der Zulässigkeit, „Unberechtigtes Befreien“
  - Befehl 40 (über 40 km/h wirkungslos), Leuchtmelder nach I60R inkl. „Fahrzeug hat gesandet“
  - Ablauf nach PZB-Zwangsbremsung mit Fdl (mündliche Zustimmung bzw. Befehl 2), gestörte Streckeneinrichtung melden
  - Funktionsprüfung (Wachsam + Frei), 5-km/h-Puffer nach Ril 483
  - Fahrzeugwahl: Regelfahrzeug oder AVG-Stadtbahn (PZB 90 Version AVG nach Schaublatt Betriebszustände: Zugart O fest, 100 km/h, Frühhalt VÜ 3 / Späthalt VÜ 2, nach 500 Hz 15 s unter 30 km/h → 25 km/h, Startprogramm 550 m)
  - PZB gestört (Leuchtmelder dunkel) und PZB-Störschalter: 50 km/h bis PZB i. O., Meldung an BZ (mit Bitte um Vormeldung) und Zü AVG, Störschalter nur bei ständiger Zwangsbremsung
  - Leuchtmelder „S“ (Zwangsbremsung wirksam) und „PZB“ (störungsfreier Betrieb), Textanzeigen wie EBI Cab 500, Schaublatt als Tabelle in der Hilfe
- **Sifa:** 30-s-Zyklus mit Leuchtmelder, Summer und Zwangsbremsung
- **Pfeife:** Taste zum Halten; an der Pfeiftafel Bü 4 etwa 3 s pfeifen, sonst Fehler am Bahnübergang
- **Fahrgastbetrieb:** zusätzliche Haltepunkte, Türen freigeben und schließen, Fahrgastwechsel mit wartenden Reisenden, Traktionssperre bei offenen Türen, Ansage „Nächster Halt“
- **Fahrplan:** Buchfahrplan je Zug mit Ankunft/Abfahrt, Blockstellen und Geschwindigkeitswechseln, Uhr und Verspätung im Streckenbild, Fehler bei vorzeitiger Abfahrt, Pünktlichkeitsauswertung
- **Signalabstände nach DS 301:** Vorsignal im Bremswegabstand (Streckenbuch: 1000/700/400 m), Ne 2 unmittelbar davor, Ne 3 250/175/100 m vor dem Vorsignal, Ne 6 im Bremswegabstand vor dem Bahnsteig, verkürzter Vorsignalabstand mit weißem Zusatzlicht, Lf 6 im Bremswegabstand vor Lf 7, 500 Hz ca. 250 m vor dem Hauptsignal, Durchrutschweg 200 m
- **S4 nach Buchfahrplan:** Strecke Grötzingen – Bretten – Eppingen – Heilbronn – Öhringen mit Original-Kilometrierung, Geschwindigkeiten aus Spalte 2 (als Lf 6/Lf 7 angezeigt), Tunneln und Zugkreuzungen
- **Gleisbögen:** sichtbare Kurven im Streckenbild; in den Übungsszenarien 5–20 Bögen mit ständiger Geschwindigkeitsbeschränkung (Lf 6 im Bremswegabstand, Lf 7 am Bogenanfang und -ende) samt PZB nach Ril 483 (ständiger 1000-Hz-Magnet, GPA, GÜ); Fahrpläne angepasst
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
| 8 | Mittel | Gegengleis Zs 8 | Zs 8, Fahrt auf dem Gegengleis und zurück, Weichenbereich 40 km/h |
| 9 | Mittel | Dichter Zugverkehr | Zugfolge im Blockabstand, häufig Ks 2 |
| 10 | Mittel | Nebel | 300 m Sicht |
| 11 | Schwer | Schwerer Güterzug | 550 m, Zugart U, schwache Bremse |
| 12 | Schwer | Schnellfahrt | Zugart O, 160 km/h |
| 13 | Schwer | Störungen im Betrieb | Zs 7, Zs 1, Zs 8 und Zugfolge kombiniert |
| 14 | Schwer | Nachtfahrt | nur Signallichter weit sichtbar |
| 15 | Schwer | Abschlussfahrt | Gesamtstrecke mit Rangierfahrt, ohne Lernhilfe |
| 16 | Schwer | S-Bahn-Takt | Ks-Block alle 700 m, Halt alle 1,4 km, S-Bahn voraus, Taktfahrplan |
| 22 | Schwer | PZB-Störung | LM 85 dunkel → 50 km/h, melden, neu aufrüsten (Startprogramm); ständige ZB → Störschalter |
| 17 | S4 | S4 Grötzingen – Bretten | nach Buchfahrplan, Jöhlinger Tunnel |
| 18 | S4 | S4 Bretten – Eppingen | Brettener/Gölshauser/Sulzfelder Tunnel, Zs 3 „6“, Kreuzung Flehingen |
| 19 | S4 | S4 Eppingen – Heilbronn | Km-Sprung 43,4 = 140,0, Zwischensignale Schwaigern/Leingarten |
| 20 | S4 | S4 Heilbronn – Öhringen | Innenstadt (BOStrab), Weinsberger Tunnel, Kreuzungen Weinsberg/Eschenau |
| 21 | S4 | S4 Gesamtstrecke | Grötzingen Oberausstraße – Öhringen-Cappel, ca. 91 km, 60 Halte |

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
| `F` | Fahrdienstleiter verständigen |
| `X` | PZB-Störschalter (nur im Stillstand) |
| `H` (halten) | Pfeife |
| `T` | Türen freigeben / schließen |
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
