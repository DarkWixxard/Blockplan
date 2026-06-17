# ⬡ BlockPlan

Ein schlanker, browserbasierter **Blockschaltplan-Editor** für Elektronik- und
Embedded-Projekte. Ziehe vorgefertigte Bausteine – von Netzteilen über Arduino,
ESP und Raspberry Pi bis zu Sensoren und Motoren – auf die Arbeitsfläche,
verbinde sie und exportiere das Ergebnis als PDF.

Die gesamte Anwendung steckt in **einer einzigen HTML-Datei** – kein Build,
keine Installation, keine Abhängigkeiten zum Selbsthosten.

## ✨ Funktionen

- **Drag & Drop** – Blöcke aus der Seitenleiste auf die Arbeitsfläche ziehen
- **Umfangreiche Bauteil-Bibliothek** mit über 150 vorgefertigten Vorlagen,
  thematisch in Kategorien gegliedert (siehe unten)
- **Vier Block-Formen**: Rechteck, Raute (Entscheidung), Kreis (Start/Ende) und
  freie Notiz
- **Verbindungen** zwischen Blöcken über Ports (oben/unten/links/rechts) als
  geschwungene Bézier-Linien mit Pfeilspitzen
- **8 Farbvarianten** je Block – die Verbindungslinien übernehmen die Blockfarbe
- **Mehrfachauswahl** per Auswahlrahmen, inklusive gemeinsamem Verschieben
- **Eigenschaften-Panel**: Beschriftung, Breite, Höhe, Farbe und Form anpassen
- **Inline-Bearbeitung** der Beschriftung direkt im Block
- **PDF-Export** (A4/A3, Hoch- oder Querformat, mit eigenem Titel)
- **Statusleiste** mit Anzahl der Blöcke, Verbindungen und aktivem Modus
- **Beispieldiagramm** wird beim Start automatisch geladen

## 🚀 Schnellstart

Es ist kein Build-Schritt nötig. Du hast zwei Möglichkeiten:

1. **Direkt öffnen** – `blockplan.html` per Doppelklick im Browser öffnen.
2. **Repository klonen** und die Datei lokal öffnen:

   ```bash
   git clone https://github.com/DarkWixxard/Blockplan.git
   cd Blockplan
   # blockplan.html im Browser öffnen
   ```

> **Hinweis:** Für den PDF-Export werden [html2canvas](https://html2canvas.hertzen.com/)
> und [jsPDF](https://github.com/parallax/jsPDF) per CDN geladen. Dafür wird beim
> Export einmalig eine Internetverbindung benötigt.

## 🖱 Bedienung

| Aktion | So geht's |
| --- | --- |
| Block hinzufügen | Vorlage aus der Seitenleiste auf die Fläche ziehen |
| Block verschieben | Block anklicken und ziehen |
| Block bearbeiten | Block anklicken → Eigenschaften-Panel rechts |
| Beschriftung ändern | Block auswählen und Text direkt eintippen |
| Verbinden | Button **🔗 Verbinden** aktivieren → zwei Ports nacheinander anklicken |
| Linie löschen | Button **✂ Linie löschen** aktivieren → Verbindung anklicken |
| Mehrere auswählen | Auswahlrahmen über leere Fläche aufziehen |
| Als PDF speichern | Button **📄 Als PDF speichern** → Format, Ausrichtung & Titel wählen |

### ⌨️ Tastenkürzel

| Taste | Funktion |
| --- | --- |
| `Entf` / `Backspace` | Ausgewählten Block oder ausgewählte Verbindung löschen |
| `Esc` | Auswahl aufheben und Verbindungsmodus verlassen |

## 🧩 Bauteil-Kategorien

Die Seitenleiste bündelt die Vorlagen in folgenden Bereichen:

- ⚡ **Stromversorgung** – Netzteile (24 V / 12 V / 5 V / 3.3 V), Akkus, USB-C PD
- 🛡 **Schutz & Sicherung** – Sicherungen, Überspannungs-/Verpol-/ESD-Schutz, Schalter
- 🔁 **Wandler & Verteiler** – Step-Down/Step-Up, Buck-Boost, LDO, Verteiler, BMS
- 🔵 **Arduino-Familie** – Uno, Nano, Mega, Mini, Leonardo, Due, MKR WiFi
- 📡 **ESP / WiFi-MCU** – ESP32 (S3/C3), ESP8266, Wemos D1 Mini, ESP32-CAM
- 🟥 **Raspberry-Pi-Familie** – Pi 5/4B/3B+, Zero (2)W, Pico (W), GPIO, HAT
- ⬛ **Weitere MCU / SBC** – STM32, ATmega/ATtiny, RP2040, nRF52840, Teensy, Jetson u. a.
- 🔘 **Halbleiter & Schalten** – MOSFET, Transistoren, Relais, Optokoppler, H-Brücke
- 💡 **Anzeige & Ausgabe** – LED(-Strip/-Matrix), OLED, LCD, TFT, E-Paper, Buzzer
- ⚙ **Aktoren & Motoren** – Servo, DC-, Stepper-, Brushless-Motor, ESC, Pumpe
- 📟 **Sensoren** – Temperatur, Feuchte, PIR, Ultraschall, IMU, GPS, Gas, Strom u. a.
- 📶 **Kommunikation** – WiFi, Bluetooth, LoRa, Zigbee, Ethernet, I2C/SPI/UART/CAN
- 💾 **Speicher** – SD-Karte, EEPROM, Flash, RAM
- 🔢 **Eingabe** – Potentiometer, Encoder, Joystick, Tastatur, RFID/NFC, Fingerabdruck
- 🔊 **Audio** – DAC, I2S, Verstärker, DFPlayer MP3
- 🌐 **System / Software** – Linux, RTOS, Webserver, MQTT, Home Assistant, Node-RED

Reicht eine Vorlage nicht aus, lässt sich jeder Block über das Eigenschaften-Panel
frei umbenennen, einfärben und in der Form ändern.

## 🛠 Technik

- Reines **HTML, CSS und Vanilla JavaScript** – keine Frameworks
- **SVG** für die Verbindungslinien (Bézier-Kurven mit Pfeil-Markern)
- **html2canvas** + **jsPDF** für den PDF-Export (via CDN)
- Schriftarten *JetBrains Mono* und *Syne* via Google Fonts

## 📂 Projektstruktur

```
Blockplan/
├── blockplan.html   # die komplette Anwendung (UI, Styles, Logik)
├── LICENSE          # MIT-Lizenz
└── README.md        # diese Datei
```

## 📄 Lizenz

Veröffentlicht unter der [MIT-Lizenz](LICENSE). © 2026 Emil Friedrich
