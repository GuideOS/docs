# Installation von GuideOS

Diese Anleitung beschreibt die Schritte zur Installation von GuideOS auf einem PC oder Notebook.  
GuideOS basiert auf Debian und verwendet den Cinnamon-Desktop.

---

## Systemanforderungen

- **Prozessor**: 64-Bit (Intel oder AMD)  
- **Arbeitsspeicher**: mindestens 2 GB (empfohlen: 4 GB oder mehr)  
- **Speicherplatz**: mindestens 20 GB (empfohlen: 40 GB oder mehr)  
- **Bootfähig über**: USB (UEFI oder Legacy BIOS)  

> **Hinweis:** Secure Boot sollte im UEFI deaktiviert sein, da GuideOS es derzeit nicht unterstützt.

---

## Installationsübersicht

1. ISO-Datei herunterladen  
2. Bootfähigen USB-Stick erstellen  
3. Vom USB-Stick starten  
4. Installation durchführen  
5. Erste Schritte nach der Installation  

---

## 1. ISO-Datei herunterladen

Die aktuelle ISO-Datei von GuideOS findest du hier:  
👉 [Download GuideOS](https://guideos.link/download)

---

## 2. Bootfähigen USB-Stick erstellen

### Unter Linux (per Terminal mit `dd`)

```bash
lsblk  # zur Erkennung des USB-Sticks
sudo dd if=guideos.iso of=/dev/sdX bs=4M status=progress && sync
