# Nervensystem — interaktiver Entwurf

Virtuell begehbare Klanginstallation für Johanna Mangold. Arbeitsfassung.

## Ausprobieren

Installation betreten anklicken, um Ton zu aktivieren. Maus ziehen zum Umschauen; WASD oder Pfeiltasten zum Bewegen; Mausrad zum Vor-/Zurückgehen. Die Pfeilfelder funktionieren auch auf Touchscreens. Gesamtansicht setzt die Kamera zurück.

Eine dunkle kleine Figur anklicken, dann eine freie Ablage anklicken. Alternativ die Kontakte rechts bedienen. Escape oder „Figur zurücksetzen“ legt ein aufgenommenes Objekt zurück. Sechs Objekte können zwischen zwölf Plätzen auf vier Körpern bewegt werden.

Jeder Platz hat einen fest zugeordneten Sound. Er läuft in Schleife, solange der Platz belegt ist. Entfernen blendet ihn aus. Alle aktiven Loops werden gemeinsam über Stereo ausgegeben. Die Zuordnung wird beim Laden zufällig verteilt; „Neue Konstellation“ verändert nur die Belegung. Elf Sounds auf zwölf Plätzen bedeuten, dass ein Sound zweimal vergeben ist.

## GitHub Pages

Den gesamten Inhalt dieses Ordners einschließlich audio/ und vendor/ in den Veröffentlichungsordner deines GitHub-Pages-Repositories hochladen. index.html muss direkt darin liegen. Bestehende Dateien vorher sichern, falls dort bereits eine Website liegt. Für eine Unterseite kannst du den Inhalt stattdessen in einen Ordner namens nervensystem legen.

Es ist kein Build nötig. Alle Pfade sind relativ; JavaScript und Audiodateien werden mitgeliefert. Die Website benötigt keinen externen CDN-Aufruf und kein Backend.

## Lokal öffnen

Ein lokaler Webserver ist nötig; ein Doppelklick auf index.html genügt wegen der JavaScript-Module nicht. Mit installiertem Python im entpackten Ordner:

    python3 -m http.server 8000

Danach http://localhost:8000 im Browser öffnen.

## Dateien und Anpassungen

- app.js: Formen, Stellplätze, Navigation und Klangsteuerung.
- style.css: Darstellung und responsive Oberfläche.
- audio/A01.mp3 bis A11.mp3: Webkopien der elf bereitgestellten WAV-Fragmente.
- fallback.js: vereinfachte Canvas-Darstellung, wenn WebGL fehlt.
- vendor/three.mjs: Three.js 0.170.0, MIT-Lizenz in vendor/LICENSE-three.txt.

Die Formen sind schematische Entwürfe, keine maßstabsverbindliche Bauplanung. Die Kamera kann durch Körper hindurchgehen. Audio startet erst nach einem Klick. Sehr kurze Originalfragmente wiederholen sich entsprechend schnell; die Loops sind nicht rhythmisch synchronisiert. Die Original-WAVs wurden nicht verändert.

## Prüfung

Im Browser geprüft: Start und Laden aller elf Audiodateien, Aufnehmen und Absetzen über die Kontaktübersicht, Belegungsanzeige. Die Testumgebung unterstützt kein WebGL; visuell wurde deshalb die Canvas-Ersatzdarstellung geprüft. WebGL- und Mobilgerätetest vor Versand an die Jury empfohlen.
