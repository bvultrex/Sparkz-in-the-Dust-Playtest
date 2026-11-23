# Changelog

Alle wesentlichen Änderungen an den Playtest-Paketen von **Sparkz in the Dust**.

Das Format folgt [Keep a Changelog](https://keepachangelog.com/de/1.1.0/). Die neueste Version steht oben.

Numerische Dateiversionen (`0.1.x`) gibt es erst ab dem Paket **Lebendige Ausrüstung** (0.1.38) vom 21.11.2026. Ältere Playtests sind in `BUILD.json` bzw. `LIESMICH.txt` mit Datums- und Themennamen sowie einem Koop-Protokoll bezeichnet. Diese Bezeichnungen werden hier übernommen; es werden keine `0.1.x`-Nummern nachträglich vergeben.

Quellen sind die lokalen Playtest-Pakete unter `releases/` (jeweils `LIESMICH.txt`, `BUILD.json`, gelegentlich `AENDERUNGEN.txt`), die zugehörigen Zip-Prüfsummen, das lokale Projekt-Git und – für 0.1.40 – das GitHub-Release `v0.1.40`. Daten ohne Uhrzeit stammen aus dem in der Quelle genannten Kalendertag. Uhrzeiten sind in **Europe/Warsaw**, sofern eine Zeitangabe vorliegt.

## [0.1.42] - 2026-11-23

**Playtest 0.1.42 – Controller & Boss-Trophäen.** Dateiversion `0.1.42.0`, Koop-Protokoll 41, Windows x64, exportiert mit Godot 4.7.2.

- Paket: `Sparkz_in_the_Dust_Playtest_2026-11-23_Controller.zip`
- Quellen: `LIESMICH.txt` und `BUILD.json` des Pakets (23.11.2026)
- **Nicht kompatibel** mit 0.1.41 oder älteren Builds (Protokoll 41 gegenüber Protokoll 40 und darunter)
- SHA256 der Zip: `7beb2e1eb1fd6dd2774e71fc6e5a71a38f57786734e026aa810ac556817d602c`

### Hinzugefügt

- Set-Boni für vollständige Rüstungssets, einschließlich Gruppen-Boni im Koop.
- Boss-Trophäen: Bosse lassen je Kill ein noch fehlendes Teil fallen. In der Arena beträgt die Chance 25 %. Bosse erscheinen erneut und tragen einen Namensbalken.
- Controller-Unterstützung für Xbox-Controller und Steam Deck: Analog bewegen, mit dem rechten Stick zielen, Menüs und Bunker-Editor ohne Maus. In den Einstellungen gibt es die Anzeige-Optionen „Pixelgenau (Letterbox)“ und „Bildschirm füllen“ (auf 1280×800/16:10 wird Füllen automatisch vorgeschlagen). In Textfeldern öffnet Steam+X die Bildschirmtastatur.
- Steam Deck: In Steam unter „Nicht-Steam-Spiel hinzufügen“ die Windows-EXE einbinden und den Windows-Build mit Proton starten.

### Geändert

- Koop-Protokoll und EOS-Bucket stehen auf 41 (`CHOBUTAI-41-`). Clients mit 0.1.41 oder älter finden sich nicht mehr.
- Wächter schießen im Echtzeitkampf 25 % langsamer.
- Inventarnamen nutzen Seltenheitsfarben und lassen sich nach Seltenheit oder Kategorie sortieren.

### Behoben

- Questbelohnungen vom Auftragbrett konnten mehrfach abgeholt werden.
- Ausgestellte Gegenstände im Bunker waren nicht zuverlässig als Besitz erkennbar und einlagerbar.
- Schilde wurden nach dem Wechsel von einer Zweihandwaffe nicht wieder angelegt.
- Die Sitzpose am Lagerfeuer und auf Bänken schwebte oder saß in der Feuerstelle.
- Dasselbe QTE-Minispiel konnte direkt hintereinander wiederholt werden.
- Nahkampftreffer am Umkehrpunkt des Schwungs wurden nicht zuverlässig erkannt.
- Ein einziges Starter- oder Reservewaffen-Exemplar ließ sich nicht zwischen den Waffenplätzen verschieben.

### Hinweise

- Das Paket bleibt eine Testversion. Offen ist unter anderem der Beitritt eines zweiten Rechners über verschiedene Internetanschlüsse.
- Alte Spielstände bleiben lesbar. Das Zip enthält keine persönlichen Spielstände.

## [0.1.41] - 2026-11-22

**Playtest 0.1.41 – Rüstungsarsenal.** Dateiversion `0.1.41.0`, Koop-Protokoll 40, Windows x64, exportiert mit Godot 4.7.2.

- Paket: `Sparkz_in_the_Dust_Playtest_2026-11-22_Ruestungsarsenal.zip`
- Quellen: `LIESMICH.txt` und `BUILD.json` des Pakets (22.11.2026)
- **Nicht kompatibel** mit 0.1.40 oder älteren Builds (Protokoll 40 gegenüber Protokoll 38 und darunter)
- SHA256 der Zip: `3e2beb768213b2ec20475aa0e9eb9719a6c8696e1b4dbd9735bc07d69172f26a`

### Hinzugefügt

- Neue Standard-Rüstungssets im normalen Beute-Pool: Leitungsdienst, Aufbruchsdienst, Saatpfleger, Quartierwacht, Fadenpegel, Absperrtrupp, Leitungsprobe, Trassendeckung, Ringpeiler, Ringbrecher, Wundmoos, Rostwehr, Rostgewölbe, Sperrmedizin, Sentinelpanzer und der legendäre Filterthron.
- Die Relikt-Rüstungen sind jetzt fünf Sets. Jedes Teil droppt sehr selten (0,3 % je besiegtem Dungeon-Gegner). Neu bzw. jetzt ebenfalls in diesem seltenen Wurf: das Kernsystem der Labormatriarchin und das Schweigesiegel der stillen Leitung.
- Waffen-Upgrade-Auswahl pro Instanz in der Basislager-Werkstatt.
- Weitere Sets folgen.

### Geändert

- Der Playtest läuft auf Godot 4.7.2 (bisher 4.4.1). Renderer bleibt Compatibility.
- Koop-Protokoll und EOS-Bucket stehen auf 40 (`CHOBUTAI-40-`). Clients mit 0.1.40 oder älter finden sich nicht mehr.

### Behoben

- Ein Relikt-Code konnte in neue Spiele und andere Speicherplätze sickern.

### Hinweise

- Das Paket bleibt eine Testversion. Offen ist unter anderem der Beitritt eines zweiten Rechners über verschiedene Internetanschlüsse.
- Alte Spielstände bleiben lesbar. Das Zip enthält keine persönlichen Spielstände.

## [0.1.40] - 2026-11-21

**Playtest 0.1.40 – Dev-Konsole.** Dateiversion `0.1.40.0`, Koop-Protokoll 38, Windows x64, exportiert mit Godot 4.4.1.

- Paket: `Sparkz_in_the_Dust_Playtest_2026-11-21_Dev-Konsole.zip`
- Quellen: `LIESMICH.txt` und `BUILD.json` des Pakets; lokaler Release-Commit `8815cab` (21.11.2026, 23:46 Uhr); GitHub-Tag und Release `v0.1.40` (veröffentlicht 22.11.2026, 00:02 Uhr Europe/Warsaw)
- Kompatibel mit 0.1.39 (Protokoll 38), **nicht** mit 0.1.38 oder älter
- SHA256 der Zip: `44f28ce345f87a26a66022ee0c8a4966e8076954365ae4f8c70507361ed3a090`

### Hinzugefügt

- Entwicklerkonsole, Taste `^` (Esc schließt ebenfalls). Befehle: `player.add.item`, `player.add.level`, `player.add.xp`, `player.set.godmode`, `list.items`, `help`, `clear`. Statt `player` auch `me` / `p1`, im Koop `p2`–`p4`, `all` oder der Charaktername. Im Koop darf nur der Host Godmode setzen (auch für alle); Verbrauchsitems kann der Host an andere geben. Ausrüstung, Möbel, Level und XP nur für den eigenen Spieler.

### Geändert

- Laut `LIESMICH.txt` bleiben Spielstand, Inhalt und Koop-Protokoll gegenüber 0.1.39 unverändert. Die GitHub-Release-Notes zu 0.1.40 wiederholen zusätzlich die Fixes aus 0.1.39 (siehe dort).

## [0.1.39] - 2026-11-21

**Lebendige Ausrüstung – Fix-Build.** Dateiversion `0.1.39.0`, Koop-Protokoll 38.

- Paket: `Sparkz_in_the_Dust_Playtest_2026-11-21_Lebendige-Ausruestung-Fix.zip`
- Quellen: `LIESMICH.txt` und `BUILD.json`; Release-Commit `e1547a4` (21.11.2026, 22:31 Uhr Europe/Warsaw)
- Nicht kompatibel mit 0.1.38 (Protokoll 37) oder älteren Builds
- SHA256 der Zip: `708e811827071d89ec3cd610c64351b8b1a8b576ff813a32fc1ddcb12d81db22`

### Geändert

- Koop-Protokoll und EOS-Bucket stehen auf 38, passend zu den sechs neuen Rüstungs-IDs. Alte und neue Clients finden sich nicht mehr.

### Behoben

- Speichern unter Windows: Beim Überschreiben eines Spielstands wird die Umbenennung kurz erneut versucht, wenn die Datei gerade gesperrt ist.
- Speicherlecks beim Beenden behoben (Kampagnen-Controller und Aufräumen im Koop-Revive-Ablauf).
- Der Ausstellungsslot für Rüstung in der Wohnungs-Vorschau heißt korrekt `armor_head`.

## [0.1.38] - 2026-11-21

**Lebendige Ausrüstung.** Dateiversion `0.1.38.0`, Koop-Protokoll 37.

- Paket: `Sparkz_in_the_Dust_Playtest_2026-11-21_Lebendige-Ausruestung.zip`
- Quellen: `LIESMICH.txt` und `BUILD.json` (LIESMICH 21.11.2026, 16:28 Uhr Europe/Warsaw)
- SHA256 der Zip: `de76b8f3b0ccdd8531089adc0eccc889f30a7f654927705ab27cf4589a1fcf87`

### Hinzugefügt

- Sechs ausrüstbare 3D-Teile mit beweglichen Baugruppen: Rußfänger (Rücken), Glühmotten-Habitat (Rücken), Wartungskrabbe (Schultern), Schachtspäher-Helm (Kopf), Kolbenmanschetten (Arme), Federläufer-Schienen (Beine). Animationen sind kosmetisch; die passiven Werte gelten normal. Die Glühmotten nutzen die vorhandene Begleiter-Aktion und erzeugen kein zusätzliches Licht.

### Hinweise

- Das Paket nennt außerdem als bereits enthalten: Relikt-Rüstungen, Arena-Rückreise, Rüstungspuppe, persönliche Quartiere, Möbel-Editor, Tag/Nacht, Ereignisse und UI-Polish. Wann das UI-Polish erstmals in einem eigenen Playtest erschien, ist aus den vorliegenden Paketen nicht ersichtlich.
- Alte Spielstände und der bisherige Einstellungsordner bleiben lesbar.

## [2026-11-20-Relikt-Icon-Update] - 2026-11-20

Relikt-Update mit eigenem App-Icon. Koop-Protokoll 37 (wie das vorangehende Relikt-Update). Keine numerische Dateiversion.

- Paket: `Sparkz_in_the_Dust_Playtest_2026-11-20_Relikt-Icon-Update.zip`
- Quellen: Inhalt der Zip (`BUILD.json` mit `"update": "Relikt-Icon-Update"`, `LIESMICH.txt`); Zip-Zeitstempel 20.11.2026, 21:08 Uhr Europe/Warsaw. Der lokale entpackte Ordner `Sparkz_in_the_Dust_Playtest_2026-11-20_Relikt-Update` entspricht diesem Icon-Update, nicht dem früheren Relikt-Update-Zip.
- SHA256 der Zip: `c5d4c27d200179ac611758cdc7cfc631d74edb1d80eca75b5a1463e3e41d95fe`

### Hinzugefügt

- Eigenes Laternen-Emblem für EXE, Explorer, Spielfenster, Taskleiste und Alt+Tab. Bei alten angehefteten Verknüpfungen gegebenenfalls die neue EXE erneut anheften.

## [2026-11-20-Relikt-Update] - 2026-11-20

Relikt-Rüstungen. Koop-Protokoll 37. Keine numerische Dateiversion.

- Paket: `Sparkz_in_the_Dust_Playtest_2026-11-20_Relikt-Update.zip`
- Quellen: `BUILD.json` und `LIESMICH.txt` in der Zip (`"update": "Relikt-Update"`, ohne App-Icon-Abschnitt); Zip-Zeitstempel 20.11.2026, 20:55 Uhr Europe/Warsaw
- SHA256 der Zip: `e89ee358119e75528c905a52b2ae70014b4a04f39821414e7b4a3483aaccfc1c`

### Hinzugefügt

- Drei Relikt-Rüstungssets mit insgesamt 18 Teilen. Jedes Teil hat 0,3 % Dropchance je besiegtem Dungeon-Gegner.

### Behoben

- Arena: Gegner erkennen den Spieler korrekt; Projektile nutzen die aktuellen Sektorgrenzen.

## [2026-11-20-Dungeon-EOS] - 2026-11-20

Dungeon-Kampfauswahl und EOS-Online. Koop-Protokoll 36. Ab hier heißt das Spielpaket **Sparkz in the Dust** (EXE `Sparkz in the Dust.exe`).

- Paket: `Sparkz_in_the_Dust_Playtest_2026-11-20_Dungeon-EOS.zip`
- Quellen: `LIESMICH.txt` (20.11.2026, 20:15 Uhr Europe/Warsaw) und `BUILD.json`
- Zu diesem Zip liegt im lokalen `releases/`-Ordner **keine** `.sha256`-Datei vor.

### Hinzugefügt

- Online-Koop über Epic Online Services: Sitzung erstellen, achtstelliger Einladungscode, Beitreten. EOS-P2P kann ein Relay nutzen. LAN/IP bleibt zusätzlich verfügbar.
- Beim Dungeon-Eintritt Wahl zwischen Runden (bestehende QTE-Kämpfe) und Echtzeit (Kampf direkt im Raum); im Koop entscheidet der Host. Standardsteuerung für den Echtzeit-Kampf: Linksklick/Leertaste Angriff, rechte Maustaste Schildblock, G Schildstoß, Q Laden, Strg Ausweichen, R Nachladen, H Heilen, T/mittlere Maustaste Werfen.
- LP und Munition bleiben beim Raumwechsel erhalten. Schotts, Quests und Beute-PvP bleiben aktiv.

### Hinweise

- Laut `LIESMICH.txt` war der Beitritt eines zweiten Rechners über verschiedene Internetanschlüsse zu diesem Zeitpunkt noch nicht geprüft. Das Paket bezeichnet sich als Testversion.

## [2026-11-20-Ruestungen-Arena-Ausstellung] - 2026-11-20

Starterrüstungen, Arena-Rückreise und Rüstungspuppe. Koop-Protokoll 35. Noch unter dem Paketnamen CHOBUTAI.

- Paket: `CHOBUTAI_Playtest_2026-11-20_Ruestungen-Arena-Ausstellung.zip`
- Quellen: `LIESMICH.txt`, `AENDERUNGEN.txt` und `BUILD.json` (LIESMICH 20.11.2026, 19:18 Uhr Europe/Warsaw)
- Zu diesem Zip liegt im lokalen `releases/`-Ordner **keine** `.sha256`-Datei vor.

### Hinzugefügt

- Individuelle Verteidigungs-, Resistenz- und Unterstützungswerte für die Charakterrüstungen von B1NZ, L0C0S, K080LD und GUN5D4L3 (gelten auch für vorhandene Spielstände; detaillierte Werte in `AENDERUNGEN.txt`).
- Arena: „Zurück ins Lager“ im Solo-Menü (Esc/F2). Im Koop steht der Button im Esc- und Host-Modusmenü; der Host führt die gesamte Gruppe zurück. Während Beuteduellen ist die Rückreise gesperrt.
- Rüstungspuppe: Ausstellung über mehrere Körperplätze gleichzeitig (Helm, Brust, Schultern, Arme, Beine, Rücken). Alte Einzelteil-Ausstellungen werden übernommen.

## [2026-11-20-Quartiere-Mobiliar-LootPvP] - 2026-11-20

Persönliche Quartiere, Möbel-Editor und Beute-PvP. Koop-Protokoll 34.

- Paket: `CHOBUTAI_Playtest_2026-11-20_Quartiere-Mobiliar-LootPvP.zip`
- Quellen: `LIESMICH.txt` und `BUILD.json` (LIESMICH 20.11.2026, 18:03 Uhr Europe/Warsaw)
- SHA256 der Zip: `7b9ff5eb4eba56ad2ed4730a935cf0da557293288571f3ae0c7abdec1018f359`

### Hinzugefügt

- Persönliche Koop-Quartiere mit Besucherauswahl an der Quartierluke.
- „Quartier bearbeiten“: Raster, 3D-Vorschau, Drehen, Verschieben, Einlagern, Rückgängig/Vor und Speichern. 20 Möbeltypen; zusätzliche Möbel über Werkstatt-Katalog, Bergungskapseln und Gegnerloot.
- Gegnerloot: „Will ich“ anklicken; ein Bewerber erhält direkt, mehrere kämpfen automatisch in der Arena. Unvergebene Items über Esc → Beute verteilen.

### Behoben

- Korrigierte Links-/Rechts-Ausrichtung der Charaktere in den gemeinsamen 3D-Ansichten.

### Hinweise

- Die `LIESMICH.txt` nennt als bereits enthalten: Tag-/Nachtzyklen, dynamische Lichtquellen, NPC-Tagesabläufe, Bergungsereignisse und Sektormodifikatoren. Für die drei zuletzt genannten Punkte wurde in `releases/` kein eigenes Playtest-Paket gefunden (siehe Lücken unten).

## [2026-11-20-Tag-Nacht] - 2026-11-20

Tag/Nacht und dynamisches Licht. Koop-Protokoll 28. `BUILD.json`-Version: `2026-11-20-Tag-Nacht`. Gebaut 20.11.2026, 12:25 Uhr Europe/Warsaw.

- Paket: `CHOBUTAI_Playtest_2026-11-20_Tag-Nacht.zip`
- SHA256 der Zip: `34592d71fc2c4f1c29c67eb13bc6b312085362c98a82ee876d43a29edfa8c150`

### Hinzugefügt

- Vollständiger Tag in 20 realen Minuten (Morgengrauen, Sonnenstand, Abenddämmerung, Mondlicht). Lager und Oberwelt ändern die Beleuchtung, das Quartier dezenter; unterirdische Dungeons behalten ihre eigene Beleuchtung. Im Titelmenü pausiert die Uhr. Die Uhrzeit wird gespeichert und im Koop vom Host synchronisiert.
- Lagerfeuer, Laternen, Randlaternen und Quartierlaternen wirken als lokale Lichtquellen; das Feuer flackert und wirft Schatten.

## [2026-11-20-3D-Audit] - 2026-11-20

Gemeinsame 3D-Darstellung von Basislager, Zuhause und Oberwelt. Koop-Protokoll 27. `BUILD.json`-Version: `2026-11-20-3D-Audit`. Gebaut 20.11.2026, 10:57 Uhr Europe/Warsaw.

- Paket: `CHOBUTAI_Playtest_2026-11-20_3D-Audit.zip`
- SHA256 der Zip: `4f30e8c7828bfdea4e05e64b177e1e67a0cf612583628d9f47fd3d2d9a8f51d8`

### Hinzugefügt

- Gemeinsame 3D-Darstellung für Basislager, Zuhause und Oberwelt. Erweitertes Lager mit verfolgender Spielerkamera; Zugänge zu Werkstatt, Versorgung, Brett, Quartier, Oberwelt und Arena bleiben aktiv.
- Anpassbare Tastenbelegung (bis zu drei Belegungen je Aktion, Konflikthinweise, Reset, Speicherung pro Benutzer), dokumentiert in diesem Paket.

## [2026-11-20-Arena-Market] - 2026-11-20

Arena-Händler, Bereitschaft und Arena-Münzen. Koop-Protokoll 26. `BUILD.json`-Version: `2026-11-20-Arena-Market`. Gebaut 20.11.2026, 01:57 Uhr Europe/Warsaw.

- Paket: `CHOBUTAI_Playtest_2026-11-20_Arena-Market.zip`
- SHA256 der Zip: `a0340cab09ebafb62f6a914cfca262f9246167e73560f287e0f2bc34c508c4f3`

### Hinzugefügt

- Kein automatischer Rundenstart: alle aktiven Spieler bestätigen mit Enter oder dem Bereit-Button, danach drei Sekunden Countdown.
- Arena-Händler an der Nordwand (E), im Kampf geschlossen. Eigener Händler-Pool: drei Rüstungen, ein Schild, drei Waffen und fünf Verbrauchsitems.
- Arena-Münzen: Gegner 1, Bosse 8, PvP-Sieger 3; im Koop wird der Fund geteilt. Münzen werden pro Charakter gespeichert und sind unabhängig von Gold.
- Kampfstim (Taste J): nächster tatsächlicher Treffer +20 %, maximal zwölf Sekunden.

## [2026-11-20-Arena-Cover] - 2026-11-20

Größere Arena mit Deckung. Koop-Protokoll 25. `BUILD.json`-Version: `2026-11-20-Arena-Cover`. Gebaut 20.11.2026, 01:27 Uhr Europe/Warsaw.

- Paket: `CHOBUTAI_Playtest_2026-11-20_Arena-Cover.zip`
- SHA256 der Zip: `5158c7610e50ee1d5304f81a4a56d518f8c2000e34159e8b9fdce7990c25af8f`

### Hinzugefügt

- Größere Arena (732 × 402 Spielpixel) mit verfolgenden Kameras pro Spieler.
- Sechs Wandsegmente, Kisten und Absperrungen als echte Deckung; Gegner laufen außen herum; neu verteilte Spawnpunkte. Ausgang im Süden, Moduskonsole im Nordosten (auch F2).

## [2026-11-20-Combat-Environment] - 2026-11-20

Kampf, Loadouts und Umweltflächen. Koop-Protokoll 24. `BUILD.json`-Version: `2026-11-20-Combat-Environment-Loadouts`. Gebaut 20.11.2026, 01:01 Uhr Europe/Warsaw.

- Paket: `CHOBUTAI_Playtest_2026-11-20_Combat-Environment.zip`
- SHA256 der Zip: `f57d25cb75be4a5968d5590cf56251fcf2c3ce74a304425bce6c9a8274545d92`

### Hinzugefügt

- Drei Waffenplätze (Aktiv, II, III) plus Schild- und Wurfplatz; Wechsel per Mausrad. Wurfplatz für Granaten, Wurfscheiben und Umweltwerkzeuge (T / mittlere Maustaste, auch F4).
- Arena-Kampf: Angriff, Schildblock, Schildstoß, Rolle, aufgeladener Angriff, Heilen, Werfen. Heilung, Wurf und Wiederbelebung sind kurze, unterbrechbare Aktionen.
- Umweltflächen: Öl, Wasser, Feuer, Elektro, Rauch und Giftqualm. Feuer entzündet Öl; Wasser kann Strom leiten; Lüfter entfernen lokale Wolken.
- Dungeon-Werkstatt im Hauptmenü auch ohne installiertes Godot, inklusive Umwelt-Werkzeug.

## [2026-11-19-Editor-Lighting] - 2026-11-19

Dungeon-Editor im Playtest und Beleuchtungs-Update. Koop-Protokoll 22. `BUILD.json`-Version: `2026-11-19-Editor-Lighting`. `LIESMICH.txt` vom 19.11.2026, 23:26 Uhr Europe/Warsaw.

- Paket: `CHOBUTAI_Playtest_2026-11-19_Editor-Lighting.zip`
- SHA256 der Zip: `8bd302444b04c4e96e69467297a7d1768f7f28869b9093d0d366ea5596f41a52`

### Hinzugefügt

- Hauptmenü → Dungeon Editor öffnet die Werkstatt auch ohne Godot. Strg+S speichert die Karte; im Koop wird die Karte des Hosts beim Gruppenstart übertragen.
- Taschenlampe an der Hand; bewegliche Gegnerschatten und Pixel-Lichtkanten.
- Rauchlaternen und Beutekapseln verwenden Ansichten neuer 3D-Modelle.

## [2026-11-19-Dungeon-Update] - 2026-11-19

Ältestes im lokalen `releases/`-Ordner gefundenes Playtest-Paket. Koop-Protokoll 21. `BUILD.json`-Version: `2026-11-19-Dungeon-Update`. `LIESMICH.txt` vom 19.11.2026, 22:50 Uhr Europe/Warsaw.

- Paket: `CHOBUTAI_Playtest_2026-11-19_Dungeon-Update.zip` (EXE noch `CHOBUTAI.exe`)
- SHA256 der Zip: `5cdae0cac4af780275fc9473eaaa65050b110159d71cba8829f7daaccf6b9617`

### Hinzugefügt

- Überarbeitete Eingangsschleuse als eigene Projektkarte im Spielpaket; Raumverbindungen und Quest-IDs bleiben bestehen. Enthalten ist eine Loot-Kapsel mit Reanimationskapseln.
- Feste Deko-Objekte blockieren Spieler, Gegner und Sichtlinien; Bodenflecken, kleiner Schutt und leichter Bewuchs bleiben begehbar.
- 40 Objekt-Atlanten aus überarbeiteten 3D-Quellen neu gerendert.
- Ausrüstungspause in Arena-Countdowns und zwischen Runden (C oder Esc → Inventar); der Rundenstart wartet, solange jemand den Charakterbildschirm offen hat.
- Abgestimmte Starterwaffen (B1NZ, L0C0S, GUN5D4L3, K080LD) und B1NZ-Drohnenangriff, wie in der `LIESMICH.txt` beschrieben.
- K.-o. und Wiederbelebung per Reanimationskapsel (Nähe + E bzw. im Rundenkampf über das Item).

### Hinweise

- Die `LIESMICH.txt` beschreibt außerdem den damals aktuellen Playtest-Stand (Koop 2–4 über IP/Tailscale, sechs Speicherplätze, Steuerung). Was davon schon vor diesem Paket existierte, lässt sich aus den vorliegenden Quellen nicht in eigene Versionen aufteilen. Ältere Playtest-Pakete wurden nicht gefunden.

## Bekannte Lücken

Diese Punkte sind absichtlich offen gelassen, weil dafür keine belastbare Versionquelle vorliegt:

- **Vor dem 19.11.2026** (vor Protokoll 21) wurde kein Playtest-Paket gefunden. Entwicklungsdokumente aus dem Projektordner (etwa vom 18. und 19.11.2026) sind keine versionierten Playtest-Releases.
- **Koop-Protokoll 23:** Zwischen Editor-Lighting (Protokoll 22) und Combat-Environment (Protokoll 24) gibt es in `releases/` kein Paket.
- **Koop-Protokolle 29–33:** Zwischen Tag-Nacht (Protokoll 28) und Quartiere-Mobiliar-LootPvP (Protokoll 34) gibt es in `releases/` keine Pakete. NPC-Tagesabläufe, Bergungsereignisse und Sektormodifikatoren tauchen in der Quartiere-`LIESMICH.txt` bereits als „bisher enthalten“ auf; das Einführungsdatum ist unbekannt.
- **UI-Polish** wird ab 0.1.38 als bereits enthalten genannt; ein eigenes Paket dazu wurde nicht gefunden.
- Im **GitHub-Repository** `bvultrex/Sparkz-in-the-Dust-Playtest` ist bisher nur **0.1.40** als Release und Tag veröffentlicht. Die älteren Stände stammen aus dem lokalen Projektordner.
- Im lokalen Arbeitsbaum gibt es **uncommittete** Änderungen (unter anderem Koop-Protokoll 39). Sie sind hier nicht als Version oder Feature aufgeführt.
