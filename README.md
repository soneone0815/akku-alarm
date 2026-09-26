# Akku Alarm

Android-App, die ein Vollbild-Popup anzeigt, sobald der Akku 10 % erreicht.

## So bekommst du die APK über GitHub

1. Neues Repository auf https://github.com/new anlegen (z. B. `battery-alert`).
2. Diesen Ordner in das Repo pushen:
   ```bash
   cd BatteryAlert
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/DEIN-NUTZERNAME/battery-alert.git
   git push -u origin main
   ```
3. Auf GitHub öffnest du den Reiter **Actions** – der Workflow "Build APK" startet automatisch.
4. Nach ca. 2–4 Minuten ist der Lauf grün. Öffne ihn und lade unter **Artifacts** die Datei `app-debug-apk` herunter (enthält `app-debug.apk`).
5. APK aufs Handy übertragen und installieren (ggf. "Installation aus unbekannten Quellen" erlauben).

## Nutzung in der App

1. App öffnen, auf **"Überwachung starten"** tippen.
2. Einmalig die Abfrage zur Akku-Optimierung bestätigen (wichtig, damit Android den Dienst nicht killt).
3. Sobald der Akku 10 % erreicht (und nicht lädt), erscheint das rote Vollbild-Popup mit Ton und Vibration.
4. Popup wird erst wieder ausgelöst, wenn der Akku über 15 % steigt oder geladen wurde.

## Hinweise

- Getestet als Konzept für Android 8.0+ (API 26+), Zielversion Android 14 (API 34).
- Für echten Dauerbetrieb solltest du den Hersteller-Akku-Optimierungen (bei Xiaomi, Huawei, Samsung etc.) zusätzlich manuell erlauben – sonst killt das System den Hintergrunddienst trotzdem gelegentlich.
- App-Icon ist der Systemstandard; du kannst später ein eigenes unter `app/src/main/res/mipmap` ergänzen.
