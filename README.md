<p align="center"><img src="bilder/logo.png" width="96" alt="IRL4YOU Cam"></p>

# IRL4YOU Cam und IRL4YOU Cam Net

**In diesem Repository liegen zwei Android-Apps.** Beide machen dein Android-Handy zur Kamera für die [IRL4YOU BOX](https://github.com/IRL4YOU/IRL4YOU-BOX); die Net-Fassung kann zusätzlich direkt an Server senden.
**This repository contains two Android apps.** Both turn your Android phone into a camera for the [IRL4YOU BOX](https://github.com/IRL4YOU/IRL4YOU-BOX); the Net version can also send directly to servers.

| | **IRL4YOU Cam** | **IRL4YOU Cam Net** |
|---|---|---|
| Datei / File | `IRL4YOU-Cam.apk` | `IRL4YOU-Cam-Net.apk` |
| Sendet an / Sends to | IRL4YOU BOX per USB-Kabel / via USB cable | USB-Box und zusätzlich RTMP, RTMPS, SRT, SRTLA / USB box plus RTMP, RTMPS, SRT, SRTLA |
| Internet-Berechtigung / Internet permission | nein / no | ja / yes |
| Gedacht für / Meant for | die einfache Fassung, nur mit der BOX / the simple version, BOX only | wer auch an eigene Server oder mehrere Netze senden will / for sending to your own servers or over several networks |

Beide lassen sich nebeneinander installieren (eigene App-Kennung) und haben getrennte Versionsnummern. Beide sind noch frühe Testversionen.
Both can be installed side by side (separate app ID) and have separate version numbers. Both are still early test versions.

**Download:** [Releases](../../releases/latest), dort liegen immer beide Dateien (nur Android) / both files are always there (Android only)

Die Beschreibung unten gilt für die Net-Fassung; die einfache hat keine Server-Ziele. / The description below covers the Net version; the simple one has no server targets.

## Screenshots

<p align="center">
  <img src="bilder/bedienfeld.jpg" width="720" alt="Bedienfeld: Linse, Codec, Bildrate, Bitrate / Control panel: lens, codec, frame rate, bitrate"><br>
  <sub>Bedienfeld / Control panel</sub>
</p>

<p align="center">
  <img src="bilder/senden.jpg" width="720" alt="Während des Sendens: Status, Akku, Strom / While sending: status, battery, current"><br>
  <sub>Beim Senden / While sending</sub>
</p>

<p align="center">
  <img src="bilder/box.png" width="720" alt="Kachel Handy auf der Box: Akku, Temperatur, Laden oder Entladen / Phone tile on the box: battery, temperature, charging or discharging"><br>
  <sub>Anzeige auf der Box: Akku, Temperatur, Laden oder Entladen / Display on the box: battery, temperature, charging or discharging</sub>
</p>

---

## Deutsch

### Was die App kann

- Bild und Ton des Handys per USB-Kabel an die Box senden, ohne WLAN
- Alternativ per RTMP, RTMPS, SRT oder SRTLA an einen Server senden (zum Beispiel Twitch, YouTube oder ein eigener Server): Adresse im Menü, bei RTMP mit Stream-Key, bei SRT mit Stream-ID, Passphrase (Verschlüsselung) und Latenz; bricht die Verbindung ab, verbindet die App von selbst neu (nur in der Net-Fassung)
- Verbindung weitergeben: Neben jeder Verbindung (Stift) zeigt die App einen QR-Code. Auf dem anderen Handy mit der Kamera-App scannen, der Link öffnet die App und bietet das Übernehmen an. Alternativ den Link kopieren und mit „Verbindung aus Link einfügen“ übernehmen. Der QR-Code wird in der App selbst erzeugt, ohne Fremdbibliothek. Er enthält Adresse und Schlüssel, also nur kurz zeigen
- Einstellungen sichern: Verbindungen und Einstellungen in eine Datei schreiben, mit Passwort verschlüsselt (nur Bordmittel von Android), und auf dem nächsten Handy wiederherstellen (Knöpfe unten auf der Verbindungsseite)
- Mehrere Verbindungen speichern (eigene Seite, je mit Namen und Kurzinfo), eine anhaken und senden; die Net-Fassung merkt sich Adresse, Key und Netze je Verbindung. Beim Senden bleibt die Verbindungsseite gesperrt, damit nichts Privates auf dem Bildschirm steht
- SRTLA bündelt WLAN, Mobilfunk und ein USB-Netz (Ethernet-Adapter, USB-Router oder USB-Tethering eines zweiten Handys) gleichzeitig zu einem Strom; fällt ein Netz weg, läuft der Strom über die anderen weiter. Je Netz einstellbare Priorität (1 bis 10, wirkt nur bei stabilem Netz), Anzeige von Anteil und Laufzeit je Netz
- Bei SRT und SRTLA passt die App die Videobitrate selbst an die Laufzeit und die Zahl der Pakete unterwegs an (nie über der gewählten Bitrate)
- Video als H.264 oder H.265, bis 1080p mit 25, 30, 50 oder 60 Bildern pro Sekunde
- Ton als AAC in Stereo oder Mono (vor dem Livegang wählbar), Mikrofon per Knopf stumm schalten; das Menü ist auch im Querformat erreichbar
- Pegelanzeige für den Ton am unteren Bildrand und Lautstärkeregler von −12 bis +24 dB, auch während der Übertragung
- Bitrate wählbar, bis 10 Mbit/s (bei RTMP und SRT ab 1 Mbit/s); im Netz senkt die App die Datenrate selbst, wenn es zu langsam wird
- Hintere Linsen einzeln wählen (zum Beispiel Weitwinkel, Normal, Tele), Wechsel auf die Frontkamera, Selfie-Bild auf Wunsch gespiegelt
- Zoomen mit zwei Fingern, über die Linsengrenzen hinweg mit automatischem Linsenwechsel (bei Handys mit Sammelkamera ohne Lücke)
- Handy drehen: Hochkant und Querformat, das Bild an der Box dreht ohne Unterbrechung mit
- Läuft weiter, wenn der Bildschirm ausgeht
- Übersteht einen Neustart der Box oder kurzes Abziehen des Kabels: Die App wartet auf die Box und sendet danach von selbst weiter
- Stopp auch über die Benachrichtigung, wenn man die Leiste von oben herunterzieht; ist die App nur offen, steht dort „Beenden“
- Logs-Knopf: Ereignisse und Kamera-Info lassen sich kopieren, zum Beispiel für eine Fehlermeldung
- Oberfläche auf Deutsch und Englisch, je nach Sprache des Handys
- Anzeige für Akkustand, Ladezustand, Strom und Temperatur des Handys, auch auf der Box sichtbar
- Sparsam gebaut: Das Bild kodiert der Video-Encoder des Handys (in der Regel in Hardware) und die Grafikeinheit dreht es, ohne Fremdbibliotheken und mit weniger als 1 MB Größe; den Internetzugriff braucht nur die Net-Fassung

### Was die App nicht kann

- Über WLAN oder Mobilfunk geht nur in der Net-Fassung etwas: RTMP, RTMPS, SRT oder SRTLA
- Keine Aufnahme auf dem Handy, keine Filter, keine Effekte, keine Einblendungen
- Per USB nur mit der IRL4YOU BOX
- H.265 per RTMP nur bei Servern mit Enhanced RTMP; wer sicher gehen will, nimmt H.264
- **Mit VPN (zum Beispiel Tailscale)** schickt Android auch die Net-App durch das VPN, wenn die VPN-App alles umleitet (etwa mit einem Exit-Node). Dann meldet die App „Server antwortet nicht“. Lösung: die App in der VPN-App vom VPN ausnehmen. Bei Tailscale (ab Version 1.70): Profilbild antippen, „App-based split tunneling“ wählen und „IRL4YOU Cam Net“ anhaken. Andere VPN-Apps haben dafür „Split Tunneling“ oder „Apps ausnehmen“. Alternativ das VPN zum Senden ausschalten.
- Dreht man das Handy während einer Übertragung ins Netz zwischen Hoch- und Querformat, ändert sich die Bildgröße, und manche Server verkraften das nicht
- Bei Handys ohne Sammelkamera entsteht beim Zoomen über eine Linsengrenze eine kurze Lücke im Bild
- Bei 50 oder 60 Bildern pro Sekunde im Hochformat schaffen manche Handys weniger
- Fokus und Belichtung laufen automatisch, von Hand einstellen (Antippen) geht noch nicht
- Externes Mikrofon (USB, Kabel, Bluetooth) nur in der Net-Fassung, im Menü wählbar; die einfache Fassung nimmt mit den eingebauten Mikrofonen auf, weil der USB-Anschluss an der Box hängt
- Ist die Box länger als 30 Minuten nicht erreichbar, beendet sich die App

### Gut zu wissen

- Ein USB-Anschluss lädt das Handy oft langsamer, als die Kamera Strom braucht. Der Akku kann trotz Kabel sinken. Besser ist ein USB-Hub mit eigenem Netzteil, der Daten und Ladestrom liefert. Die Strom-Anzeige der App hilft beim Prüfen.
- Das Handy wird bei laufender Kamera warm. Für lange Sendungen für Kühlung sorgen.
- Liefert Android bei einem Handy nur einen Mikrofonkanal, sendet die App denselben Ton auf beiden Seiten.
- Voraussetzung: Android 8.0 oder neuer und eine IRL4YOU BOX ab Version 0.5.142.

### Installation

1. Auf dem Handy die [Releases](../../releases/latest) öffnen und `IRL4YOU-Cam.apk` herunterladen.
2. Die heruntergeladene Datei öffnen. Android fragt, ob Installationen aus dieser Quelle (zum Beispiel dem Browser) erlaubt sind. Einmal erlauben, dann „Installieren“ tippen.
3. App „IRL4YOU Cam“ starten und die Berechtigungen für Kamera, Mikrofon und Benachrichtigungen erlauben. Die Benachrichtigung braucht Android, damit die App im Hintergrund weitersenden darf.
4. Updates: neue APK herunterladen und einfach über die alte installieren. Einstellungen bleiben erhalten.

### So benutzt du die App

1. Das Handy per USB-Kabel mit der IRL4YOU BOX verbinden. Das Kabel muss Daten übertragen, ein reines Ladekabel reicht nicht. Besser ist ein Hub mit eigenem Netzteil.
2. Android fragt, ob die App auf das USB-Gerät zugreifen darf. Erlauben.
3. In der App Linse, Codec, Bildrate und Bitrate wählen. Mit dem Start-Knopf unten beginnt die Übertragung. Das Bedienfeld klappt dann weg, das Bild bleibt.
4. Die Box zeigt das Handy als Kamera. Dort wählst du es wie jede andere Kamera aus.
5. Mit zwei Fingern zoomen, mit dem Umschalt-Symbol zwischen vorderer und hinterer Kamera wechseln, mit dem Mikrofon-Knopf den Ton stumm schalten. Mit Stopp beendest du die Übertragung.

### Wofür sie gut ist

- Das Handy als Hauptkamera oder als zweite Kamera für Live-Streams mit der IRL4YOU BOX, zum Beispiel unterwegs oder am Einsatzort
- Gute Handykamera mit mehreren Linsen statt einer teuren Zusatzkamera nutzen
- Hochkant oder Querformat, je nach Stream
- Ton direkt vom Handy-Mikrofon mitsenden

---

## English

### What the app does

- Sends the phone's video and audio to the box over a USB cable, without Wi-Fi
- Alternatively sends over RTMP, RTMPS, SRT or SRTLA to a server (for example Twitch, YouTube or your own server): address in the menu, with a stream key for RTMP, with stream ID, passphrase (encryption) and latency for SRT; if the connection drops, the app reconnects by itself (Net version only)
- Share a connection: next to each connection (pencil) the app shows a QR code. Scan it with the camera app of the other phone, the link opens the app and offers to add it. Alternatively copy the link and use "Verbindung aus Link einfügen" (paste connection from link). The QR code is generated inside the app, with no third-party library. It contains address and key, so show it only briefly
- Back up settings: write connections and settings to one file, encrypted with a password (Android built-ins only), and restore them on the next phone (buttons at the bottom of the connections page)
- Save several connections (own page, each with a name and a short summary), tick one and send; the Net version remembers address, key and networks per connection. While sending, the connections page stays locked so nothing private is on screen
- SRTLA bonds Wi-Fi, mobile data and a USB network (Ethernet adapter, USB router or USB tethering from a second phone) into one stream; if one network drops, the stream continues over the others. Priority per network (1 to 10, only effective while the network is stable), share and round-trip time per network shown
- With SRT and SRTLA the app adapts the video bitrate itself to round-trip time and packets in flight (never above the chosen bitrate)
- Video as H.264 or H.265, up to 1080p at 25, 30, 50 or 60 frames per second
- Audio as AAC in stereo or mono (selectable before going live), microphone can be muted with a button; the menu is also reachable in landscape
- Level meter for the sound at the bottom edge of the picture and a volume control from −12 to +24 dB, also while streaming
- Selectable bitrate, up to 10 Mbit/s (from 1 Mbit/s with RTMP and SRT); over the network the app lowers the data rate by itself when it is too slow
- Choose rear lenses individually (for example wide, normal, tele), switch to the front camera, selfie image mirrored if wanted
- Pinch to zoom, with automatic lens switching across lens boundaries (no gap on phones with a logical multi-camera)
- Rotate the phone: portrait and landscape, the picture on the box rotates without interruption
- Keeps running when the screen turns off
- Survives a restart of the box or briefly unplugging the cable: the app waits for the box and then keeps sending by itself
- Stop also from the notification when you pull the shade down; while the app is only open it offers "Quit"
- Logs button: events and camera info can be copied, for example for a bug report
- Interface in German and English, depending on the phone's language
- Shows battery level, charging state, current and temperature of the phone, also visible on the box
- Built to be frugal: the picture is encoded by the phone's video encoder (usually in hardware) and rotated by the graphics unit, with no third-party libraries and a size below 1 MB; only the Net version needs internet access

### What the app does not do

- Over Wi-Fi or mobile data only the Net version does something: RTMP, RTMPS, SRT or SRTLA
- No recording on the phone, no filters, no effects, no overlays
- Over USB it works only with the IRL4YOU BOX
- H.265 over RTMP only with servers that support Enhanced RTMP; choose H.264 to be safe
- **With a VPN (for example Tailscale)** Android also sends the Net app through the VPN when the VPN app redirects everything (for example with an exit node). The app then reports "Server antwortet nicht" (server does not answer). Fix: exclude the app from the VPN in the VPN app. With Tailscale (version 1.70 or later): tap your profile picture, choose "App-based split tunneling" and tick "IRL4YOU Cam Net". Other VPN apps call this "split tunneling" or "exclude apps". Alternatively turn the VPN off while sending.
- Rotating the phone between portrait and landscape during a stream over the network changes the picture size, and some servers cannot handle that
- On phones without a logical multi-camera, zooming across a lens boundary causes a short gap in the picture
- At 50 or 60 frames per second in portrait, some phones deliver fewer
- Focus and exposure are automatic, setting them by hand (tap) is not possible yet
- External microphone (USB, cable, Bluetooth) only in the Net version, selectable in the menu; the simple version records with the built-in microphones because the USB port is used for the box
- If the box is not reachable for more than 30 minutes, the app quits

### Good to know

- A USB port often charges the phone more slowly than the camera uses power. The battery can drop even with the cable plugged in. A USB hub with its own power supply that provides data and charging current works better. The app's current display helps to check this.
- The phone gets warm while the camera runs. Provide cooling for long streams.
- If Android delivers only one microphone channel on a phone, the app sends the same sound on both sides.
- Requires Android 8.0 or newer and an IRL4YOU BOX version 0.5.142 or later.

### Installation

1. On the phone, open the [Releases](../../releases/latest) and download `IRL4YOU-Cam.apk`.
2. Open the downloaded file. Android asks whether installs from this source (for example the browser) are allowed. Allow it once, then tap "Install".
3. Start the app "IRL4YOU Cam" and allow the permissions for camera, microphone and notifications. Android needs the notification so the app may keep sending in the background.
4. Updates: download the new APK and install it over the old one. Settings are kept.

### How to use the app

1. Connect the phone to the IRL4YOU BOX with a USB cable. The cable must carry data, a charge-only cable is not enough. A hub with its own power supply is better.
2. Android asks whether the app may access the USB device. Allow it.
3. In the app choose lens, codec, frame rate and bitrate. The start button at the bottom begins the stream. The panel then folds away, the picture stays.
4. The box shows the phone as a camera. You select it there like any other camera.
5. Pinch with two fingers to zoom, use the switch icon to change between front and rear camera, use the microphone button to mute. Stop ends the stream.

### What it is good for

- The phone as main camera or second camera for live streams with the IRL4YOU BOX, for example on the road or on location
- Use a good multi-lens phone camera instead of an expensive extra camera
- Portrait or landscape, depending on the stream
- Send the sound from the phone's microphone along

---

## Hinweis zu KI

Dieses Projekt entsteht mit Unterstützung von KI. Wir testen auf echten Geräten, nicht jede Zeile wird aber von Hand geprüft. Bitte vor dem Livebetrieb kurz selbst ausprobieren.

## Note on AI

This project is made with the support of AI. We test on real devices, but not every line is reviewed by hand. Please try it out yourself briefly before going live.

---

[Nutzungslizenz / License](LICENSE.md) · [Datenschutz / Privacy](DATENSCHUTZ.md)
