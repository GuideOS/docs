# Installation von GuideOS

Diese Anleitung beschreibt die Schritte zur Installation von GuideOS auf einem PC oder Notebook.  
GuideOS basiert auf Debian und verwendet den Cinnamon-Desktop.

## Systemanforderungen

- **Prozessor**: 64-Bit (Intel oder AMD)  
- **Arbeitsspeicher**: mindestens 2 GB (empfohlen: 4 GB oder mehr)  
- **Speicherplatz**: mindestens 20 GB (empfohlen: 40 GB oder mehr)  
- **Bootfähig über**: USB (UEFI oder Legacy BIOS)  

> **Hinweis:** Secure Boot sollte im UEFI deaktiviert sein, da GuideOS es derzeit nicht unterstützt.

## Installationsübersicht

1. ISO-Datei herunterladen  
2. Bootfähigen USB-Stick erstellen  
3. Vom USB-Stick starten  
4. Installation durchführen  
5. Erste Schritte nach der Installation  

## 1. ISO-Datei herunterladen

Die aktuelle ISO-Datei von GuideOS findest du hier:  
👉 [Download GuideOS](https://guideos.link/download)

## 2. Bootfähigen USB-Stick erstellen

### Unter Linux (per Terminal mit `dd`)

```bash
lsblk  # zur Erkennung des USB-Sticks
sudo dd if=guideos.iso of=/dev/sdX bs=4M status=progress && sync
```

> **Achtung**: Ersetze `sdX` mit dem Gerätenamen deines USB-Sticks (z. B. `sdb`).  
> Stelle sicher, dass du das richtige Laufwerk angibst – falsche Eingaben können zu Datenverlust führen.

### Alternativ: grafische Tools für alle Plattformen

- **balenaEtcher** (Windows, Linux, macOS):  
  https://etcher.io

- **GNOME Laufwerke** („Laufwerke“ unter vielen Linux-Desktops):  
  Funktion *"Abbild auf Laufwerk schreiben…"*

- **Ventoy** (Multiboot-USB-Stick, ideal für mehrere ISOs):  
  https://ventoy.net

## 3. Vom USB-Stick starten

1. USB-Stick einstecken  
2. Rechner neu starten  
3. Boot-Menü aufrufen (`F12`, `F10`, `ESC` oder `DEL`, je nach Hersteller)  
4. USB-Stick als Startlaufwerk auswählen

## 4. GuideOS installieren

Nach dem Booten erscheint der Cinnamon-Desktop mit einem Symbol zur Installation.

1. Starte die grafische Installation über das Icon  
2. Folge dem Installationsassistenten:  
   - Sprache und Tastatur auswählen  
   - Partitionierung (automatisch oder manuell)  
   - Benutzername, Passwort und Rechnername festlegen  
   - Zeitzone einstellen  
3. Installation starten  
4. Nach Abschluss: System neu starten und USB-Stick entfernen

## 5. Erste Schritte nach der Installation

### System aktualisieren

```bash
gos -up
```

### Optional

- Weitere Software über das Anwendungsmenü oder per Terminal installieren  
- Cinnamon-Desktop nach eigenen Wünschen anpassen

> Bei Fragen oder Problemen steht dir die Community auf [linuxguides.de](https://forum.linuxguides.de) zur Verfügung.
