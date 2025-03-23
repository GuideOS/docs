# GuideOS – Installation

Diese Anleitung beschreibt die Schritte zur Installation von GuideOS auf einem PC oder Notebook. GuideOS basiert auf Debian und nutzt den Cinnamon-Desktop.

## Systemanforderungen

- **CPU**: 64-Bit-Prozessor (Intel oder AMD)
- **RAM**: mindestens 2 GB (empfohlen: 4 GB oder mehr)
- **Speicherplatz**: mindestens 20 GB (empfohlen: 40 GB)
- **Bootfähig über**: USB (UEFI oder Legacy)

## 1. ISO-Datei herunterladen

Die aktuelle ISO findest du hier:

👉 [Download GuideOS](https://guideos.link/download)  

## 2. Bootfähigen USB-Stick erstellen

Nutze eines der folgenden Tools, um die ISO auf einen USB-Stick zu schreiben:

- **Linux**:  
  ```bash
  sudo dd if=guideos.iso of=/dev/sdX bs=4M status=progress && sync
