# Тропа · Russisch A2 → B1

Russisch-Lern-App von A2 bis B1 mit drei Themen: **Islam**, **Dagestan** und **Sport**.

## Funktionen
- **Heute**: 20-Minuten-Einheit mit Timer (5 Min. Karten, 10 Min. Text, 5 Min. Grammatik), Streak und Fortschritt pro Thema
- **Karten**: rund 100 Wörter mit Betonung und Beispielsatz, Wiederholung nach dem Leitner-System (1, 2, 4, 8, 16 Tage), Russisch ↔ Deutsch, Vorlesen
- **Texte**: 6 Lesetexte (A2 bis B1) mit antippbaren Vokabeln und Verständnisfragen
- **Grammatik**: Präpositiv, Genitiv, Instrumental, Dativ, Verbalaspekt, Verben der Bewegung, который
- **Quiz**: 10 Fragen pro Runde
- **Sprechen**: 12 Sprechthemen plus fertiger ChatGPT-Prompt

## Starten
Einfach `index.html` im Browser öffnen. Der Fortschritt wird im `localStorage` des Browsers gespeichert.

## Firebase (Google-Login + Cloud-Speicherung)
1. In der [Firebase Console](https://console.firebase.google.com) ein Projekt anlegen (oder ein bestehendes nutzen).
2. **Authentication → Anmeldemethode → Google** aktivieren.
3. **Authentication → Einstellungen → Autorisierte Domains**: `athleticconsumer-dotcom.github.io` hinzufügen.
4. **Firestore Database** erstellen und die Regeln aus `firestore.rules` einfügen.
5. **Projekteinstellungen → Deine Apps → Web-App** anlegen und die Werte von `firebaseConfig` in `firebase-config.js` eintragen.

Ohne Konfiguration funktioniert die App weiter, speichert dann aber nur lokal im Browser.
Beim Anmelden werden lokaler Fortschritt und Cloud-Fortschritt zusammengeführt.

## Als App installieren
- **Android / Chrome / Edge:** oben in der App auf „App installieren“ tippen.
- **iPhone / iPad:** in Safari auf Teilen → „Zum Home-Bildschirm“.

Die App funktioniert danach auch offline (Fortschritt wird beim nächsten Online-Sein mit Firebase synchronisiert, wenn du angemeldet bist).
