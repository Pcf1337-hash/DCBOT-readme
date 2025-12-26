# 🎵 Groove Master 3000 - Discord Music Bot

Ein hochperformanter Discord Music Bot mit persistentem UI, modularer Architektur und Enterprise-Grade Features.

## ✨ Features

- **12 interaktive Buttons** - Vollständige Kontrolle über die Musik
- **Multi-Plattform Support** - YouTube, SoundCloud, Bandcamp, Mixcloud, Vimeo
- **Live Progress Bar** - Echtzeit-Updates alle 5 Sekunden
- **Latency Display** - Zeigt Bot- und Voice-Latenz für Troubleshooting
- **YouTube Link Display** - Direkter Zugriff auf aktuelle Song-URLs
- **Intelligente Queue** - Bis zu 20 Songs mit Shuffle & Repeat
- **Radio Mode** - Automatische ähnliche Songs
- **Robuste Fehlerbehandlung** - Mit automatischen Reconnects
- **Thread Safety** - Race Condition Prevention mit Locks
- **Optimiertes Caching** - Schnelle Downloads, keine Duplikate
- **Strukturiertes Logging** - JSON Format für Monitoring
- **Input Validation** - URL Whitelist & Sanitization
- **Rate Limiting** - Schutz vor Spam
- **Automatisches Queue-Backup** - Persistence alle 10 Minuten

## 📋 Installation

### Voraussetzungen

- Python 3.10+
- FFmpeg
- Discord Bot Token
- YouTube API Key (optional)

### Schritt-für-Schritt

```bash
# Repository klonen
git clone https://github.com/Pcf1337-hash/BOTNEUENEU.git
cd BOTNEUENEU

# Dependencies installieren
pip install -r requirements.txt

# FFmpeg installieren
# Linux: sudo apt install ffmpeg
# macOS: brew install ffmpeg
# Windows: https://ffmpeg.org/download.html

# .env Datei erstellen
cat > .env << EOF
DISCORD_BOT_TOKEN=dein_token_hier
YOUTUBE_API_KEY=dein_key_hier
EOF

# Bot starten
python3 main.py
```

## 🎮 Befehle

| Befehl | Aliases | Beschreibung |
|--------|---------|-------------|
| `!play <URL/Suche>` | `!p` | Song abspielen |
| `!stop` | — | Bot stoppen & disconnecten |
| `!panel` | — | Control Panel anzeigen |
| `!voicereset` | `!vr` | Voice Connection resetten |
| `!status` | — | Bot Status anzeigen |
| `!help` | `!h` | Hilfe anzeigen |

## 🎵 Unterstützte Plattformen

| Plattform | Unterstützung | Features |
|-----------|--------------|----------|
| 🎵 **YouTube** | ✅ Vollständig | Videos, Musik, Livestreams* |
| 🎧 **SoundCloud** | ✅ Vollständig | Tracks, Playlists |
| 🎸 **Bandcamp** | ✅ Vollständig | Indie-Künstler, Albums |
| 🎛️ **Mixcloud** | ✅ Vollständig | DJ Sets, Radio Shows |
| 🎬 **Vimeo** | ✅ Vollständig | Audio-Extraktion |

*Livestreams werden nicht unterstützt

## 🎛️ Die 12 Buttons

| Button | Funktion |
|--------|----------|
| ⏮️ | Vorheriger Song |
| ⏯️ | Play/Pause |
| ⏭️ | Skip |
| 🔁 | Repeat-Modus (Off → 🔁 Playlist → 🔂 Track) |
| 🔀 | Shuffle Queue |
| 📻 | Radio Mode |
| 🔊 | Lautstärke ändern |
| ⏩ | Zu Zeit springen |
| ➕ | Song hinzufügen |
| 📋 | Queue anzeigen (mit YouTube Links) |
| 🗑️ | Queue leeren |
| ⏹️ | Stop & Disconnect |

## 🏗️ Projektstruktur

```
BOTNEUENEU/
├── main.py                 # Einstiegspunkt
├── core/
│   ├── __init__.py
│   ├── bot.py              # Bot-Initialisierung & Setup
│   └── config.py           # Konfiguration & Konstanten
├── models/
│   ├── __init__.py
│   └── song.py             # Song & GuildMusicState Datenklassen
├── managers/
│   ├── __init__.py
│   └── download.py         # Download-Manager mit Caching
├── commands/
│   ├── __init__.py
│   ├── music.py            # Musik-Befehle & Logik
│   ├── events.py           # Event-Handler (on_ready, on_voice_state_update)
│   └── tasks.py            # Hintergrund-Tasks (Panel-Updates, Cleanup)
├── ui/
│   ├── __init__.py
│   └── views.py            # UI-Komponenten (13 Buttons + 3 Modals)
├── utils/
│   ├── __init__.py
│   ├── logging.py          # JSON Logging-System
│   ├── validation.py       # Eingabe-Validierung & Sicherheit
│   ├── performance.py      # Performance-Monitor & Rate-Limiter
│   ├── youtube.py          # YouTube API-Integration
│   └── helpers.py          # Hilfsfunktionen
└── requirements.txt        # Python-Abhängigkeiten
```

## ⚙️ Konfiguration

Bearbeite `core/config.py` für diese Einstellungen:

```python
QUEUE_LIMIT = 20              # Maximale Songs in der Queue
UPDATE_INTERVAL = 5           # Panel-Update-Intervall (Sekunden)
DOWNLOADS_DIR = "downloads"   # Download-Verzeichnis
VOICE_TIMEOUT = 30            # Voice-Verbindungs-Timeout (Sekunden)
```

## 🔍 Protokollierung

Der Bot erstellt automatisch Protokoll-Dateien:

- **`music_bot.log`** - Alle Events im JSON-Format
- **`music_bot_errors.log`** - Nur Fehler mit Stack Traces

## 🔒 Sicherheit

- ✅ URL-Whitelist (YouTube, SoundCloud, Bandcamp, Mixcloud, Vimeo)
- ✅ Eingabe-Bereinigung (max. 2000 Zeichen für URLs, 200 für Suchanfragen)
- ✅ Rate-Limiting pro Benutzer (konfigurierbar)
- ✅ XSS/Injection-Schutz
- ✅ API-Schlüssel in `.env` (nicht im Code)
- ✅ Command-Injection-Schutz

## 🚀 Deployment

### Heroku

```bash
# Procfile
worker: python3 main.py

# Buildpacks hinzufügen
heroku buildpacks:add heroku/python
heroku buildpacks:add https://github.com/jonathanong/heroku-buildpack-ffmpeg-latest

# Konfiguration setzen
heroku config:set DISCORD_BOT_TOKEN=...
heroku config:set YOUTUBE_API_KEY=...
```

### Docker

```dockerfile
FROM python:3.10-slim
RUN apt-get update && apt-get install -y ffmpeg
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . .
CMD ["python3", "main.py"]
```

## 📦 Abhängigkeiten

Hauptabhängigkeiten (siehe `requirements.txt`):

- `discord.py==2.4.0` - Discord API
- `yt-dlp>=2024.12.13` - Video-Downloads
- `PyNaCl>=1.5.0` - Voice-Unterstützung
- `google-api-python-client>=2.149.0` - YouTube API
- `python-dotenv>=1.0.1` - Umgebungsvariablen
- `aiofiles>=23.2.1` - Asynchrone Datei-Operationen
- `psutil>=6.1.0` - Performance-Überwachung

## 🐛 Troubleshooting

### Bot verbindet nicht zum Voice Channel
- Stelle sicher, dass du in einem Voice Channel bist
- Prüfe Bot-Berechtigungen (Voice Connect, Speak)
- Versuche `!voicereset`

### Kein Audio wird abgespielt
- FFmpeg installiert? `ffmpeg -version`
- FFmpeg im PATH? (Windows)
- Prüfe `music_bot_errors.log`

### Download-Fehler
- Internetverbindung prüfen
- Manche Videos sind regional gesperrt
- Live-Streams werden nicht unterstützt
- Bot versucht automatisch erneut (konfigurierbar)

### YouTube API-Fehler
- API-Schlüssel korrekt in `.env`?
- API-Kontingent prüfen (1.000.000 Einheiten/Tag)
- Bot funktioniert auch ohne API-Schlüssel (direkter Download)

### ModuleNotFoundError
```bash
# Stelle sicher, dass alle Abhängigkeiten installiert sind
pip3 install -r requirements.txt

# Bei Python-Versions-Warnung (Python 3.10)
# Die Warnung wird automatisch unterdrückt, da Python 3.10 bis 2026 unterstützt wird
```

## 🔧 Entwicklung

### Code-Struktur

- **Modulare Architektur** - Klare Trennung der Zuständigkeiten
- **Async/Await** - Performante I/O-Operationen
- **Thread-Safe** - Locks für Queue-Operationen
- **Fehlerbehandlung** - Umfassende Exception-Behandlung
- **Type Hints** - Bessere IDE-Unterstützung

### Hintergrund-Tasks

1. **auto_update_panel** - Aktualisiert Control Panel alle 5s
2. **cleanup_task** - Löscht alte Downloads jede Stunde
3. **queue_backup_task** - Speichert Queue alle 10 Minuten
4. **voice_recovery_task** - Verbindungswiederherstellung bei Abbruch alle 30s

### Event-Handler

- `on_ready` - Bot-Initialisierung & Task-Start
- `on_guild_remove` - Aufräumen bei Server-Entfernung
- `on_voice_state_update` - Auto-Disconnect wenn Bot alleine
- `on_command_error` - Globale Fehlerbehandlung

## 🤝 Mitwirken

Pull Requests sind willkommen! Für größere Änderungen bitte zuerst ein Issue öffnen.

### Code-Stil
- Folge PEP 8
- Verwende Type Hints
- Umfassende Docstrings
- Fehlerbehandlung für alle async-Operationen

## 📄 Lizenz

MIT License - siehe LICENSE Datei

## 📞 Support

Bei Problemen:
1. Prüfe die Troubleshooting-Sektion
2. Schaue in `music_bot.log` und `music_bot_errors.log`
3. Erstelle ein GitHub Issue mit:
   - Fehlermeldung
   - Relevante Logs
   - Schritte zur Reproduktion
   - Python-Version (`python3 --version`)
   - Betriebssystem & FFmpeg-Version

## 🔄 Änderungshistorie

### Aktuell (2025-12-26)
- ✅ Feature: Drei-Status Repeat-Button (Off → 🔁 Playlist → 🔂 Track)
- ✅ Verbesserung: Panel-Layout optimiert - 3 Reihen statt 4 für harmonische Darstellung
- ✅ Verbesserung: Refresh-Button entfernt (automatische Updates machen ihn überflüssig)
- ✅ Bugfix: Radio Mode Zuverlässigkeit verbessert
- ✅ Update: Dependencies auf neueste Versionen aktualisiert (yt-dlp 2024.12.13, google-api 2.149.0)
- ✅ Aufräumen: Überflüssige Dateien entfernt (start.bat, start.sh, MEGA_OPTIMIZATION_PROMPT.md)

### Version 2025-12-26 (früher)
- ✅ Feature: Multi-Plattform Support erweitert (Bandcamp, Mixcloud, Vimeo)
- ✅ Feature: Latenz-Anzeige im Control Panel (Bot & Voice Latenz)
- ✅ Feature: YouTube-Link-Anzeige in Queue-Ansicht
- ✅ Feature: Stop-Button (⏹️) für schnellen Disconnect
- ✅ Bugfix: Track-Seek überspringt nicht mehr die Queue
- ✅ Bugfix: Korrekte Locks für alle State-Zugriffe (Race Condition Prevention)

### Vorherige Version (2025-12-21)
- ✅ Bugfix: Python-Versions-Warnung unterdrückt
- ✅ Bugfix: Nicht existierende Modul-Imports entfernt (VoiceClientManager, EmbedFactory)
- ✅ Refactoring: InputValidator für Sicherheit integriert
- ✅ Refactoring: Befehle in music.py, events.py, tasks.py modularisiert
- ✅ Großes Refactoring: Thread-Sicherheit & Race-Condition-Fixes
- ✅ Komplette Umstrukturierung: Flache Modul-Hierarchie
- ✅ Umfassende Fehlerbehandlung hinzugefügt
- ✅ Queue-Persistenz implementiert

---

**Gemacht mit ❤️ für die Discord-Community**
