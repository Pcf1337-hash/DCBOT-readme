# 🏗️ DachTimer - Arbeitszeiterfassungs-App für Dachdecker

Moderne, mobile Arbeitszeiterfassungs- und Baustellendokumentations-App für Dachdecker mit KI-gestützter Spracheingabe.

## 📦 APK Build & Verteilung

Die App kann als standalone APK gebaut und an Kollegen verteilt werden - ohne Metro-Bundler und PC-Verbindung!

### 🚀 Schnellstart für APK-Build
1. **Eingabeaufforderung öffnen** (Windows + R → cmd)
2. **In Projektordner wechseln:** `cd c:\DachTimerApp`
3. **EAS initialisieren:** `npx eas-cli@latest init --id b9b80cf0-121c-4799-ae4a-f3edfa758638`
4. **APK bauen:** `npx eas-cli@latest build --platform android --profile production`
5. **10-20 Minuten warten** und APK herunterladen von [expo.dev](https://expo.dev)

### 📚 Dokumentation
- **[SCHRITT_FÜR_SCHRITT.md](SCHRITT_FÜR_SCHRITT.md)** - Detaillierte Build-Anleitung für Nicht-Programmierer
- **[GOOGLE_SPEECH_SETUP.md](GOOGLE_SPEECH_SETUP.md)** - Google Speech-to-Text Setup (Optional)
- **[DEVELOPMENT.md](DEVELOPMENT.md)** - Entwickler-Guide & Testing
- **[TODO.md](TODO.md)** - Projektstatus & Roadmap

### ✅ App Features
- ✅ Funktioniert komplett offline (SQLite Datenbank)
- ✅ Alle Features ohne Metro/PC nach Installation
- ✅ Android Widget für Home Screen
- ✅ Keine Server-Kosten
- 📡 Internet nur für optionale KI-Features (Claude API)

## 🚀 Hauptfeatures

- ⏱️ **Zeiterfassung mit Widget**: Android Home-Screen Widget mit Start/Pause/Stop Buttons und Live-Timer
- 🎤 **KI-gestützte Spracheingabe**: Automatische Extraktion von Arbeitsdaten via Claude API (Haiku 4.5 - schnellstes Modell)
  - Versteht deutsche Dachdecker-Fachbegriffe
  - Extrahiert Kunde, Adresse, Zeiten, Material, Mitarbeiter automatisch
  - Manuelle Texteingabe als Alternative
  - Extrem günstig: ~€0.005 pro Extraktion (~0,5 Cent)
- 📊 **Dashboard & Analytics**: Umfassende Übersichten
  - Tagesansicht mit Balkendiagramm (letzte 7 Tage)
  - Wochenansicht (letzte 4 Wochen)
  - Monatsansicht mit Liniendiagramm (12 Monate)
  - Kundenstatistiken mit Kreisdiagramm
  - Kalenderansicht mit Eintragsmarkierungen
- 💰 **Gehaltsberechnung**: Stundenlohn konfigurierbar in Einstellungen
- 📸 **Foto-Dokumentation**: Bis zu 10 Fotos pro Eintrag (Kamera & Galerie)
- 📑 **Export & Sharing**:
  - PDF-Reports mit professionellem Layout
  - CSV-Export für Excel (deutsche Formatierung)
  - Datenbank-Backup-Funktion
- 🌙 **Dark Mode**: Vollständige Dark/Light Mode Unterstützung mit automatischer Systemerkennung
- 📴 **Offline-fähig**: Vollständige Funktionalität ohne Internet (außer KI-Features)

## 🛠️ Tech Stack

- **Framework**: React Native 0.81.5 + Expo 54
- **Sprache**: TypeScript 5.9
- **UI Framework**: React 19 + React Native Paper 5.12
- **Navigation**: Expo Router 6.0 (File-based Routing)
- **Datenbank**: SQLite (expo-sqlite) mit Repository Pattern
- **State Management**: Zustand 5.0
- **KI-Integration**:
  - Claude API Haiku 4.5 (Anthropic) - schnellstes & günstigstes Modell
  - Zod-Validierung für robuste Type-Safety
  - Spezialisierter Prompt für deutsche Dachdecker-Terminologie
- **Charts & Visualisierung**: react-native-chart-kit, react-native-calendars
- **Native Features**:
  - Android Widget (Kotlin)
  - Push Notifications
  - Kamera & Galerie
  - Haptisches Feedback

## 📋 Voraussetzungen

### Für Entwicklung
- Node.js >= 18
- npm (kommt mit Node.js)
- Android Studio mit Android SDK (für Android-Entwicklung)
- Android Emulator oder physisches Android-Gerät

### Für APK-Build (Production)
- Expo-Account (kostenlos auf [expo.dev](https://expo.dev))
- Internet-Verbindung
- Keine lokale Build-Umgebung nötig (EAS Build in der Cloud)

## 🏁 Installation & Setup

### 1. Repository klonen
```bash
git clone <repository-url>
cd DachTimerApp
```

### 2. Dependencies installieren
```bash
npm install --legacy-peer-deps
```

### 3. API-Keys konfigurieren (Optional - nur für KI-Features)

Die App funktioniert komplett offline. API-Keys sind nur für optionale KI-Features nötig:

- **Claude API**: Für KI-gestützte Datenextraktion aus Spracheingaben
  - Modell: Claude Haiku 4.5 (schnellstes & günstigstes)
  - Kosten: ~€0.005 pro Extraktion (~0,5 Cent)
  - Key wird sicher in der App gespeichert (Settings → Voice Input Tab)
  - Setup: Direkt in der App unter "Voice Input" → API Key eingeben

- **Google Speech-to-Text** (Optional): Für Audio-zu-Text-Umwandlung
  - Setup-Anleitung: [GOOGLE_SPEECH_SETUP.md](GOOGLE_SPEECH_SETUP.md)
  - 60 Minuten/Monat kostenlos

### 4. App im Entwicklermodus testen

**Empfohlene Methode (Windows):**
```bash
# PowerShell-Skript ausführen (setzt automatisch JAVA_HOME und Android SDK)
powershell -ExecutionPolicy Bypass -File "build-android.ps1"
```

**Manuelle Methode:**
```bash
# Terminal 1: Metro Bundler starten
npx expo start

# Terminal 2: App auf Android Emulator installieren
set JAVA_HOME=C:\Program Files\Android\Android Studio\jbr
set ANDROID_HOME=C:\Users\Administrator\AppData\Local\Android\Sdk
npx expo run:android
```

Detaillierte Anleitung: [DEVELOPMENT.md](DEVELOPMENT.md)

## 📱 Verwendung

### ⏱️ Zeiterfassung mit Widget
1. **Widget hinzufügen**: Auf Home Screen lange drücken → Widgets → DachTimer
2. **Timer starten**: Direkt vom Widget oder im Timer-Tab
3. **Pausen**: "Pause" Button (Widget oder App)
4. **Stoppen**: "Stop" Button → Eintrag wird automatisch gespeichert
5. **Widget-Sync**: Widget und App synchronisieren sich automatisch

### 🎤 KI-gestützte Spracheingabe
1. **Voice Input Tab** öffnen
2. **Claude API Key** einrichten (einmalig in Settings)
3. **Eingabemethode wählen**:
   - **AUDIO**: Mikrofon-Button für Aufnahme
   - **TEXT**: Manuelle Texteingabe
4. **Arbeitsbericht sprechen/schreiben**:
   ```
   "Bei Frau Müller in der Hauptstraße 12, 32051 Herford von 8-12 Uhr,
   30 Min Pause. Flicken geschweißt auf Flachdach. 2 Rollen PYE 2000 verwendet."
   ```
5. **KI verarbeitet** automatisch:
   - Kunde, Adresse, Zeiten, Pausen
   - Material mit Mengen
   - Arbeitsbeschreibung
   - Mitarbeiter
6. **Review-Screen**: Alle Felder prüfen & anpassen
7. **Speichern**

### 📊 Analytics & Reports
- **Tag**: Balkendiagramm der letzten 7 Tage
- **Woche**: Stundenübersicht der letzten 4 Wochen
- **Monat**: Jahresübersicht mit Liniendiagramm
- **Kunden**: Top 5 Kunden mit Kreisdiagramm
- **Kalender**: Monatsansicht mit Eintragsmarkierungen
- **Export**: PDF/CSV via FAB-Button (unten rechts)

### ⚙️ Einstellungen
- Theme (Hell/Dunkel/Auto)
- Stundenlohn für Kostenberechnung
- Mitarbeiter-Verwaltung
- Standard-Pausenlänge
- Benachrichtigungen
- Datenbank-Backup

## 🗂️ Projektstruktur

```
DachTimerApp/
├── app/                           # Expo Router Screens (File-based Routing)
│   ├── (tabs)/                   # Tab Navigation
│   │   ├── dashboard.tsx         # Dashboard mit Übersicht
│   │   ├── timer.tsx             # Timer-Funktionalität
│   │   ├── voice-input.tsx       # KI-Spracheingabe
│   │   ├── analytics.tsx         # Charts & Statistiken
│   │   └── settings.tsx          # App-Einstellungen
│   ├── entries/                  # Zeiteinträge-Verwaltung
│   │   ├── index.tsx             # Liste aller Einträge
│   │   ├── new.tsx               # Neuer Eintrag
│   │   ├── [id].tsx              # Detail-Ansicht
│   │   └── edit/[id].tsx         # Bearbeiten
│   ├── review-voice-input.tsx    # Review KI-extrahierter Daten
│   └── _layout.tsx               # Root Layout mit Theme
├── src/
│   ├── components/               # Wiederverwendbare UI-Komponenten
│   │   ├── timer/                # Timer-Komponenten
│   │   ├── dashboard/            # Dashboard-Cards
│   │   ├── analytics/            # Charts (Daily, Weekly, Monthly, etc.)
│   │   ├── photos/               # Foto-Verwaltung
│   │   └── export/               # Export-Modal
│   ├── database/
│   │   ├── schema.ts             # SQLite-Schema (4 Tabellen)
│   │   ├── connection.ts         # DB-Verbindung
│   │   └── repositories/         # Repository Pattern für DB-Zugriff
│   ├── services/
│   │   ├── claudeService.ts      # Claude API Integration (optimiert)
│   │   ├── photoService.ts       # Foto-Verwaltung
│   │   ├── exportService.ts      # PDF/CSV-Export
│   │   ├── backupService.ts      # DB-Backup
│   │   └── notificationService.ts # Push Notifications
│   ├── store/                    # Zustand State Management
│   │   ├── timerStore.ts         # Timer-State
│   │   └── settingsStore.ts      # App-Einstellungen
│   ├── types/                    # TypeScript Interfaces
│   ├── constants/                # Theme & Config
│   └── utils/                    # Helper Functions
├── android/                      # Native Android Code
│   └── app/src/main/
│       ├── java/.../             # Widget (Kotlin)
│       └── res/                  # Widget Layout & Resources
└── assets/                       # Images, Icons, Fonts
```

## 🔧 Konfiguration

### API-Keys
API-Keys werden verschlüsselt gespeichert (expo-secure-store):
- **Claude API**: Einrichten in Settings → Voice Input Tab
  - Benötigt für KI-gestützte Datenextraktion
  - Modell: Claude Haiku 4.5 (claude-haiku-4-5-20251001)
  - Kosten: ~€0.005 pro Extraktion (~0,5 Cent)
  - API Key erhalten unter: [console.anthropic.com](https://console.anthropic.com/)

### Theme & Erscheinungsbild
- **Dark Mode**: Automatisch basierend auf System-Einstellungen
- **Manuelle Umschaltung**: Settings → Theme (Hell/Dunkel/Auto)
- **Vollständige Dark Mode Unterstützung**: Alle Screens, Komponenten, Charts

## 📦 Datenbank Schema

Die App verwendet SQLite für lokale Datenspeicherung (komplett offline):

### time_entries
- **Basisdaten**: id, date, kunde, baustelle, adresse
- **Zeiten**: startZeit, endZeit, pausenMinuten, arbeitsStunden
- **Mitarbeiter**: mitarbeiter (JSON-Array)
- **Arbeiten**: durchgefuehrteArbeiten, kundenhinweise, offeneAufgaben
- **Medien**: photos (JSON-Array von Pfaden)
- **Metadaten**: createdAt, updatedAt

### materials
- **Material-Info**: beschreibung, menge, einheit, kosten
- **Verknüpfung**: timeEntryId (Foreign Key mit CASCADE)

### settings
- **Key-Value Store**: key, value
- **Speichert**: API-Keys, Theme, Stundenlohn, Mitarbeiter, etc.

### construction_sites
- **Baustellen-Verwaltung**: name, lastUsed
- **Für Autocomplete** (zukünftig)

## 🧪 Testing & Entwicklung

### Android Emulator Testing (Empfohlen)

**Voraussetzungen:**
- Android Studio mit Android SDK installiert
- Android Emulator läuft (z.B. Pixel 9 API 35)

**Schnellstart:**
```bash
# PowerShell-Skript (empfohlen - setzt automatisch Umgebungsvariablen)
powershell -ExecutionPolicy Bypass -File "build-android.ps1"
```

**App neu laden nach Code-Änderungen:**
- **R** zweimal drücken (Reload)
- **Ctrl+M** → "Reload" (Dev Menu)

**Troubleshooting:**
```bash
# Port 8081 belegt
taskkill //F //IM node.exe
npx expo start --clear

# Native Module geändert
powershell -ExecutionPolicy Bypass -File "build-android.ps1"
```

**Details:** Siehe [DEVELOPMENT.md](DEVELOPMENT.md)

### Claude API Testen

Die App enthält eine umfassende Test-Suite für die Claude API Integration:

```typescript
import testSuite from '@services/__tests__/claudeService.test';

// Alle Tests ausführen
await testSuite.runAllTests();

// Einzelnen Test ausführen
await testSuite.runSingleTest(0);

// Custom Text testen
await testSuite.runCustomTest('Ihr Test-Text hier...');
```

**Details:** Siehe [CLAUDE_API_SETUP.md](CLAUDE_API_SETUP.md)

## 📤 Export & Sharing

### PDF-Export
- **Professionelles Layout** mit Firmen-Header
- **Zeitraum-Auswahl**: Heute, Woche, Monat, Benutzerdefiniert
- **Detaillierte Tabelle**: Alle Zeiteinträge mit Material
- **Zusammenfassung**: Gesamtstunden und Materialkosten
- **Sharing**: Direkt per E-Mail, WhatsApp, etc.

### CSV-Export
- **Excel-kompatibel**: UTF-8 BOM, Semikolon-Separator
- **Deutsche Formatierung**: Komma als Dezimaltrennzeichen
- **Buchhaltungs-ready**: Datum, Kunde, Stunden, Kosten
- **Zeitraum-Auswahl**: Flexibel konfigurierbar

### Datenbank-Backup
- **SQLite-Export**: Komplette Datenbank als .db-Datei
- **Sicher teilen**: Via Sharing-Funktionalität
- **Wiederherstellung**: Für zukünftige Versionen geplant

## 🤝 Entwicklungshistorie & Status

### Aktueller Stand: **~98% komplett** 🎉 (2026-01-08)

Die DachTimerApp ist eine vollständig funktionsfähige Produktions-App mit allen geplanten Kernfeatures.

### 🆕 Neueste Änderungen (2026-01-08)
- 📝 README.md vollständig aktualisiert mit allen implementierten Features
- 🔄 Claude API Modell korrekt dokumentiert (Haiku 4.5)
- 💰 Korrekte Kostenangaben für KI-Features
- 📚 Dokumentation vereinheitlicht und bereinigt

### Abgeschlossene Entwicklungsphasen

#### Phase 1-3: Grundlegende Infrastruktur ✅
- React Native 0.81.5 + Expo 54 + TypeScript 5.9
- Expo Router Navigation (5 Tabs)
- SQLite-Datenbank mit Repository Pattern
- Theme-System (Light/Dark Mode)
- Timer-Funktionalität mit Zustand State Management
- Push Notifications & Haptisches Feedback

#### Phase 4-6: UI & Datenvisualisierung ✅
- Dashboard mit Statistiken & Schnellaktionen
- Zeiteinträge-Verwaltung (Liste, Detail, Bearbeiten)
- Manuelle Eingabe mit Validierung
- Analytics mit 5 Ansichten:
  - Tagesansicht (Balkendiagramm)
  - Wochenansicht (4 Wochen)
  - Monatsansicht (Liniendiagramm, 12 Monate)
  - Kundenstatistiken (Kreisdiagramm)
  - Kalenderansicht mit Markierungen

#### Phase 7: Foto-Dokumentation ✅
- Kamera & Galerie-Integration
- Max. 10 Fotos pro Eintrag
- Vollbild-Ansicht & Thumbnail-Galerie
- Automatische Speicherung im App-Verzeichnis

#### Phase 9: KI-Integration (2026-01-07 OPTIMIERT) ✅
- **Claude API Haiku 4.5** - schnellstes & günstigstes Modell
  - Model ID: claude-haiku-4-5-20251001
  - Kosten: ~€0.005 pro Extraktion (~0,5 Cent)
- **Spezialisierter Prompt** für deutsche Dachdecker-Terminologie
- **Robustes Error-Handling** mit detaillierten Fehlermeldungen
- **Zod-Validierung** für Type-Safety
- **Test-Suite** mit umfassenden Test-Cases
- **Fachbegriffe-Support**: PYE, Schweißbahn, Bitumen, Flachdach, Steildach, etc.
- Audio-Recording & manuelle Texteingabe
- Review-Screen für KI-extrahierte Daten
- API Key wird sicher in expo-secure-store gespeichert

#### Phase 10: Einstellungen ✅
- Theme-Auswahl (Hell/Dunkel/Auto)
- Stundenlohn-Konfiguration
- Mitarbeiter-Verwaltung
- Benachrichtigungs-Einstellungen
- Datenbank-Statistiken
- "Alle Daten löschen" mit Bestätigung

#### Phase 11: Export & Sharing ✅
- **PDF-Export** mit professionellem Layout
- **CSV-Export** für Excel (deutsche Formatierung)
- **Datenbank-Backup** (.db-Datei)
- Zeitraum-Auswahl (Heute, Woche, Monat, Custom)
- Sharing-Funktionalität

#### Phase 12: Android Widget (2026-01-04 - 2026-01-05) ✅
- **Native Kotlin-Implementierung**
- **Live-Timer** mit 1-Sekunden-Updates
- **Widget-Steuerung**: Start/Pause/Stop Buttons
- **Bidirektionale Synchronisation** Widget ↔ App
- **React Native Bridge** für Kommunikation
- **Modernes Design** mit Farbverlauf
- Bug-Fixes: Rundungsfehler, Adressformatierung, Widget-Kommunikation

#### Dark Mode (2026-01-04) ✅
- Vollständige Dark Mode Unterstützung in allen Screens
- `useThemeColors()` Hook für konsistente Theming
- Separate Chart-Farbpaletten für Light/Dark
- Alle hartcodierten Farben entfernt

### Nächste Schritte (Optional)

**Phase 13 - Erweiterte Features:**
- Performance-Optimierungen
- Infinite Scroll für lange Listen
- Cloud-Sync (Firebase/Supabase)
- Multi-Language Support

Details in [TODO.md](TODO.md)

## 📄 Lizenz

Private Projekt - Alle Rechte vorbehalten

## 🐛 Issues & Feedback

Bei Problemen oder Verbesserungsvorschlägen bitte ein Issue erstellen.

---

Entwickelt mit ❤️ für Dachdecker
