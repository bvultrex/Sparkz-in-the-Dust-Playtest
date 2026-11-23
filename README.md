# Sparkz in the Dust – Playtest

**Sparkz in the Dust** ist ein Action-RPG für Windows. Die Welt liegt nach einem verheerenden Krieg in industriellen Ruinen und kontaminiertem Nebel. In kleinen Kommunen versuchen Überlebende, mit Bergung, Handwerk und improvisierter Technik weiterzumachen.

Dies ist das öffentliche Playtest-Repository. Hier liegen die spielbaren Windows-Pakete, nicht der vollständige Quellcode. Der aktuelle Stand ist eine **Testversion**.

## Download

**[Neueste Playtest-Version herunterladen](https://github.com/bvultrex/Sparkz-in-the-Dust-Playtest/releases/latest)**

Aktuell veröffentlicht: **Playtest 0.1.42** (Controller und Boss-Trophäen, 23.11.2026, Koop-Protokoll 41). Auf der Release-Seite unter *Assets* die `.zip` wählen. Ältere Pakete stehen unter [Releases](https://github.com/bvultrex/Sparkz-in-the-Dust-Playtest/releases). Eine Übersicht aller bekannten Playtest-Stände – auch solche, die bisher nur lokal vorliegen – steht in [CHANGELOG.md](CHANGELOG.md).

## Installation

1. Die Zip herunterladen und **vollständig in einen eigenen Ordner entpacken** (nicht direkt aus der Zip starten).
2. Im entpackten Ordner `Sparkz in the Dust.exe` starten.
3. Die `.pck`-Datei, die DLLs und `eos.cfg` müssen bei der EXE bleiben.
4. Godot, Steam und der Epic Games Launcher müssen nicht separat installiert werden.
5. Falls Windows SmartScreen warnt: *Weitere Informationen* → *Trotzdem ausführen* (der Build ist nicht signiert).

Alle Details zur jeweiligen Version, zur Steuerung und zu bekannten Grenzen stehen in der `LIESMICH.txt` im Paket.

**Steam Deck:** In Steam unter *Nicht-Steam-Spiel hinzufügen* die Windows-`Sparkz in the Dust.exe` einbinden und den Windows-Build mit Proton starten. In Textfeldern öffnet **Steam+X** die Bildschirmtastatur. In den Einstellungen gibt es die Anzeige-Optionen *Pixelgenau (Letterbox)* (480×270 in ganzen Stufen) und *Bildschirm füllen*; auf 1280×800 (16:10) wird *Bildschirm füllen* automatisch vorgeschlagen.

Der exportierte Playtest 0.1.42 ist ein **Windows-x64**-Build mit **Godot 4.7.2**.

## Koop

Es gibt Koop für 2–4 Spieler.

- Im Koop-Menü Name und gegebenenfalls einen gespeicherten Charakter wählen.
- **Online mit EOS:** Der Host erstellt eine Sitzung und teilt seinen achtstelligen Einladungscode (erneutes Anklicken kopiert den Code). Mitspieler geben den Code ein und treten bei. Der Host startet danach mit *Base betreten*.
- **LAN/IP** bleibt zusätzlich verfügbar (Spielport UDP 28730).
- Wenn der Host die Sitzung beendet, endet sie für alle. Es gibt keinen Hostwechsel und keinen späteren Einstieg.
- Alle Mitspieler brauchen eine Version mit **demselben Koop-Protokoll**. **0.1.42 ist nicht mit 0.1.41 oder älteren Builds kompatibel** (Protokoll 41 gegenüber Protokoll 40 und darunter).

Welche Versionen zusammenpassen, steht in den Release-Notes und im [CHANGELOG](CHANGELOG.md).

## Steuerung (Standard in 0.1.42)

Die Tasten sind in den Einstellungen änderbar (Titelmenü > Einstellungen > Tastenbelegung; im Spiel auch über Charakter/Inventar).

**Erkundung und Menüs**

| Aktion | Standard |
| --- | --- |
| Bewegen | WASD / Pfeiltasten |
| Sprint | Shift |
| Ausweichen | Strg |
| Interagieren | E |
| Charakter / Inventar | C |
| Emote-Rad | Q |
| Pausemenü | Esc |
| Speichern / Laden (Solo) | F5 / F9 |

**Dungeon (Echtzeit)**

| Aktion | Standard |
| --- | --- |
| Angriff | Linksklick oder Leertaste |
| Schildblock | Rechte Maustaste |
| Schildstoß | G |
| Aufladen | Q |
| Ausweichen | Strg |
| Nachladen | R |
| Heilen | H |
| Werfen | T oder mittlere Maustaste |

Im Dungeon wählt ihr beim Eintritt **Runden** (QTE-Kämpfe) oder **Echtzeit** (Kampf direkt im Raum); im Koop entscheidet der Host.

**Controller und Steam Deck** (ab 0.1.42): Xbox-Controller und Steam Deck werden unterstützt. Bewegen mit dem linken Stick, Zielen mit dem rechten Stick, Menüs ohne Maus (sichtbarer Fokus; B/Zurück schließt). Der Bunker-Editor ist vollständig mit dem Pad bedienbar. Standardbelegungen für Fähigkeiten liegen auf dem Steuerkreuz; Tasten bleiben in den Einstellungen änderbar.

**Dev-Konsole** (ab 0.1.40): Taste `^` öffnet und schließt die Konsole, Esc schließt ebenfalls. Befehle stehen in der `LIESMICH.txt` und in den [Release Notes zu 0.1.40](https://github.com/bvultrex/Sparkz-in-the-Dust-Playtest/releases/tag/v0.1.40).

## Was der aktuelle Playtest enthält

Die folgende Liste gilt für Playtest **0.1.42**. Neu gegenüber 0.1.41 sind Set-Boni und Gruppen-Boni, Boss-Trophäen, Controller- und Steam-Deck-Unterstützung sowie mehrere Spiel- und Oberflächenkorrekturen. Koop nutzt Protokoll 41 und ist nicht mit 0.1.41 oder älteren Builds kompatibel. Alles Weitere ist kumulativ aus den Playtest-Notizen der vorangegangenen Pakete übernommen, soweit später keine Entfernung dokumentiert ist.

### Welt und Gebiete

- Basislager, Zuhause und Oberwelt nutzen eine gemeinsame 3D-Darstellung. Das erweiterte Lager hat eine verfolgende Spielerkamera; Zugänge zu Werkstatt, Versorgung, Brett, Quartier, Oberwelt und Arena bleiben aktiv.
- Persönliche Quartiere, im Koop unabhängig betret- und verlassbar, mit Besucherauswahl an der Quartierluke.
- Arena: sichtbarer Eingang im Südwesten des Lagers (E). Spielfeld 732 × 402 Pixel mit verfolgenden Kameras pro Spieler, sechs Wandsegmenten, Kisten und Absperrungen als echte Deckung, Gegnern, die außen herumlaufen, neu verteilten Spawnpunkten, Ausgang im Süden und Moduskonsole im Nordosten (auch F2).
- Dungeon mit überarbeiteter Eingangsschleuse als eigener Projektkarte. Raumverbindungen und Quest-IDs bleiben bestehen. Enthalten ist eine Loot-Kapsel mit Reanimationskapseln. Feste Deko blockiert Spieler, Gegner und Sichtlinien; Bodenflecken, kleiner Schutt und leichter Bewuchs bleiben begehbar.
- Weitere in den Paketprüfungen von 0.1.38/0.1.39 genannte Orte, an denen Ausrüstung angebaut wurde: Signal-Turm, Druckschacht und Filtermagazin. 0.1.40 erklärt den Inhalt gegenüber 0.1.39 für unverändert.

### Spielmodi

- Einzelspieler und Koop für 2–4 Spieler.
- Arena-Moduswahl über F2 (im Koop durch den Host). In den Playtest-Notizen startet Koop mit PvP und Solo mit Horden.
- Kein automatischer Rundenstart: alle aktiven Spieler bestätigen mit Enter oder dem Bereit-Button (im Solo reicht die eigene Bestätigung), danach folgen drei Sekunden Countdown. Erneutes Bestätigen nimmt Bereit zurück. Shop oder Ausrüstung öffnen nimmt die eigene Bestätigung zurück; der Start wartet, bis niemand mehr handelt und alle bereit sind.
- Dungeon-Expeditionen: beim Eintritt Wahl zwischen Runden (bestehende QTE-Kämpfe) und Echtzeit (Kampf direkt im Raum); im Koop entscheidet der Host. Schotts, Quests und Beute-PvP bleiben aktiv. LP und Munition bleiben beim Raumwechsel erhalten.

### Kampf

- Echtzeit-Arena: Angriff in Maus- oder Blickrichtung, Frontblock mit Schild und Einhandwaffe, kurzer Schildstoß aus der Deckung, Rolle (nur ein Teil der Bewegung schützt vor Treffern), aufgeladener Angriff mit zusätzlichen AP, Heilen, Werfen und Waffenwechsel per Mausrad.
- Heilung, Wurf und Wiederbelebung sind kurze, unterbrechbare Aktionen. Der Verbrauch erfolgt erst beim Wirksamwerden; eine abgebrochene Heilung kostet kein Item.
- Umweltflächen: Öl, Wasser, Feuer, Elektro, Rauch und Giftqualm. Feuer entzündet Öl, Wasser kann Strom leiten, Lüfter entfernen lokale Wolken. Spielerflächen treffen im PvE keine Verbündeten; neutrale Levelgefahren schon. In der Erkundung stehen Umwelt-Verbrauchswerkzeuge zur Verfügung.
- Ausrüstungspause in Arena-Countdowns und zwischen Runden (C oder Esc → Inventar). Solange jemand den Charakterbildschirm offen hat, wartet der Rundenstart. Während der laufenden Runde bleibt ein Ausrüstungswechsel gesperrt.
- Bei 0 HP sind Bewegung und Aktionen gesperrt. In Horden, Bosskämpfen und Koop-Dungeons hilft die Reanimationskapsel eines Mitspielers (außerhalb des Rundenkampfs: Nähe und E; in der Arena muss die kurze Wiederbelebung ungestört enden; im Rundenkampf über das Item). Im PvP werden kampfunfähige Spieler zur nächsten Runde wieder fit. Sind alle Spieler kampfunfähig, ist der Lauf verloren.
- Kampfstim (J): der nächste tatsächliche Treffer verursacht 20 % mehr Schaden, höchstens zwölf Sekunden.
- Dungeon-Gegner werden im Koop synchronisiert.

### Ausrüstung und Charakter

- Charakterbildschirm und Inventar (C), in den Paketprüfungen mit sechs Menüreitern. Rechts liegen die Plätze Schild, Aktiv, II, III und Wurf. Waffen werden per Ziehen und Ablegen gesetzt; das Mausrad wechselt durch belegte Plätze. Reserven geben keine Boni. Mit Schild werden unvereinbare Zweihandwaffen beim Wechsel übersprungen. Während Angriff, Nachladen, Blocken, Rollen oder einer aktiven Drohne ist der Wechsel gesperrt; Magazine werden dadurch nicht aufgefüllt. Der Wurfplatz nimmt Granaten, Wurfscheiben und Umweltwerkzeuge auf und arbeitet getrennt von der Hauptwaffe.
- Starterwaffen B1NZ, L0C0S, GUN5D4L3 und K080LD. Bei B1NZ startet die Angriffstaste eine Drohne auf den anvisierten Gegner (in den Notizen 150 Reichweite); die Drohne kehrt zum Rucksack zurück, Ausweichen kann den Einschlag vermeiden. K080LD ist als Ritualimpuls ohne Munition beschrieben. Treffer, Rüstung und Resistenzen beeinflussen den Schaden. Loot-Waffen behalten eigene Werte und dürfen stärker oder schneller sein.
- Standard-Rüstungssets, erhältlich über Beutekapseln und den Signalturm: Nebelbergung, Wiederhüter, Zisterne, Schleusenwacht, Aschekurier, Stahlreißer, Bagger, Sturmspule, Sichelspur, Bastionswacht, Sporenhüter, Moorhüter, Weidenorakel, Wurzelgeist, Dornlitanei, Nachtzirkel, Aluhut, Pappheld, Rettungsteam, Smasher, Junkgenius, Aerial, Porzellankitsch, Leitungsdienst, Aufbruchsdienst, Saatpfleger, Quartierwacht, Fadenpegel, Absperrtrupp, Leitungsprobe, Trassendeckung, Ringpeiler, Ringbrecher, Wundmoos, Rostwehr, Rostgewölbe, Sperrmedizin, Sentinelpanzer und Filterthron (legendär). Jedes Set hat sechs Teile (Helm, Brust, Schultern, Arme, Beine und Rücken). Weitere Sets folgen.
- Lebendige Ausrüstung: sechs ausrüstbare 3D-Teile mit beweglichen Baugruppen – Rußfänger (Rücken), Glühmotten-Habitat (Rücken), Wartungskrabbe (Schultern), Schachtspäher-Helm (Kopf), Kolbenmanschetten (Arme), Federläufer-Schienen (Beine). Die Animationen sind kosmetisch; die passiven Werte gelten normal. Die Glühmotten nutzen die vorhandene Begleiter-Aktion und erzeugen kein zusätzliches Licht.
- Fünf Relikt-Rüstungssets; jedes Teil droppt sehr selten (0,3 % je besiegtem Dungeon-Gegner). Darunter sind das Kernsystem der Labormatriarchin und das Schweigesiegel der stillen Leitung.
- Set-Boni für vollständige Rüstungssets, einschließlich Gruppen-Boni, wenn mehrere Spieler im Koop Teile desselben Sets tragen.
- Boss-Trophäen: Bosse lassen je Kill ein noch fehlendes Teil fallen. In der Arena beträgt die Chance 25 %. Besiegte Bosse erscheinen erneut und tragen einen Namensbalken.
- Rüstungspuppe: unter Ausstellung → Rüstung können Helm, Brust, Schultern, Arme, Beine und Rücken gleichzeitig belegt werden. Unterschiedliche Sets sind kombinierbar, ausgestellte Teile bleiben im Besitz, alte Einzelteil-Ausstellungen werden übernommen. Besucher können das Set ansehen; ihr eigener Ausstellungsstand bleibt getrennt. In 0.1.39 wurde der Wohnungsslot für den Helm auf `armor_head` korrigiert.
- Level, Skills und persönliches Gold gehören zum Charakter. Arena-Münzen werden pro Charakter gespeichert und sind unabhängig von Gold.
- Backpack-Begleiter mit passender Ausrüstung (Standardtaste V).

### Lager, Werkstatt und Beute

- Werkstatt, Versorgung und Brett sind im Basislager erreichbar. Die Werkstatt hat unter anderem einen Verbrauchsreiter (dort war in den frühen Notizen die Reanimationskapsel käuflich).
- Dungeon-Werkstatt im Hauptmenü, auch ohne installiertes Godot: Kategorien, Suche, Vorschau, 90-Grad-Drehung, Wände, Türen, Gegner und Deko sowie ein Umwelt-Werkzeug für Flächen, Filterlüfter und Druckfässer. Eigene Karten werden im Benutzerprofil gespeichert (JSON-Import/Export und Rückgängig). Im Koop verteilt der Host seine Karte an die Gruppe.
- Arena-Händler links an der Nordwand (E); im Kampf ist sein Schott geschlossen. Eigener Händler-Pool: drei Rüstungen, ein Schild, drei Waffen und fünf Verbrauchsitems. Arena-Münzen: gewöhnliche Gegner 1, Bosse 8, PvP-Sieger 3; im Koop wird der Fund geteilt, bei PvE-Sieg wird der Rest eingesammelt.
- Möbel-Editor im eigenen Quartier („Quartier bearbeiten“): Raster, 3D-Vorschau, Drehen, Verschieben, Einlagern, Rückgängig/Vor und Speichern. 20 Möbeltypen mit Icons und Stückzahlen; die bisherige Einrichtung zählt als Startbestand, weitere Stücke kommen über Werkstatt-Katalog, Bergungskapseln und Gegnerloot. Im Katalog wird gegen persönliches Gold gekauft (Kauf wird sofort gespeichert). R dreht um 90 Grad, Entf lagert ein, Strg+Z / Strg+Y machen Schritte rückgängig oder wiederholen sie. Rote Vorschau markiert ungültige Platzierungen (Luke, Wände, Überschneidungen, erreichbare Interaktionspunkte). Besucher dürfen ansehen und Exponate begutachten, aber keine fremden Möbel oder Truhen verändern. Möbelkollisionen und Besitz sind je Quartier getrennt; Live-Änderungen gelten für Besucher.
- Gegnerloot: „Will ich“ anklicken und bestätigen. Ein Bewerber erhält den Gegenstand direkt, mehrere kämpfen automatisch in der Arena, andere Spieler schauen zu, danach kehrt die Gruppe zur Expedition zurück. Unvergebene Items lassen sich über Esc → Beute verteilen (persönliche Vergabe mit Speicherquittungen). Während Beuteduellen ist die Arena-Rückreise gesperrt.

### Koop und Online

- Online über Epic Online Services: im Koop-Menü Name und gegebenenfalls einen gespeicherten Charakter wählen, dann Online mit EOS → Erstellen. Der Host teilt einen achtstelligen Einladungscode (erneutes Anklicken kopiert den Code). Mitspieler: Code eingeben und beitreten. Der Host startet danach mit *Base betreten* und simuliert die Spielwelt.
- EOS-P2P kann bei Bedarf ein Relay nutzen. `eos.cfg` liegt im Paket. LAN/IP bleibt zusätzlich verfügbar (Spielport UDP 28730).
- Koop-Protokoll 41 (EOS-Bucket in der Paketprüfung: `CHOBUTAI-41-`). 0.1.42 ist nicht mit 0.1.41 oder älteren Builds kompatibel.
- Wenn der Host die Sitzung beendet, endet sie für alle. Es gibt keinen Hostwechsel und keinen späteren Einstieg. Der Host steuert Reisen zwischen Bereichen. Expeditionen bleiben gemeinsame Gruppenreisen; Quartiere können unabhängig betreten und verlassen werden.
- Charakter laden in der Lobby oder im Esc-Menü des Lagers übernimmt den gespeicherten Charakter samt Ausrüstung, Inventar, Level, Skills und persönlichem Geld. Die Gruppenwelt bleibt erhalten.

### Tag, Nacht, Licht und Weltgeschehen

- Ein vollständiger Tag dauert 20 reale Minuten (Morgengrauen, Sonnenstand, Abenddämmerung, lesbares Mondlicht). Lager und Oberwelt ändern ihre Beleuchtung, das Quartier reagiert dezenter, unterirdische Dungeons behalten ihre eigene Beleuchtung. Im Titelmenü pausiert die Uhr. Die Uhrzeit wird gespeichert und im Koop vom Host synchronisiert.
- Lagerfeuer und Laternen – einschließlich Randlaternen und der vier Quartierlaternen – beleuchten Boden und nahe Figuren. Das Feuer flackert und wirft Schatten.
- Taschenlampe an der Hand (Standardtaste F), bewegliche Gegnerschatten und Pixel-Lichtkanten. Rauchlaternen und Beutekapseln verwenden Ansichten neuer 3D-Modelle.
- NPC-Tagesabläufe, Bergungsereignisse und Sektormodifikatoren (in den Quartiere-Notizen bereits als enthalten genannt; 0.1.40 spricht zusammenfassend von Tag/Nacht und Ereignissen).

### Steuerung, Speichern und Oberfläche

- Tastenbelegung im Titelmenü unter Einstellungen und im Spiel über Charakter/Inventar (im Koop zusätzlich Esc). Eine Aktion hat bis zu drei Belegungen, Konflikte werden gemeldet, „Alles zurücksetzen“ stellt die Standardbelegung wieder her, Änderungen werden sofort pro Benutzer gespeichert, Hinweise im HUD folgen der Belegung. Esc bleibt als fester Rückweg. Die Standardbelegung steht im Abschnitt [Steuerung](#steuerung-standard-in-0142). Xbox-Controller und Steam Deck: Analogsticks, Menüfokus, Bunker-Editor mit dem Pad, Anzeige-Option (Letterbox oder Bildschirm füllen) und Steam+X für die Bildschirmtastatur.
- Sechs Speicherplätze. F5 öffnet die Speicherauswahl, F9 die Ladeauswahl im Solo-Spiel. Neue Spiele fragen vor Beginn nach dem Ziel-Slot, Automatiken speichern danach in den aktiven Slot. Belegte Slots werden zum Überschreiben erneut ausgewählt. Unter Windows wird beim Überschreiben die Umbenennung kurz erneut versucht, wenn die Datei gerade gesperrt ist. Alte Spielstände bleiben lesbar. Sie liegen unter `%APPDATA%\Godot\app_userdata\CHOBUTAI - Action RPG Prototype\`; das Paket enthält keine persönlichen Spielstände.
- Korrigierte Links-/Rechts-Ausrichtung der Charaktere in den gemeinsamen 3D-Ansichten.
- UI-Polish, in den Paketprüfungen von 0.1.38/0.1.39 als sechs überarbeitete Menüreiter geprüft. Eine feinere Aufschlüsselung, was das Polish umfasst, steht in den Playtest-Notizen nicht.
- Eigenes Laternen-Emblem für EXE, Explorer, Spielfenster, Taskleiste und Alt+Tab. Bei alten angehefteten Verknüpfungen gegebenenfalls die neue EXE erneut anheften.
- Aus der Arena führt „Zurück ins Lager“ zurück: im Solo über Esc/F2, im Koop im Esc- und Host-Modusmenü; der Host nimmt die gesamte Gruppe mit.

### Entwicklerkonsole

- Mit `^` öffnen und schließen, Esc schließt ebenfalls. Solange die Konsole offen ist, reagiert die Spielfigur nicht. Pfeil hoch/runter blättert durch die letzten Befehle, Tab ergänzt Befehle und Item-IDs. Bei aktivem Godmode steht oben rechts ein Hinweis.
- Befehle: `player.add.item <ItemID> [Anzahl]`, `player.add.level <Anzahl>`, `player.add.xp <Anzahl>`, `player.set.godmode on|off`, `list.items [Filter]`, `help`, `clear`.
- Statt `player` gelten auch `me` und `p1`, im Koop zusätzlich `p2` bis `p4`, `all` oder der Charaktername. Im Koop darf nur der Host Godmode setzen, dafür auch für alle Spieler. Verbrauchsitems kann der Host auch an andere geben. Ausrüstung, Möbel, Level und XP funktionieren nur für den eigenen Spieler.

### Audio und Technik

- Soundeffekte von JDSherbert (Pixel Game Essentials SFX Pack); Atmosphärenklänge sind prozedural erstellt.
- Windows-x64-Playtest, exportiert mit Godot 4.7.2. Eigenes App-Icon, Dateiversion 0.1.42.0. Godot, Steam und der Epic Games Launcher müssen nicht separat installiert werden.
- Das Paket bezeichnet sich ausdrücklich als Testversion. Offen ist laut `LIESMICH.txt` unter anderem der Beitritt eines zweiten Rechners über verschiedene Internetanschlüsse. Die Export-Prüfung der EXE bestätigte die Regionen Basis, Quartiere, Oberwelt, Dungeon und Arena, erreichte danach aber das Zeitlimit von 180 s vor den Checks zu Möbeln, Blickrichtung, Tag/Nacht und Tasten-Remap.

## Prüfsumme

Zu der veröffentlichten Zip gibt es eine `.sha256`-Datei. So prüfst du, ob der Download vollständig ist:

```powershell
Get-FileHash .\Sparkz_in_the_Dust_Playtest_*.zip -Algorithm SHA256
```

SHA256 der aktuellen Zip `Sparkz_in_the_Dust_Playtest_2026-11-23_Controller.zip`:

`7beb2e1eb1fd6dd2774e71fc6e5a71a38f57786734e026aa810ac556817d602c`

## Feedback

Fehler, Abstürze und Anmerkungen bitte als [Issue in diesem Repository](https://github.com/bvultrex/Sparkz-in-the-Dust-Playtest/issues) öffnen. In der `LIESMICH.txt` steht zusätzlich, wo Spielstände und Logs liegen.

Spielstände bleiben aus Kompatibilitätsgründen unter `%APPDATA%\Godot\app_userdata\CHOBUTAI - Action RPG Prototype\`.

## Credits und Lizenzen

Im Playtest-Paket liegen `CREDITS.txt`, `GODOT-LICENSE.txt` und `EOSG-LICENSE.txt`. In der `CREDITS.txt` von 0.1.42 heißt es:

- Sound effects by JDSherbert (Pixel Game Essentials SFX Pack); Audiodaten unverändert
- Atmosphärenklänge: prozedural erstellt
- EOSG 2.3.1 by Delano Lourenco (MIT), <https://github.com/3ddelano/epic-online-services-godot>
- Epic Online Services SDK: Copyright Epic Games, Inc. All Rights Reserved

In diesem GitHub-Repository gibt es keine eigene Lizenzdatei für das Spiel selbst.
