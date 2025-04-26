# Twitch API Keys erstellen – Schritt für Schritt Anleitung

> Diese Anleitung hilft dir dabei, deine Twitch **Client ID** und dein **Client Secret** korrekt zu erstellen und sie im Projekt einzutragen.

---

## 1. Gehe auf die Twitch Developer Console

Öffne die folgende Seite:  
👉 [https://dev.twitch.tv/console](https://dev.twitch.tv/console)

---

## 2. Klicke links auf „Anwendungen“

Hier siehst du bereits bestehende Apps oder kannst neue erstellen.

![Anwendungen öffnen](./screenshots/anwendungen_öffnen.png)

---

## 3. Neue Anwendung registrieren

- Klicke auf **"Deine Anwendung registrieren"**.

![Anwendung registrieren](./screenshots/anwendung_registrieren.png)

---

## 4. Formular ausfüllen

Trage folgende Daten ein:

| Feld | Wert |
|:---|:---|
| **Name** | Wähle einen beliebigen Namen (z.B. `discord_notify_bot`) |
| **OAuth Redirect URLs** | `http://localhost` |
| **Kategorie** | `Application Integration` |
| **Client-Typ** | `Vertraulich` |

- Bestätige das Captcha „Ich bin kein Roboter“.
- Danach auf **"Erstellen"** klicken.

![Formular ausfüllen](./screenshots/formular_ausfüllen.png)

---

## 5. Client ID und Client Secret finden

- Klicke auf **Verwalten** neben deiner Anwendung.
- Dort findest du:
  - **Client ID** (sichtbar)
  - **Client Secret** (über **"Neues Geheimnis"** generieren)

⚡ **Wichtig:** Das Client Secret wird nur einmal angezeigt – unbedingt speichern!

![Verwalten und Keys abrufen](./screenshots/verwalten_keys.png)

---

## 6. In der `config.json` einfügen

Beispiel:

```json
"twitch": {
  "accounts": [
    {
      "username": "DEIN_TWITCH_USERNAME",
      "client_id": "DEINE_CLIENT_ID",
      "client_secret": "DEIN_CLIENT_SECRET"
    }
  ]
}
```

---

# Fehlerbehebung

| Problem | Lösung |
|:---|:---|
| „Unauthorized“ Fehler | Client ID und Secret überprüfen |
| Stream wird nicht erkannt | Username korrekt schreiben |
| Secret vergessen | Neues Geheimnis erstellen |

---

**Fertig!** 🎉  
Jetzt kannst du deinen Twitch Account erfolgreich für das Projekt nutzen.
