# Führerstand DS 301

Lern- und Übungssimulator für den Führerstand: Signale nach DS 301 (Signalbuch der DB), PZB 90 und Sifa in 17 Übungsszenarien auf fiktiven Strecken und 5 Szenarien auf der AVG-Linie S4 nach Buchfahrplan. Läuft im Browser auf Android, iOS und am PC – ohne Installation, ohne Build. Streckenbild wahlweise in 3D (WebGL, three.js) oder 2D.

## Streckenbild 3D/2D

- **3D-Ansicht (Standard):** echte räumliche Szene mit three.js – Gleisachse aus den Bögen der Strecke, Schotterbett, Schwellen, Schienen, Weichenverbindungen, Bahnhofsgleise 3/4, Inselbahnsteige mit Dach, Haltepunkte mit Wartehäuschen, Empfangsgebäude, Oberleitung mit Masten, Tunnel mit Portal und Bezeichnungstafel, Bahnübergänge, Felder, Wälder, Dörfer, Innenstadt Heilbronn als Straßenbahnabschnitt (BOStrab), Gegenzüge, vorausfahrender Zug, wartende Fahrgäste, Nebel, Nacht mit Sternen und Spitzenlicht
- Signale und Tafeln sind dieselben Signalbilder wie in 2D (als Textur), Signallichter leuchten weit sichtbar
- Die Auflösung passt sich der Leistung des Geräts an
- **Licht und Himmel:** Sonne nach der Uhrzeit des Szenarios (Sommertag in Karlsruhe) mit Schatten von Bäumen, Masten, Häusern, Signalen, Zügen und dem eigenen Zug; Himmel mit Sonnenhof und ziehenden Wolken (je Szenario unterschiedlich bewölkt), Morgen- und Abendrot, Nebel und Nacht; glänzende Schienenköpfe
- **Texturen:** Schotter aus einzelnen Steinen mit Rostspur unter den Schienen, Betonschwellen mit Rippenplatten und Spannklemmen, Gras mit Halmen und Flecken, Asphalt mit Flickstellen und Rissen, Bahnsteigplatten, Fassaden mit Fensterrahmen, Läden und Markisen; großflächige Farbschwankungen verhindern sichtbare Kachelung – alles im Code gezeichnet, keine Bilddateien
- **Stadtbahn- und Straßenbahnwagen** nach Renderbildern: AVG GT8-100D/2S-M 898 (Zweisystem), AVG Bombardier ET 2010 (Zweisystem, blaue Faltenbälge) und VBK NET 2012 (Vossloh/Stadler Citylink) – mit Zielanzeige (Linie und Ziel), Nummer (ohne Firmenlogos), Türen, Fenstern mit Innenraum, Drehgestellen, Dachaufbauten und Einholm-Stromabnehmer. Sie fahren als Gegen-, Kreuzungs- und vorausfahrende Züge (AVG-Strecken in Doppeltraktion)
- **Fahrdynamik nach Fahrzeugdaten:** Masse, Anfahrzugkraft und Leistung (Zugkraft = min(F0, P/v)), Zugkraftaufbau, Fahrwiderstand A + B·V + C·V², Massenfaktor, Neigung aus Streckendaten (sobald vorhanden). Daten öffentlich (Hersteller, Fachpresse) oder geschätzt – in der Szenarioliste angezeigt (Masse, Leistung, Bremshundertstel, Bremsstellung) und mit Werten aus den Fahrzeugunterlagen ersetzbar
- **Druckluftbremse der DB-Züge:** Führerbremsventil (Fahrtstellung 5 bar, Bremsstufen bis 3,5 bar, Schnellbremsung entlüftet die Hauptluftleitung), Durchschlag der Bremse längs des Zuges (250 m/s), Bremszylinder je Zugabschnitt mit Füll- und Lösezeiten der Bremsstellung (P, G, ep), Klotzbremse mit geschwindigkeitsabhängiger Reibung, Magnetschienenbremse bei Schnellbremsung, elektrische Bremse der Lok; Manometer mit Zeigern für Hauptluftleitung und Hauptluftbehälter sowie Bremszylinder. Stadtbahn und Straßenbahn: elektrische Bremse mit Federspeicher, Gefahrbremse mit Magnetschienenbremse
- **Menü:** sichtbar sind die S-Linien der AVG (S 31, S4, Tram-Train, S1/S11) und die Straßenbahnlinien 1–5; die DB-Szenarien und DB-Züge sind ausgeblendet (im Code vorhanden)
- **Fahrzeug je Szenario:** DB-Strecken fahren mit DB-Zügen – RB mit Talent 2 (BR 442, Doppeltraktion), RE mit BR 146 und Doppelstockwagen, IC mit BR 101 und IC-Wagen, Güterzug mit BR 185 (Kessel-, Container- und offene Wagen), Rangierfahrt mit Rangierlok BR 363; S-Linien (S4, S 31, Tram-Train) mit Zweisystemwagen der AVG (GT8-100D/2S-M oder ET 2010, wählbar unter „Wagen“); Straßenbahnlinien 1–5 und S1/S11 nur NET 2012
- **Menü „Szenarien“ → DB-Züge:** Bilder aller DB-Züge mit Einsatz (Szenario oder Gegenzug), der Zug des laufenden Szenarios ist markiert
- **DB-Gegenzüge nach Bildvorlage:** Talent 2, BR 146 + Doppelstockwagen, IC2 (BR 146.5 + Twindexx mit Steuerwagen), IC (BR 101 + IC-Wagen), ICE 3 (nur auf Strecken ab 150 km/h) und Güterzüge mit BR 185; je Zug ein Texturatlas (Seitenwände, Bug, Stirn mit Frontscheibe und Leuchten), Drehgestelle mit Rädern, Puffer, Stromabnehmer bis zum Fahrdraht. Auf Straßenbahnlinien nur NET 2012, auf der S1/S11 nur NET 2012, auf S-Linien GT8/ET 2010
- **Straßenverkehr in der Stadt:** Autos fahren auf eigenen Spuren und weichen aus – Straßenbahnhaltestellen sind schmal (2,65 m) zwischen Gleis und Fahrbahn, im Straßenraum mit Haltestelleninsel und ausschwenkender Spur; an der Rampe des Stadtbahntunnels liegen die Spuren außerhalb der Stützwände und steigen zur Straßenebene, über dem Tunnel fährt der Verkehr weiter; beim Wechsel zwischen Rasengleis und Straßenraum mündet eine Seitenstraße; Querverkehr wartet, solange ein Gegenzug die Kreuzung belegt
- **Führerstand GT8-100D/2S-M** nach Foto (Wagen 920 B): geneigtes Instrumentenpult mit Federspeicher- und Notbremspilz, PZB-Leuchtmeldern (85, 70, 1000 Hz, 500 Hz, Befehl 40, Zwangsbremse, Federsp. angelegt), Batteriespannungsmesser, Tacho bis 120 km/h, Weichentastern, Türmeldern 1–4, Druckluftmanometer, Stromanzeigern und Anzeige (Uhrzeit, nächster Halt); Schalterleiste mit Batteriehauptschalter, Linienschütz, Stromabnehmer, Heizung, Klima, Beleuchtung, Blinker, Türen, Ansage, Lautsprecher, Indusi-wachsam-Knauf und Scheibenwischer; Schwanenhalsmikrofon und Funkhörer. Lampen, Zeiger und Schalter folgen dem Fahrzeugzustand. Der Fahrschalter links ist geschätzt (nicht auf dem Foto)
- **Führerstand Bombardier ET 2010** nach Fotos: gerundete Armaturentafel mit Blendschutz – links Display mit Softkeys (Wagenübersicht mit Türen und Bremsen), Instrumentendisplay (Tacho bis 100 km/h, Digitalanzeige mit zulässiger Geschwindigkeit, 12 Symbolleuchten: PZB, Befehl, Zwangsbremse, Hauptschalter, Türen, Federspeicher, Sifa, Halt, Bremse), Tastenfeld 4 × 4 mit Drehschlüsseln, Touch-Display mit heller Oberfläche (Fahrleitung, Stromabnehmer, Türen, Druckluft, Zugkraft/Bremse, nächster Halt), Hebel und zwei Not-Aus-Pilze; rechts Seitenpult mit Drehschaltern und Gerätesäule (Fahrgastinformation, Funkgerät, IBIS mit Linie und Ziel), Innenspiegel; links Seitenpult mit Fahr-/Bremshebel als Seitenstick (Kugelknauf, rote Lasche), Richtungswender, Kippschaltern, Tastern und Drehschaltern mit Schutzbügeln, Armlehne.
- **NET 2012 (Vossloh/Stadler Citylink)** nach VBK-Broschüre: Ein-Richtungs-Gelenkwagen aus 3 Wagenteilen (12,8 / 10,85 / 12,45 m, 37,2 m), 5 Doppeltüren nur auf der rechten Seite, hinten Rangierfahrerstand ohne Zielanzeige, Stromabnehmer auf dem Mittelteil, Achsfolge Bo'(2')(2')Bo', 80 km/h, 750 V =. Führerstand: hellgraues Pult mit schwarzer Tafel – links blaues Display (Geschwindigkeit, zulässige Geschwindigkeit, Uhrzeit, nächster Halt), Leuchttaster, runder Tacho, Taster und Drehschalter, rechts Display mit Fahrzeugübersicht (3 Wagenteile, Türen, Bremsen), Not-Aus; links Fahr-/Bremshebel mit Pilzknauf (Fahren · 0 · Bremsen · Gef. Bre.); rechts tiefes Seitenpult mit Energie-Display und Drehschaltern
- **Außenansicht** (Schalter „Außen“ oder Taste `V`): eigener Zug von außen, ziehen dreht um den Zug, Mausrad zoomt; im Tunnel bleibt die Kamera auf der Gleisachse
- **Grafikqualität** (Menü „Szenarien“ → Grafik): Automatisch (nach Gerät, senkt bei Bedarf), Niedrig (ohne Schatten), Mittel, Hoch
- **Gelände:** Hügel und Täler aus Rauschen, Bahnkörper mit Dämmen (1:1,6) und Einschnitten (1:1,5), Stützmauern in tieferen Einschnitten, Hügel über den Tunneln mit Voreinschnitt und Portalbauwerk, Flüsse mit Talaue und Eisenbahnbrücke (Überbau mit Gesimskappen, Geländer, Pfeilern, Widerlagern), Straßenüberführungen über Einschnitte. Gleisnah ein genaues Geländeband, weiter draußen Kacheln mit Detailstufen bis zum Horizont; Felder mit Furchen, Waldböden, Bahnhöfe, Übergänge und Stadt bleiben eben
- **Vegetation:** Laubbäume aus mehreren Kronenballen, Fichten in Stufen, Pappeln, Birken mit weißem Stamm, Büsche an Böschung und Feldrand, Hecken, Grasbüschel neben dem Gleis; Wälder auf Hügeln als Baum-Bildpunkte (sehr günstig zu zeichnen)
- **Details:** Oberleitung mit Tragseil, Hängern, Isolatoren und Fahrdraht im Zickzack, Mastfundamente; Hauptsignale mit Gehäuse, Blende, Steigleiter und Arbeitsbühne; Weichen mit Antrieb, Herzstück und Radlenker; Bahnübergänge mit Lichtzeichen (gelb → rot), Halbschranken und Fahrbahnmarkierung; Bahnsteige mit Leuchten, Bänken, Abfallbehältern und Zugzielanzeiger; in der Stadt Ampeln für Längs- und Querverkehr (abhängig vom Fahrsignal), Haltlinien, Mittellinien und Straßenleuchten
- **Nacht:** Fensterlicht in Häusern und Empfangsgebäuden, Leuchten an Bahnsteigen und Straßen mit Lichtflecken, Tunnelbeleuchtung, Lichthof um Signale, Lichtkegel der Scheinwerfer, Mond und Sterne
- **Wetter** (Menü „Szenarien“ → Wetter): Szenario, Klar, Dunst, Nebel, Regen (Regenstriche, Tropfen auf der Frontscheibe mit Scheibenwischern, nasser Asphalt) und Schnee (Flocken, verschneites Gelände, Dächer, Bäume und Schotter). Auf „Niedrig“ ohne Tropfen, Lichtkegel, Lichthöfe und Lichtflecke
- **2D-Ansicht:** Schalter „3D“ oben – für ältere Geräte; ohne WebGL startet automatisch 2D
- **Führerstand in 3D:** Pult mit Tacho (zulässige Geschwindigkeit als gelbe Marke), Manometern (Hauptluftbehälter, Bremszylinder), Fahrplanbildschirm, PZB-Leuchtmeldern, Fahrzeug-Leuchtmeldern (HS, Stromabnehmer, Kompressor, Türen, Sifa), Schalterreihe, beweglichem Fahr-/Bremshebel und Schnellbremstaster; Frontscheibe mit Wischern und Sonnenblende, **Seitenfenster** mit Schiebefenster und Außenspiegeln, Rückwand mit Tür; Pultbeleuchtung bei Nacht und im Tunnel; Wagenkasten schwankt leicht, Stöße an Weichen
- **Umschauen:** im Bild ziehen (Maus oder Finger), `←`/`→` bzw. `A`/`D` halten; Doppeltipp oder `C` zentriert
- **Bildschirmaufteilung:** Das Bedienpult unten nimmt 30 % der Bildschirmhöhe ein, der Streckenblick den Rest; Handy quer: Pult als Spalte rechts (30 % der Breite, scrollbar)
- **2D-Kabine:** in der 2D-Ansicht gezeichneter Fensterrahmen mit Pult; Schalter „Kabine“ blendet die Kabine aus

## Aufrüsten und Geräusche

- Jedes Szenario beginnt abgerüstet: **Motor starten** (Taste `M`) hebt den Stromabnehmer, schaltet den Hauptschalter ein und startet die Hilfsbetriebe – ohne Hauptschalter keine Zugkraft
- Druckluft: Kompressor schaltet bei 8 bar ein und bei 10 bar ab, jede Bremsung verbraucht Luft
- Geräusche (Web Audio, nach dem Vorbild eines Drehstrom-Triebwagens nachgebildet): Hubantrieb des Stromabnehmers, Hauptschalter, Lüfter, Kompressor mit Abblasen, Pulswechselrichter mit gestuften Taktfrequenzen („Singen“ beim Anfahren und elektrischen Bremsen), Getriebe, Rollgeräusch, Fahrtwind, lauter im Tunnel, Achsstöße an Weichen und Bahnübergängen, Bremsluft und Lösen, Bremsenquietschen kurz vor dem Halt, Türwarnton und Türen, Zweiklang-Signalhorn, Vorbeifahrt von Gegenzügen

## Straßenbahn Karlsruhe (Szenarien 31–36)

Stadtlinien 1–5 und 8 mit der Haltestellenfolge aus dem KVV-Liniennetzplan (Stand 2023). Abstände, Gleislage, Kreuzungen, Weichen und Abschnitte (Rasengleis / Straßenraum) sind angenommen. Fahrzeug Straßenbahn (37 m, 70 km/h), keine PZB, Fahren auf Sicht nach BOStrab, Glocke statt Pfeife.

| Nr. | Linie | Strecke |
|---|---|---|
| 31 | 1 | Neureut-Heide – Kunstakademie – Mühlburger Tor – Stadtbahntunnel (Europaplatz – Durlacher Tor) – Durlacher Allee – Durlach Turmberg |
| 32 | 2 | Knielingen Nord – Kaiserallee – Mühlburger Tor – Europaplatz – Südweststadt – Hauptbahnhof (Bahnhofsvorplatz) – Tunnel (Kongresszentrum – Durlacher Tor) – Durlach – Wolfartsweier Nord |
| 33 | 3 | Rappenwört – Daxlanden – Entenfang – Kaiserallee – Europaplatz – Karlstor – Hauptbahnhof (Bahnhofsvorplatz) – Tivoli – Rüppurrer Tor – Kronenplatz – Durlacher Tor – Hauptfriedhof – Rintheim |
| 34 | 4 | Oberreut Badeniaplatz – Weinbrennerplatz – Europaplatz – Kriegsstraße – Durlacher Tor – Hauptfriedhof – Waldstadt Europäische Schule |
| 35 | 5 | Rheinhafen – Entenfang – Kühler Krug – Kriegsstraße – Rüppurrer Tor – Ostendstraße – Schloss Gottesaue – Durlacher Allee – Durlach Bf |
| 36 | 8 | Durlach Turmberg – Schlossplatz – Friedrichschule – Auer Straße – Gritznerstraße – Aue – Wolfartsweier Nord |

## Albtalbahn S1/S11 (Szenarien 41–43)

Linien S1 und S11 der AVG mit allen Haltestellen und Kilometern nach der AVG-Fahrplantabelle (Stand 2023):

| Nr. | Strecke | Länge |
|---|---|---|
| 41 | S1 Hochstetten – Karlsruhe – Ettlingen – Busenbach – Bad Herrenalb (52 Halte) | 45,5 km |
| 42 | S11 Hochstetten – Karlsruhe – Ettlingen – Busenbach – Ittersbach Rathaus (55 Halte) | 44,8 km |
| 43 | S1 Albtal: Ettlingen Stadt – Bad Herrenalb | 18,5 km |

- **Hardtbahn** Hochstetten – Haus Bethlehem nach EBO mit H/V-Signalen und PZB, zweigleisig bis auf 500 m bei Neureut, Hardtwald zwischen Eggenstein und Neureut
- **Karlsruhe nach BOStrab** ab Haus Bethlehem: Kurt-Schumacher-Straße, Moltkestraße, Yorckstraße, Mühlburger Tor, Stadtbahntunnel der Kombilösung (Europaplatz, Marktplatz Kaiserstraße und Pyramide, Ettlinger Tor, Kongresszentrum) mit Rampe und Portal an beiden Enden, Ettlinger Straße, Hauptbahnhof (Vorplatz), Albtalbahnhof, Rüppurr auf Sicht mit Fahrsignalen an den Kreuzungen
- **Albtalbahn** ab Rüppurr Battstraße mit H/V-Lichtsignalen, Kilometrierung ab Albtalbahnhof (km 0,0), nach Ittersbach ab Busenbach; ab Busenbach eingleisig mit Kreuzungsbahnhöfen (Ausweichgleis mit Bahnsteig, Zugkreuzungen in Fischweier und Frauenalb-Schielberg bzw. Reichenbach und Spielberg), S11 in Busenbach abzweigend (Hp 2)
- **Fahrzeuge:** S11 nur NET 2012 der AVG (Zweirichtungswagen, Führerstand und Zielanzeige an beiden Enden, Türen auf beiden Seiten, 80 km/h); auf der S1 GT8 oder NET 2012; Gegen- und Kreuzungszüge auf der Albtalbahn NET 2012 und GT8
- **Albtal:** die Alb begleitet die Strecke ab Ettlingen und wechselt an mehreren Albbrücken die Seite, Talaue und bewaldete Hänge; die S11 steigt hinter Busenbach aus dem Tal
- Bahnübergänge technisch gesichert (Lichtzeichen, Halbschranken), einzelne mit Pfeiftafel Bü 4
- Angenommen sind Geschwindigkeiten (Hardtbahn bis 80, Stadt 40–60, Albtal 70, Bögen 50 km/h), Signalstandorte, Bögen, Lage der Brücken und Bahnübergänge; Fahrzeiten aus der Simulation abgeleitet (Gesamtfahrzeit wie im Fahrplan, etwa 88 min)

## Tram-Train (Szenario 23, Beispielstrecke)

- **EBO-Abschnitt** mit Ks-Signalen, PZB und Lf, dann **Systemwechsel 15 kV ~ / 750 V =**: El 1v im halben Bremswegabstand vor El 1 (Fahrschalter auf 0), El 1 (spätestens hier Hauptschalter aus), Systemtrennstelle ohne Spannung antriebslos durchrollen, El 2 mit Spannungstafel „750 V =“ (weiße Rechtecktafel wie an den Systemtrennstellen der Stadtbahn Karlsruhe) – Hauptschalter erst ein, wenn der Stromabnehmer das El 2 passiert hat. Die El-Tafeln hängen vorn an den Fahrleitungsmasten und sind nach Ril 301 gezeichnet (blaue, auf der Spitze stehende Tafel, weiß und schwarz umrandet; El 1v zwei Rechtecke, El 1 zerlegtes U, El 2 geschlossenes U). Fehler: mit eingeschaltetem Hauptschalter am El 1 oder in der Trennstelle, Einschalten vor El 2; liegen bleiben in der Trennstelle beendet die Fahrt
- **So 2** – Ende der Zugsicherung, ab hier **BOStrab**: Rasengleis mit Alleebäumen und Fahrbahnen, Straßenbahn in der Straße mit Autoverkehr, Häuserzeilen
- **Fahrsignale** F 0 / F 1 / F 4 mit Anforderungsanzeige „A“ (St 9); an der Haltlinie warten, bis F 1 kommt – der Querverkehr fährt solange
- **Weichensignale** W 11 (verschlossen) und W 1 (nicht verschlossen, höchstens 15 km/h), **G-Signale** G 1a / G 2a / G 4, **Läutetafel Sh 4** (Glocke statt Pfeife), Haltestellen mit Sh 7
- **Stadtbahntunnel** unter der Straße: Rampe zwischen Stützwänden hinab, Portal unter der Fahrbahn, darüber Straße, Häuser, Bäume, Leuchten und Verkehr; H-/V-Signale, Ausfahrsignal nach Haltezeit, H 2 (40 km/h), unterirdische Haltestellen mit Zugängen (U-Schild) auf dem Gehweg
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
  - Fahrzeug je Szenario: DB-Zug (PZB 90 nach Ril 483) oder AVG-Stadtbahn auf S-Linien (PZB 90 Version AVG nach Schaublatt Betriebszustände: Zugart O fest, 100 km/h, Frühhalt VÜ 3 / Späthalt VÜ 2, nach 500 Hz 15 s unter 30 km/h → 25 km/h, Startprogramm 550 m)
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
| 24 | S4 | S4 Übung: GPA und Bahnübergang | Geschwindigkeitsprüfabschnitt am Lf 6 „8“ (Einschaltmagnet, Messstrecke, 1000-Hz-Wirkmagnet, Ausschaltmagnet), Gefahr am Bahnübergang |
| 51 | S4 PZB | Halt erwarten (500 Hz) | Ks 2, 1000 Hz, 500 Hz vor dem Esig Bauerbach: 65 → 45 km/h auf 153 m, Halt vor Hp 0 |
| 52 | S4 PZB | Restriktiv bei der Zugkreuzung | Flehingen: Stand über 15 s → 45/25 km/h, AVG-Regel 500 Hz + 15 s unter 30 km/h → 25 km/h, richtig befreien |
| 53 | S4 PZB | Startprogramm und Späthalt | Startprogramm 45/25 (AVG 550 m), Halt in Bt-Wannenweg vor Bksig 21 mit Hp 0 |
| 54 | S4 PZB | Zs 3 „3“ vor Eppingen | Zs 3v, 500 Hz 150 m vor dem Esig, 30 km/h im Weichenbereich |
| 55 | S4 PZB | Ersatzsignal Zs 1 | Esig Wössingen gestört, Befehl über 2000 Hz mit höchstens 40 km/h |
| 56 | S4 PZB | Vorsichtsignal Zs 7 | Befehl, Fahrt auf Sicht bis Bksig 7, stehender Zug im Abschnitt |
| 57 | S4 PZB | Gegengleis mit Zs 8 | Jöhlingen West – Wössingen auf dem Gegengleis, 2000 Hz an der Ne 1 |
| 58 | S4 PZB | Abfahrt nur bei Fahrt | Asig Bretten bleibt auf Hp 0 über die Abfahrtszeit hinaus |
| 59 | S4 PZB | Signal fällt auf Halt | Bksig 702 fällt 420 m vor dem Zug auf Halt: Schnellbremsung, Fdl melden |
| 60 | S4 PZB | Gestörte Streckeneinrichtung | 2000 Hz am Fahrt zeigenden Bksig 3: Zwangsbremsung ohne Verschulden, melden |
| 61 | S4 PZB | Befreien zur falschen Zeit | Esig Sulzfeld kommt erst spät in Fahrt; vorzeitiges Befreien → 500 Hz → Zwangsbremsung |

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
| `K` | Freiflug „Erkunden“ ein/aus |

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

## Karlsruhe Hbf (Szenario 50, Vorschau)

Bahnhof nach Vorbild für die künftigen Linien S8, S31 und S32: fünfschiffige Bahnsteighalle (1913, August Stürzenacker) mit verglasten Flanken, Laterne im Scheitel, Bogenbindern alle 9 m, Stützen zwischen den Gleispaaren und Glasschürzen an den Hallenenden mit Schriftzug „KARLSRUHE HBF“; fünf Inselbahnsteige unter der Halle (Gleis 1–10), zwei weitere mit Bahnsteigdächern (Gleis 11–14), Zugzielanzeiger mit Uhr und Gleisnummern, Stationsschilder, Pendelleuchten, Bänke, Weichenfächer an beiden Enden, Fahrleitung über allen Gleisen, Empfangsgebäude mit Kuppelhalle, abgestellte Stadtbahnwagen. Der Bahnhof wird über die Station (`hbf:{gleis, dir}`) eingebunden; das eigene Gleis und die Fahrtrichtung (West/Ost) legen die Lage aller Gleise fest. Szenario 50: Probefahrt Karlsruhe-Durlach – Karlsruhe Hbf Gleis 8.

## Bahnhofsvorplatz Karlsruhe Hbf (Linien 2 und 3, Szenario 50)

Nach Fotos und den Visualisierungen des Umbaus: gepflasterter Platz mit vier Straßenbahngleisen und drei Bahnsteigen (Glasdächer auf schlanken Stützen, gläserne Rückwände an den Sitzgruppen, Bänke, rote Haltestellenmaste mit „H“, Abfahrtsanzeiger, Fahrkartenautomaten), hohe Gittermaste mit Leuchtenkronen und Querseilen, Leuchtenmaste, Kiosk, Fahrräder vor dem Westflügel, Fahnen, Bäume und Fahrgäste.
Empfangsgebäude: Mittelbau mit steilem Giebel (vier Reliefpfeiler mit Figuren, Uhr, fünf hohe Sprossenfenster), Eckpfeiler mit Ornamentblöcken, Vordach mit sechs gläsernen Oberlichtern und Schriftzug „Hauptbahnhof“, Kupferdach mit Glasflächen und dahinter die Kuppelhalle als Kupfertonne mit Laterne; Flügel mit zwei Geschossen, Mansarddach und Gauben, Eckpavillons an den Enden. Gegenüber die Häuserzeile am Bahnhofplatz (Hotelbauten mit Schieferdach, Arkadenhäuser mit rotem Mansarddach, Kolonnade mit Fahnen, Bürohaus). Nachts leuchten Eingänge und Uhr.
Derselbe Platz steht in Szenario 50 hinter dem Empfangsgebäude nördlich der Bahnsteighalle (um 180° gedreht, Gelände dort eben, Straßenbahngleise mit Fahrleitung laufen beidseits als Straße weiter). Im Freiflug („Erkunden“) lässt sich von der Halle über das Gebäude auf den Platz fliegen.

## Freiflug „Erkunden“

Strecke ohne Zug ansehen: „Erkunden“ in der Kopfleiste (Taste `K`) oder „Strecke ansehen“ unter jeder Szenariokarte. Die Fahrt ist währenddessen angehalten und geht danach an derselben Stelle weiter (bei laufender Fahrt mit Pause). Das Streckenbild füllt den Bildschirm, die Abschnitte werden um den nächsten Streckenpunkt der Kamera gebaut.

| Bedienung | Smartphone | Rechner |
|---|---|---|
| Fliegen | Steuerkreis links | `W` `A` `S` `D` / `↑` `↓` |
| Umschauen | im Bild ziehen | Maus ziehen, `←` `→` drehen, `R` `F` neigen |
| Höher / tiefer | ▲ / ▼ | `E` oder Leertaste / `Q` |
| Tempo | „Tempo“ (0,3× – 8×) | `+` / `−`, `Shift` dreifach |
| Vor / zurück in Blickrichtung | – | Mausrad |
| Hinfliegen | Karte oben rechts antippen | Karte anklicken, `M` Ausschnitt (Strecke / 4 km / 1 km), `N` Karte ein/aus |
| Halt anspringen | „Springen zu …“ | dto. |
| Augenhöhe im Gleis | „Ins Gleis“ | `G` |
| Beenden | „Beenden“ | `Esc` oder `K` |

Die Geschwindigkeit wächst mit der Höhe über Grund; die Kamera bleibt mindestens 1,6 m über dem Gelände, im Tunnel über den Schienen, höchstens 1,8 km neben der Strecke.

## Liniennetz Karlsruhe (gemeinsame Karte)

Die Stadtlinien 1, 2, 3, 4, 5 und 8 liegen in einer Karte. Grundlage ist der Liniennetzplan: Lage jeder Haltestelle aus dem Plan (11,5 m je Bildpunkt, Ursprung Europaplatz), Linienführung als Polygonzug mit Kreisbögen an den Ecken (an Haltestellen eng, an Abzweigen mittel, an Stützpunkten weit). Gemeinsame Abschnitte laufen über dieselben Punkte und Knoten; jede Linie fährt auf dem rechten Gleis (2,1 m neben der Achse), Linien in Gegenrichtung (z. B. 1 und 8 in Durlach) nutzen das andere Gleis.

- Umsteigehaltestellen: Mühlburger Tor, Yorckstraße, Schillerstraße, Europaplatz, Karlstor/Bundesgerichtshof, Mathystraße, Otto-Sachs-Straße, Ebertstraße, Hauptbahnhof, Poststraße, Ettlinger Tor, Rüppurrer Tor, Durlacher Tor, Karl-Wilhelm-Platz, Hauptfriedhof, Marktplatz/Kronenplatz (U), Gottesauer Platz, Tullastraße, Weinweg, Untermühlstraße, Auer Straße, Gritznerstraße bis Wolfartsweier, Friedrichschule, Schlossplatz, Turmberg.
- Andere Linien im Bild: eigene Gleise (Rillenschienen bzw. Rasengleis), Straßenraum, Fahrleitung, Haltestellen mit Bahnsteigen an beiden Gleisen, Häuserzeilen; gemeinsame Abschnitte zeichnet nur die eigene Strecke, unterirdische Abschnitte und Rampen des Stadtbahntunnels werden ausgelassen.
- Kreuzungen zweier Linien an der Oberfläche (Entenfang, Weinbrennerplatz, Rüppurrer Tor) mit Fahrsignal vor der Kreuzung; zufällige Straßenkreuzungen in der Nähe entfallen.
- Enge Bögen mit Geschwindigkeitsbeschränkung nach v ≈ 4,6·√R (Lf 6/Lf 7 als G-Tafeln).
- Zwischen den Linien Blockbebauung (Raster 76 m, nach der nächsten Strecke ausgerichtet, in der Innenstadt höher); im Stadtgebiet keine Felder und kein Wald.
- Freiflug: Karte mit dem ganzen Netz in den Linienfarben; beim Überfliegen einer anderen Linie wird deren Strecke aufgebaut (Kamera bleibt an ihrem Ort), beim Beenden geht es mit der ursprünglichen Fahrt weiter.
- Neu: Mathystraße auch bei Linie 2 und 5 (nach dem Netzplan). Fahrpläne aller Stadtlinien neu berechnet.

### S1/S11 im Liniennetz

Der Stadtabschnitt der S1/S11 (BOStrab, km 12,85–23,6) liegt in derselben Karte: Haus Bethlehem, Kurt-Schumacher-Straße, August-Bebel-Straße, Knielinger Allee/Städt. Klinikum, dann gemeinsam mit Linie 2 Moltkestraße – Yorckstraße – Mühlburger Tor, im Stadtbahntunnel mit Linie 1/2 Europaplatz – Marktplatz (Kaiserstraße, Pyramide) – Ettlinger Tor – Kongresszentrum, wieder gemeinsam mit Linie 2/3 Augartenstraße – Poststraße – Hauptbahnhof (Vorplatz), ab dem Knoten westlich des Vorplatzes nach Süden Albtalbahnhof – Dammerstock – Rüppurr – Battstraße. Hardtbahn (Hochstetten – Neureut) und Albtalbahn (Ettlingen – Bad Herrenalb/Ittersbach) behalten ihre Bögen und sind an den Stadtabschnitt angehängt (gedreht und verschoben, sodass sie in dessen Richtung ankommen). Die Kilometrierung wird im Stadtabschnitt zwischen den Haltestellen auf die Weglänge der Karte abgebildet.

Am Bahnhofsvorplatz fährt die S1/S11 westwärts auf dem Gegengleis der Linien 2 und 3 und hält am nördlichen Bahnsteig; der Vorplatz wird dafür um 180° gedreht aufgebaut, das Empfangsgebäude liegt links (Süden). Fahrpläne der Szenarien 41 und 42 neu berechnet.

## S4-Übung: Geschwindigkeitsprüfabschnitt und Bahnübergang (Szenario 24)

Grötzingen Oberausstraße – Wössingen nach Buchfahrplan. Lage des GPA und der beiden Bahnübergänge angenommen (Übung).

- **GPA vor dem Esig Jöhlingen** (100 → 80 km/h): Lf 6 „8“ bei km 5,05, Lf 7 „8“ am Esig km 6,2.
  Aufbau wie im WBT: **Einschaltmagnet** (km 4,85) – **Messstrecke 200 m** – **1000-Hz-Wirkmagnet am Lf 6** – **Ausschaltmagnet** 50 m dahinter.
  Der Einschaltmagnet startet ein Zeitglied (Prüfzeit = 200 m bei 95 km/h ≈ 7,6 s). Erreicht der Zug den Wirkmagneten,
  solange die Prüfzeit läuft, war er im Mittel schneller als 95 km/h: 1000-Hz-Beeinflussung (Wachsam binnen 4 s, danach 1000-Hz-Überwachung).
  Ist die Zeit abgelaufen, ist der Magnet unwirksam. Der Ausschaltmagnet stellt die Anlage zurück.
  Mit Lernhilfe zeigen die Magnetschilder den Zustand: „GPA Ein“, „GPA 1000 Hz · 3,2 s“ (Zeitglied läuft), „GPA unwirksam“, „GPA Aus“.
- **Gefahr am Bahnübergang:** An einem der beiden technisch gesicherten Bahnübergänge (km 6,45 hinter dem Jöhlinger Tunnel oder km 8,55 vor Wössingen,
  zufällig) umfährt ein Pkw die geschlossene Halbschranke und bleibt im Gleis liegen. Richtig: Achtungssignal Zp 1 (Taste H), sofort Schnellbremsung (SB),
  nach dem Halt das gefährliche Ereignis dem Fdl melden (Taste Fdl). Der Pkw-Fahrer bekommt den Motor wieder an, wenn der Zug steht; danach Weiterfahrt auf Sicht
  mit höchstens 20 km/h über den Bahnübergang. Fehler: kein Achtungssignal, Weiterfahrt ohne Meldung; Zusammenstoß bricht die Fahrt ab.
  Wer erst reagiert, wenn der Pkw schon steht, schafft es bei 100 km/h nur noch mit Schnellbremsung.

## Eine Karte für alle Szenarien

Alle sichtbaren Szenarien liegen in einer gemeinsamen Karte (Koordinaten des Liniennetzplans):

- **Straßenbahnlinien 1–5, 8** und **S1/S11** wie bisher im Liniennetz.
- **S4**: Anbindung in **Durlach Bf** am Ende der Linie 5 über Hubstraße und Grötzingen Bahnhof zur Oberausstraße (Grötzingen Bahnhof = km 0,0), dann Kraichgaubahn über Bretten, Eppingen und Heilbronn bis Öhringen. Die Bögen sind für die ganze Strecke einmal festgelegt (grob nach der echten Lage der Orte) – die Szenarien 17–21 und 24 nehmen ihren Ausschnitt daraus. Bahnübergänge, GPA und Gelände sind dadurch in jedem S4-Szenario gleich.
- **Szenario 50**: DB-Strecke von Karlsruhe-Durlach zur Bahnsteighalle des Hauptbahnhofs (Gleis 8), genau hinter dem Bahnhofsvorplatz der Linien 2 und 3.
- **Szenarien 16 und 23** (Beispielstrecken, fiktiv): zweigen in Durlach bzw. Grötzingen ab.
- Gelände: fester Zufallswert für die ganze Karte; Bäume, Häuser und Wald entlang der Strecke richten sich nach der Lage auf der Strecke, nicht nach dem Szenario.

Freiflug: Die Karte oben rechts zeigt in jedem Szenario dasselbe Netz (Knopf: Netz, Strecke, 4 km, 1 km). Fliegt man zu einer anderen Strecke oder über das Ende des Abschnitts hinaus, wird der passende Abschnitt aufgebaut – die Kamera bleibt an derselben Stelle.

Leistung: Schilder und Signaltafeln werden ohne Rücklesen aus der Grafikkarte ausgemessen (das hat beim Aufbau der Abschnitte mehrere Sekunden gekostet), der Aufbau im Freiflug ist je Bild zeitlich begrenzt, Gelände nach Sprüngen wird über mehrere Bilder nachgeladen. Die 2D-Ansicht stürzte mit einem vorausfahrenden Zug im Bild ab – behoben.

## S4: PZB-Übungen mit 500 Hz und 2000 Hz (Szenarien 51–61, Zugart O)

Alle Übungen laufen auf echten Abschnitten der S4 mit Zugart O (AVG: O fest). Überwachung nach PZB 90: 1000 Hz 165 → 85 km/h in 23 s, 500 Hz am Magneten 65 km/h und 153 m danach 45 km/h, restriktiv 45/25 km/h, Startprogramm 45/25 km/h (AVG bis Befreien oder 550 m), 2000 Hz am Hp 0 sofort Zwangsbremsung, mit Befehl (Zs 1, Zs 7, Zs 8) höchstens 40 km/h.

Neu in der Simulation dafür: Haltfall (Signal fällt vor dem Zug auf Halt; Zwangsbremsung zählt nicht als Fehler, wenn binnen 3 s mindestens voll gebremst wurde), Signal kommt erst bei Annäherung in Fahrt, gestörter 2000-Hz-Magnet am Fahrt zeigenden Signal (Meldung an den Fdl), Startprogramm bei Fahrtbeginn, stehender Zug im Abschnitt, der erst weiterfährt, wenn man dahinter steht.

