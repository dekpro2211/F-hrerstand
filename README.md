# Führerstand DS 301

Lern- und Übungssimulator für den Führerstand: Signale nach DS 301 (Signalbuch der DB), PZB 90 und Sifa in 17 Übungsszenarien auf fiktiven Strecken und 5 Szenarien auf der AVG-Linie S4 nach Buchfahrplan. Läuft im Browser auf Android, iOS und am PC – ohne Installation, ohne Build. Streckenbild wahlweise in 3D (WebGL, three.js) oder 2D.

## Streckenbild 3D/2D

- **3D-Ansicht (Standard):** echte räumliche Szene mit three.js – Gleisachse aus den Bögen der Strecke, Schotterbett, Schwellen, Schienen, Weichenverbindungen, Bahnhofsgleise 3/4, Inselbahnsteige mit Dach, Haltepunkte mit Wartehäuschen, Empfangsgebäude, Oberleitung mit Masten, Tunnel mit Portal und Bezeichnungstafel, Bahnübergänge mit Andreaskreuz, Felder, Bäume, Dörfer, Innenstadt Heilbronn als Straßenbahnabschnitt (BOStrab), Gegenzüge, vorausfahrender Zug, wartende Fahrgäste, Nebel, Nacht mit Sternen und Spitzenlicht
- Signale und Tafeln sind dieselben Signalbilder wie in 2D (als Textur), Signallichter leuchten weit sichtbar
- Die Auflösung passt sich der Leistung des Geräts an
- **2D-Ansicht:** Schalter „3D“ oben – für ältere Geräte; ohne WebGL startet automatisch 2D
- **Führerstand in 3D:** Pult mit Tacho (zulässige Geschwindigkeit als gelbe Marke), Manometern (Hauptluftbehälter, Bremszylinder), Fahrplanbildschirm, PZB-Leuchtmeldern, Fahrzeug-Leuchtmeldern (HS, Stromabnehmer, Kompressor, Türen, Sifa), Schalterreihe, beweglichem Fahr-/Bremshebel und Schnellbremstaster; Frontscheibe mit Wischern und Sonnenblende, **Seitenfenster** mit Schiebefenster und Außenspiegeln, Rückwand mit Tür; Pultbeleuchtung bei Nacht und im Tunnel; Wagenkasten schwankt leicht, Stöße an Weichen
- **Umschauen:** im Bild ziehen (Maus oder Finger), `←`/`→` bzw. `A`/`D` halten; Doppeltipp oder `C` zentriert
- **2D-Kabine:** in der 2D-Ansicht gezeichneter Fensterrahmen mit Pult; Schalter „Kabine“ blendet die Kabine aus

## Aufrüsten und Geräusche

- Jedes Szenario beginnt abgerüstet: **Motor starten** (Taste `M`) hebt den Stromabnehmer, schaltet den Hauptschalter ein und startet die Hilfsbetriebe – ohne Hauptschalter keine Zugkraft
- Druckluft: Kompressor schaltet bei 8 bar ein und bei 10 bar ab, jede Bremsung verbraucht Luft
- Geräusche (Web Audio, nach dem Vorbild eines Drehstrom-Triebwagens nachgebildet): Hubantrieb des Stromabnehmers, Hauptschalter, Lüfter, Kompressor mit Abblasen, Pulswechselrichter mit gestuften Taktfrequenzen („Singen“ beim Anfahren und elektrischen Bremsen), Getriebe, Rollgeräusch, Fahrtwind, lauter im Tunnel, Achsstöße an Weichen und Bahnübergängen, Bremsluft und Lösen, Bremsenquietschen kurz vor dem Halt, Türwarnton und Türen, Zweiklang-Signalhorn, Vorbeifahrt von Gegenzügen

## Straßenbahn Karlsruhe (Szenarien 31–35)

Stadtlinien 1–5 mit der Haltestellenfolge aus dem KVV-Liniennetzplan (Stand 2023). Abstände, Gleislage, Kreuzungen, Weichen und Abschnitte (Rasengleis / Straßenraum) sind angenommen. Fahrzeug Straßenbahn (37 m, 70 km/h), keine PZB, Fahren auf Sicht nach BOStrab, Glocke statt Pfeife.

| Nr. | Linie | Strecke |
|---|---|---|
| 31 | 1 | Neureut-Heide – Kunstakademie – Stadtbahntunnel (Europaplatz – Durlacher Tor) – Durlacher Allee – Durlach Turmberg |
| 32 | 2 | Knielingen Nord – Mühlburger Tor – Europaplatz – Südweststadt – Hauptbahnhof – Tunnel (Kongresszentrum – Durlacher Tor) – Durlach – Wolfartsweier Nord |
| 33 | 3 | Europaplatz – Karlstor – Hauptbahnhof – Tivoli – Rüppurrer Tor – Kronenplatz – Durlacher Tor – Hauptfriedhof – Rintheim |
| 34 | 4 | Oberreut Badeniaplatz – Weinbrennerplatz – Europaplatz – Kriegsstraße – Durlacher Tor – Hauptfriedhof – Waldstadt Europäische Schule |
| 35 | 5 | Rheinhafen – Entenfang – Kühler Krug – Kriegsstraße – Rüppurrer Tor – Ostendstraße – Durlacher Allee – Durlach Bf |

## Tram-Train (Szenario 23, Beispielstrecke)

- **EBO-Abschnitt** mit Ks-Signalen, PZB und Lf, dann **Systemwechsel 15 kV ~ / 750 V =**: El 1v (Ankündigung), El 1 (Hauptschalter aus), Systemtrennstelle ohne Spannung, El 2 (Hauptschalter wieder ein). Mit eingeschaltetem Hauptschalter in die Trennstelle → Fehler und Schutzabschaltung; Liegenbleiben in der Trennstelle beendet die Fahrt
- **So 2** – Ende der Zugsicherung, ab hier **BOStrab**: Rasengleis mit Alleebäumen und Fahrbahnen, Straßenbahn in der Straße mit Autoverkehr, Häuserzeilen
- **Fahrsignale** F 0 / F 1 / F 4 mit Anforderungsanzeige „A“ (St 9); an der Haltlinie warten, bis F 1 kommt – der Querverkehr fährt solange
- **Weichensignale** W 11 (verschlossen) und W 1 (nicht verschlossen, höchstens 15 km/h), **G-Signale** G 1a / G 2a / G 4, **Läutetafel Sh 4** (Glocke statt Pfeife), Haltestellen mit Sh 7
- **Stadtbahntunnel** mit Rampe, H-/V-Signalen, Ausfahrsignal nach Haltezeit, H 2 (40 km/h) und unterirdischen Haltestellen
- Der genaue Ablauf des Systemwechsels ist an die DB-Signale El 1/El 2 angelehnt und vereinfacht

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
  - Leuchtmelderblock wie im GT8 (85, 70, 1000 Hz, 500 Hz, Befehl 40, „Fzg hat gesandet“, Leuchttaster „Indusi Befehl“/„Indusi Frei“; Regelfahrzeug zusätzlich 55), Textanzeigen wie EBI Cab 500, Schaublatt als Tabelle in der Hilfe
- **Sifa:** 30-s-Zyklus mit Leuchtmelder, Summer und Zwangsbremsung
- **Bahnhofsgleise:** Einfahr- und Ausfahrweichen, Inselbahnsteig mit Gleis 3, Gleis 4; bei Zs 3/Hp 2 abzweigende Fahrt über Gleis 3, Weichenbereich bis zur letzten Weiche
- **Gegenverkehr:** Regionalzüge, Güterzüge und IC auf dem Nachbargleis (auf der S4 Stadtbahnen nur in den zweigleisigen Abschnitten), mit Spitzensignal und Vorbeifahrt; bei Gegengleisfahrt gesperrt
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
| 23 | Tram-Train | Systemwechsel und Innenstadt | El 1v/El 1/El 2, So 2, F-/W-/G-Signale, Sh 4, Stadtbahntunnel (fiktive Strecke) |
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
| `H` (halten) | Pfeife (im BOStrab-Abschnitt Glocke) |
| `T` | Türen freigeben / schließen |
| `M` | Motor starten / abstellen (Aufrüsten) |
| `←` `→` / `A` `D` | Umschauen in der 3D-Kabine, `C` zentriert |
| `P` | Pause |

Auf dem Smartphone werden Hebel und Tasten per Touch bedient.

## Starten

`index.html` im Browser öffnen – fertig. `three.min.js` muss im selben Ordner liegen (sonst wird es aus dem Netz geladen).

### GitHub Pages

1. Repository auf GitHub anlegen und den Inhalt dieses Ordners hochladen.
2. *Settings → Pages → Source: Deploy from a branch*, Branch `main`, Ordner `/ (root)`.
3. Nach kurzer Zeit läuft der Simulator unter `https://<benutzer>.github.io/<repo>/`.

Auf Android lässt sich die Seite im Chrome-Menü über „Zum Startbildschirm hinzufügen“ wie eine App ablegen.

## Hinweis

Vereinfachte Fahrdynamik und PZB-Logik. Ersetzt weder Signalbuch noch Ausbildung.

## Lizenz

MIT – siehe [LICENSE](LICENSE).

Enthält [three.js](https://threejs.org) r128 (`three.min.js`), © 2010–2021 three.js authors, MIT-Lizenz.
