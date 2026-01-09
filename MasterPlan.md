# 🧠 OVERTHINKING SURVIVORS - MASTER PLAN
**Projekt-Codename:** OverthinkingSurvivors  
**Engine:** Unity 6.3 LTS  
**Render Pipeline:** Universal Render Pipeline (URP)  
**Zielplattform:** PC (Windows/Linux) + Multiplayer  
**Sprache:** Deutsch  
**Genre:** Fun Co-op Survival gegen Overthinking-Monster  
**Entwicklungszeit:** 5-7 Monate  
**Schwierigkeitsgrad:** Anfängerfreundlich mit erweiterten Features  

---

## 🎮 SPIELKONZEPT

### Overthinking-Thematik
Du spielst eine Person, die von ihren eigenen Gedanken überwältigt wird. Sorgen, Zweifel, Ängste und negative Gedanken manifestieren sich als Monster, die dich angreifen. Mit "Klarheits-Werkzeugen" wie Meditation, Sport, Musik und positivem Denken bekämpfst du deine Overthinking-Manifestationen!

**Gegner-Typen:**
- 💭 **Die Sorge** (langsam, viel HP) - "Was wenn...?"
- 😰 **Der Zweifel** (mittel, normal) - "Das schaffst du nie!"
- 🌪️ **Die Panik** (schnell, wenig HP) - "ALLES IST SCHRECKLICH!"
- 😴 **Die Prokrastination** (sehr langsam, blockiert) - "Mach ich später..."

**Waffen = Klarheits-Tools:**
- 🧘 **Meditation** (Nahkampf, beruhigt Gedanken)
- 🎵 **Musik** (Mittelstrecke, lenkt ab)
- 🏃 **Sport** (Nahkampf, stark, verbraucht Energie)
- 📝 **Journaling** (Fernkampf, sortiert Gedanken)
- ☕ **Kaffee** (Boost-Item, Speed +50%)

**Charakter-Sprüche (Lustig):**
- "Natürlich denke ich zu viel... klassisch ich!"
- "Das wird schon... ODER DOCH NICHT?!"
- "Warum bin ich so?"
- "Moment, habe ich den Herd ausgemacht?"
- "Ich brauch 'ne Pause... vom Denken!"

---

## 📋 QUICK START FÜR CLAUDE

### ⚡ WICHTIG: AUTONOME AGENTEN-ARBEITSWEISE
**Jeder Agent arbeitet ALLE seine Tasks in EINER Session komplett ab!**

Wenn du einen Agenten aktivierst:
1. Arbeite ALLE Tasks des Agenten nacheinander ab
2. Erstelle ALLE Scripts, Assets, Konfigurationen
3. Update den Status NACH jedem Task
4. Erst wenn ALLE Tasks ✅ sind, frage ob der nächste Agent aktiviert werden soll

**Du musst NICHT für jeden Task einzeln fragen!**

### Standard-Workflow:
```bash
# 1. MasterPlan.md öffnen
# 2. Aktiven Agenten identifizieren
# 3. ALLE Tasks des Agenten abarbeiten (in einer Session!)
# 4. Status komplett updaten
# 5. Nächsten Agenten vorschlagen
```

---

## 🎯 PROJEKT-STATUS

### Aktueller Stand
```yaml
Projekt-Phase: SETUP
Aktiver Agent: Agent-01 (Projekt-Setup)
Fortschritt Gesamt: 0%
Letztes Update: [WIRD VON CLAUDE AUSGEFÜLLT]
Nächster Meilenstein: "Lauffähiges Unity-Projekt mit deutscher Lokalisierung"
```

### Milestone-Übersicht (5-7 Monate)
- [ ] **M1 - Projekt Setup** (Woche 1-2)
- [ ] **M2 - Core Systems** (Woche 3-4)
- [ ] **M3 - Player Mechanics** (Woche 5-6)
- [ ] **M4 - Character Editor** (Woche 7-8)
- [ ] **M5 - Klarheits-Tools (Waffen)** (Woche 9-10)
- [ ] **M6 - Overthinking-Manifestationen (AI)** (Woche 11-12)
- [ ] **M7 - UI & HUD (Deutsch)** (Woche 13-14)
- [ ] **M8 - Audio & Sprüche** (Woche 15-16)
- [ ] **M9 - Level & Polish** (Woche 17-18)
- [ ] **M10 - Multiplayer-System** (Woche 19-22)
- [ ] **M11 - Testing & Optimization** (Woche 23-24)

---

## 🤖 AGENTEN-SYSTEM

### Agent-01: PROJEKT-SETUP AGENT
**Status:** 🔴 AKTIV  
**Verantwortlich für:** Unity-Projekt, Ordnerstruktur, Git, Packages, Deutsche Lokalisierung  
**Dependencies:** Keine  
**Geschätzte Dauer:** 2-4 Stunden  
**Arbeitsweise:** Führt ALLE 7 Tasks in EINER Session aus

#### Tasks (Alle nacheinander abarbeiten):

**TASK-01-01: Unity-Projekt erstellen**
```yaml
Action:
  - Unity Hub öffnen
  - New Project → 3D (URP) Template
  - Projektname: "OverthinkingSurvivors"
  - Location: [Gewünschter Pfad]
  - Unity Version: 6.3 LTS (oder neueste LTS)
  - Template: 3D (URP)
  - Create Project

Ergebnis:
  - Lauffähiges Unity-Projekt
  - URP bereits konfiguriert
  - Sample Scene vorhanden
```

**TASK-01-02: Git-Repository initialisieren**
```yaml
Action:
  - Terminal im Projektordner öffnen
  - git init
  - .gitignore erstellen (siehe Template unten)
  - .gitattributes erstellen (siehe Template unten)
  - git add .
  - git commit -m "Initial commit: OverthinkingSurvivors Setup"

Dateien erstellen:
  - .gitignore (komplette Liste unten)
  - .gitattributes (Git LFS Config)
  - README.md (siehe Template)
```

**TASK-01-03: Ordnerstruktur erstellen**
```yaml
Action: Alle Ordner im Unity-Editor erstellen (Assets-Fenster)

Struktur:
Assets/
  _Dev/                          # Experimenteller Bereich
  !OverthinkingSurvivors/        # Hauptprojekt
      Animations/
          Characters/
              Player/
              Manifestationen/
      Art/
          Materials/
          Models/
              Characters/
                  Player/
                      BodyParts/  # Für Character Editor
                  Manifestationen/
              Environment/
                  MentalScapes/   # Mentale Landschaften
              ClarityTools/       # Waffen-Modelle
          Textures/
              UI/
              Characters/
              Environment/
      Audio/
          Music/
              Menu/
              Gameplay/
          SFX/
              ClarityTools/       # Waffen-Sounds
              Manifestationen/    # Gegner-Sounds
              Player/
                  Sprueche/       # Lustige Sprüche!
              Ambient/
          Voice/                  # Charakter-Sprüche
      Localization/               # Deutsche Texte
          Strings/
      Prefabs/
          Characters/
              Player/
              Manifestationen/
          Environment/
          UI/
              Menus/
          ClarityTools/
          VFX/
          Multiplayer/            # Netzwerk-Prefabs
      Scenes/
          Menu/
          Gameplay/
          CharacterEditor/
      Scripts/
          AI/
          Core/
          Gameplay/
          Managers/
          Player/
          UI/
          ClarityTools/
          CharacterEditor/
          Multiplayer/            # Netcode Scripts
          Localization/
      ScriptableObjects/
          ClarityTools/
          Manifestationen/
          Items/
          CharacterParts/         # Für Editor
      UI/
          Sprites/
          Fonts/
  Plugins/                        # Third-Party unverändert
```

**TASK-01-04: Essential Packages installieren**
```yaml
Action: Window → Package Manager → Install

Packages:
  - Input System (New Input System) - v1.7+
  - Cinemachine - v2.9+
  - ProBuilder - v5.2+
  - TextMeshPro - v3.0+
  - AI Navigation (NavMesh Components) - v1.1+
  - Netcode for GameObjects - v1.8+ (FÜR MULTIPLAYER!)
  - Unity Transport - v2.0+ (FÜR MULTIPLAYER!)

Nach Installation: Neustart akzeptieren wenn gefordert
```

**TASK-01-05: Unity Editor Settings konfigurieren**
```yaml
Action: Edit → Project Settings

Editor Settings:
  Version Control Mode: Visible Meta Files
  Asset Serialization Mode: Force Text
  Default Behavior Mode: 3D
  Enter Play Mode Options: 
    - ✅ Enter Play Mode Settings aktivieren
    - ❌ Reload Domain (schnellere Iteration)

Player Settings:
  Company Name: [DEIN NAME]
  Product Name: OverthinkingSurvivors
  Default Icon: [Später hinzufügen]
  
Quality Settings:
  - URP-Medium als Default setzen
  - VSync: Every V Blank (für stabile 60 FPS)

Physics Settings:
  Layer Collision Matrix konfigurieren:
    - Player kollidiert mit: Ground, Manifestationen
    - Manifestationen kollidieren mit: Ground, Player
```

**TASK-01-06: Layer & Tags Setup**
```yaml
Action: Edit → Project Settings → Tags and Layers

Layers:
  0  - Default
  1  - TransparentFX
  2  - Ignore Raycast
  3  - Ground
  4  - Water
  5  - UI
  6  - Player
  7  - Manifestation (Gegner)
  8  - ClarityTool (Waffen)
  9  - Pickups
  10 - Environment
  11 - NetworkObject

Tags:
  - Player
  - Manifestation
  - ClarityTool
  - Pickup
  - Ground
  - Spawner
  - NetworkPlayer
```

**TASK-01-07: Basis-Szenen erstellen**
```yaml
Action: File → New Scene

Szenen erstellen:
  1. MainMenu (in Scenes/Menu/)
     - Canvas mit Logo
     - Buttons: Spielen, Character Editor, Einstellungen, Beenden
     - Background (mentale Landschaft)
  
  2. CharacterEditor (in Scenes/CharacterEditor/)
     - Leere Szene für späteren Character Editor
  
  3. GameLevel_01 (in Scenes/Gameplay/)
     - Directional Light
     - Plane (Ground) - Tag: Ground, Layer: Ground
     - Player Spawn Point (Empty GameObject)
     - Event System (für UI)
  
  4. TestScene (in _Dev/)
     - Für schnelle Tests

Alle Szenen speichern!
Build Settings: File → Build Settings → Add Open Scenes
```

**TASK-01-08: Deutsche Lokalisierung vorbereiten**
```yaml
Action: Localization-System aufsetzen

1. Ordner erstellen: Assets/!OverthinkingSurvivors/Localization/Strings/

2. C# Script erstellen: LocalizationManager.cs
   Location: Scripts/Managers/LocalizationManager.cs
   
3. JSON erstellen: de_DE.json in Localization/Strings/
   Initiale Strings:
   {
     "ui_main_menu_play": "Spielen",
     "ui_main_menu_character": "Charakter",
     "ui_main_menu_settings": "Einstellungen",
     "ui_main_menu_quit": "Beenden",
     "ui_game_health": "Mentale Gesundheit",
     "ui_game_confidence": "Selbstvertrauen",
     "ui_game_wave": "Welle",
     "ui_game_killed": "Besiegt"
   }

4. LocalizedText.cs Component erstellen
   - Automatisch TextMeshPro-Text auf Deutsch setzen
```

**TASK-01-09: README.md und Dokumentation**
```yaml
Action: Dateien im Root erstellen

1. README.md (siehe Template unten)
2. CHANGELOG.md (leer, für Updates)
3. CREDITS.md (Asset-Quellen)
4. BUGS.md (für Bug-Tracking)

Alle Dateien in Git committen
```

**TASK-01-10: Initiales Git Commit**
```yaml
Action:
  git add .
  git commit -m "feat: Complete project setup with German localization"
  
Status updaten: Agent-01 auf ✅ ABGESCHLOSSEN
Nächster Agent: Agent-02 vorschlagen
```

**Fertigstellungskriterien Agent-01:**
- ✅ Unity-Projekt läuft fehlerfrei
- ✅ Alle Packages installiert
- ✅ Ordnerstruktur vollständig
- ✅ Layers & Tags konfiguriert
- ✅ Basis-Szenen vorhanden
- ✅ Deutsche Lokalisierung vorbereitet
- ✅ Git-Repository initialisiert
- ✅ Dokumentation erstellt

---

### Agent-02: CORE SYSTEMS AGENT
**Status:** ⚪ WARTEND  
**Verantwortlich für:** Mental-Health-System, Schaden, GameManager, Events, Object Pooling  
**Dependencies:** Agent-01 ✅  
**Geschätzte Dauer:** 6-8 Stunden  
**Arbeitsweise:** Führt ALLE 7 Tasks in EINER Session aus

#### Tasks (Alle nacheinander abarbeiten):

**TASK-02-01: Mental-Health-System (statt Health)**
```yaml
Datei: Scripts/Core/MentalHealth.cs

Features:
  - MaxMentalHealth (z.B. 100)
  - CurrentMentalHealth
  - MaxConfidence (Shield = Selbstvertrauen)
  - CurrentConfidence
  - TakeMentalDamage(float damage)
  - RestoreConfidence(float amount)
  - Heal(float amount)
  - OnMentalBreakdown Event (statt OnDeath)
  - OnConfidenceLost Event

Kommentare auf Deutsch!
```

**TASK-02-02: IDamageable Interface**
```yaml
Datei: Scripts/Core/IDamageable.cs

Interface:
  void TakeMentalDamage(float damage);
  bool IsStable { get; } // statt IsAlive
```

**TASK-02-03: GameManager Singleton**
```yaml
Datei: Scripts/Managers/GameManager.cs

Features:
  - GameState: MainMenu, CharacterEditor, Playing, Paused, GameOver
  - StartGame()
  - PauseGame()
  - ResumeGame()
  - MentalBreakdown() // statt GameOver
  - ReturnToMainMenu()
  - LoadCharacterEditor()
  - QuitGame()

Alle Strings auf Deutsch (Debug.Log etc.)
```

**TASK-02-04: Event-System**
```yaml
Datei: Scripts/Core/GameEvents.cs

Events:
  - OnPlayerMentalBreakdown
  - OnManifestationDefeated (statt OnZombieKilled)
  - OnWaveComplete
  - OnClarityToolUsed (statt OnWeaponFired)
  - OnConfidenceRestored

Verwendung: UnityEvent-basiert
```

**TASK-02-05: Object Pool System**
```yaml
Datei: Scripts/Core/ObjectPool.cs

Generic Pool für:
  - Manifestationen (Gegner)
  - Projektile (falls ranged Clarity Tools)
  - VFX (Partikel)
  - Loot-Drops

Features:
  - GetFromPool(position, rotation)
  - ReturnToPool(GameObject)
  - ReturnAllToPool()
  - InitialPoolSize, CanGrow
```

**TASK-02-06: Audio Manager**
```yaml
Datei: Scripts/Managers/AudioManager.cs

Features:
  - PlaySFX(AudioClip clip, Vector3 position)
  - PlayMusic(AudioClip clip, bool loop)
  - PlayCharacterSpruche(string spruchID) // Lustige Sprüche!
  - SetMusicVolume(float volume)
  - SetSFXVolume(float volume)
  - FadeMusic(float duration)

Singleton-Pattern
```

**TASK-02-07: Sprüche-System**
```yaml
Datei: Scripts/Gameplay/CharacterSprueche.cs

Features:
  - Dictionary mit Spruch-IDs und Texten
  - PlayRandomSpruch(SpruchType type)
  - SpruchTypes: OnDamage, OnKill, OnLowHealth, OnPickup, OnWaveStart

Sprüche:
  OnDamage:
    - "Autsch! Das tut mental weh..."
    - "Typisch ich, wieder zu empfindlich!"
    - "Das wird schon... oder?"
  
  OnKill:
    - "Einen Gedanken weniger!"
    - "Das schaffst du nie? DOCH!"
    - "Klarheit siegt!"
  
  OnLowHealth:
    - "Ich brauch 'ne Pause..."
    - "Das wird zu viel!"
    - "Atmen... einfach atmen..."
  
  OnPickup:
    - "Das hilft!"
    - "Genau was ich brauchte!"
    - "Motivation gefunden!"
```

**Fertigstellungskriterien Agent-02:**
- ✅ MentalHealth-System funktioniert
- ✅ GameManager verwaltet States
- ✅ Event-System kommuniziert
- ✅ Object Pool wiederverwendet Objekte
- ✅ Audio Manager spielt Sounds
- ✅ Sprüche-System kann Texte ausgeben

---

### Agent-03: PLAYER MECHANICS AGENT
**Status:** ⚪ WARTEND  
**Verantwortlich für:** Movement, Kamera, Input, Sprüche-Integration  
**Dependencies:** Agent-02 ✅  
**Geschätzte Dauer:** 8-10 Stunden  
**Arbeitsweise:** Führt ALLE 6 Tasks in EINER Session aus

#### Tasks:

**TASK-03-01: Input System Setup**
```yaml
Action: Create → Input Actions
Name: PlayerInputActions

Actions definieren:
  Movement (Vector2) - WASD
  Look (Vector2) - Mouse
  Jump (Button) - Space
  Sprint (Button) - Shift
  Crouch (Button) - Ctrl
  UseClarityTool (Button) - Left Mouse
  Reload (Button) - R
  SwitchClarityTool1-5 (Button) - 1,2,3,4,5
  Pause (Button) - ESC
  
Generate C# Class aktivieren
```

**TASK-03-02: Player Movement**
```yaml
Datei: Scripts/Player/PlayerMovement.cs

Features:
  - CharacterController-basiert
  - Walk Speed: 5 m/s
  - Sprint Multiplier: 1.8x
  - Crouch Speed: 0.5x
  - Jump Height: 2m
  - Gravity: -19.62 m/s²
  
Kommentare auf Deutsch:
  // Bewegungsgeschwindigkeit berechnen
  // Gravitation anwenden
  // Sprung durchführen
```

**TASK-03-03: Mouse Look (First Person)**
```yaml
Datei: Scripts/Player/MouseLook.cs

Features:
  - Mouse Sensitivity: 100 (anpassbar)
  - Vertical Clamp: -90° bis +90°
  - Horizontal Rotation: Player Body
  - Vertical Rotation: Camera Transform
  - Cursor Lock/Unlock
```

**TASK-03-04: Player Prefab erstellen**
```yaml
Hierarchy erstellen:
  Player (GameObject)
    - Tag: Player
    - Layer: Player
    - Components:
        - CharacterController (Height: 2, Radius: 0.5)
        - PlayerMovement.cs
        - MentalHealth.cs
        - AudioSource (für Sprüche)
    
    └─ CameraHolder (Empty, Position Y: 1.6)
         └─ MainCamera
              - Tag: MainCamera
              - Components: Camera, MouseLook.cs

Als Prefab speichern: Prefabs/Characters/Player/Player.prefab
```

**TASK-03-05: Sprüche-Integration beim Player**
```yaml
Datei: Scripts/Player/PlayerSpruchTrigger.cs

Features:
  - Referenz zu CharacterSprueche.cs
  - Bei TakeMentalDamage() → Spruch abspielen
  - Bei Manifestation besiegt → Spruch
  - Bei Low Mental Health → Spruch
  - Cooldown zwischen Sprüchen (5 Sekunden)

AudioSource nutzen für Text-to-Speech oder Audio-Clips
```

**TASK-03-06: Player Health UI Connection**
```yaml
Datei: Scripts/Player/PlayerMentalHealth.cs

Erbt von MentalHealth.cs
Features:
  - Verbindung zu HUD (später von Agent-07)
  - OnMentalHealthChanged Event → UI Update
  - OnConfidenceChanged Event → UI Update
  - OnMentalBreakdown → Game Over
```

**Fertigstellungskriterien Agent-03:**
- ✅ Player bewegt sich flüssig (WASD)
- ✅ Sprint/Jump/Crouch funktioniert
- ✅ Mouse Look funktioniert
- ✅ Player Prefab vollständig
- ✅ Sprüche werden getriggert
- ✅ Mental Health System verbunden

---

### Agent-04: CHARACTER EDITOR AGENT
**Status:** ⚪ WARTEND  
**Verantwortlich für:** Charakter-Anpassung, Body Parts, Farben, Speicherung  
**Dependencies:** Agent-03 ✅  
**Geschätzte Dauer:** 10-12 Stunden  
**Arbeitsweise:** Führt ALLE 8 Tasks in EINER Session aus

#### Tasks:

**TASK-04-01: Character Data ScriptableObject**
```yaml
Datei: Scripts/ScriptableObjects/CharacterPartData.cs

Properties:
  - PartType (Enum: Hair, Face, Body, Legs, Shoes)
  - PartName (string)
  - PartModel (GameObject)
  - PreviewIcon (Sprite)
  - UnlockLevel (int, für später)
```

**TASK-04-02: Character Customization Manager**
```yaml
Datei: Scripts/CharacterEditor/CharacterCustomizationManager.cs

Features:
  - CurrentCharacterData (speichert Auswahl)
  - EquipPart(PartType type, CharacterPartData data)
  - RemovePart(PartType type)
  - SetSkinColor(Color color)
  - SaveCharacter()
  - LoadCharacter()
  
Speicherung: PlayerPrefs (später JSON)
```

**TASK-04-03: Character Editor Scene Setup**
```yaml
Scene: CharacterEditor

Aufbau:
  - UI Canvas (Character Selection UI)
  - Character Preview (Rotation Platform)
  - Lighting (für schöne Darstellung)
  - Camera (Orbital View)
  
UI Elemente:
  - Dropdown: Frisuren
  - Dropdown: Gesichter
  - Color Picker: Hautfarbe
  - Dropdown: Körper
  - Dropdown: Beine
  - Dropdown: Schuhe
  - Button: Speichern (deutsch: "Charakter speichern")
  - Button: Zurück zum Menü
```

**TASK-04-04: Body Parts Prefabs erstellen**
```yaml
Action: Placeholder Body Parts erstellen

Einfache Low-Poly-Cubes als Platzhalter:
  Hair_01, Hair_02, Hair_03 (verschiedene Formen)
  Face_01, Face_02 (verschiedene Gesichter)
  Body_01 (Torso)
  Legs_01 (Beine)
  Shoes_01, Shoes_02

Später: Free Assets von Quaternius ersetzen

Alle als Prefabs in: Prefabs/Characters/Player/BodyParts/
```

**TASK-04-05: CharacterPartData Assets erstellen**
```yaml
Action: ScriptableObjects erstellen

Für jedes Body Part:
  Right-Click → Create → Game → Character Part Data
  
Beispiel: Hair_01_Data
  - PartType: Hair
  - PartName: "Kurze Haare"
  - PartModel: Hair_01 Prefab
  - PreviewIcon: null (später)

Speichern in: ScriptableObjects/CharacterParts/
```

**TASK-04-06: Character Preview Controller**
```yaml
Datei: Scripts/CharacterEditor/CharacterPreview.cs

Features:
  - Rotation mit Maus (Drag)
  - Zoom mit Mausrad
  - Auto-Rotation (optional)
  - Part-Wechsel in Echtzeit
  
Visualisierung der aktuellen Auswahl
```

**TASK-04-07: Character Editor UI**
```yaml
Datei: Scripts/CharacterEditor/CharacterEditorUI.cs

Features:
  - Populate Dropdowns mit CharacterPartData
  - OnDropdownChanged → Preview Update
  - OnColorChanged → Skin Color Update
  - OnSaveClicked → Save & Return to Menu
  - Alle Labels auf Deutsch
  
Deutsche UI-Texte:
  - "Frisur wählen"
  - "Hautfarbe"
  - "Charakter speichern"
  - "Zurück"
```

**TASK-04-08: Character Save/Load System**
```yaml
Datei: Scripts/CharacterEditor/CharacterSaveData.cs

Serializable Class:
  - string selectedHairID
  - string selectedFaceID
  - string selectedBodyID
  - string selectedLegsID
  - string selectedShoesID
  - Color skinColor

Save to PlayerPrefs oder JSON
Load beim Spielstart → Apply to Player Prefab
```

**Fertigstellungskriterien Agent-04:**
- ✅ Character Editor Scene funktioniert
- ✅ Body Parts können gewechselt werden
- ✅ Preview zeigt Character korrekt
- ✅ Speichern/Laden funktioniert
- ✅ Auswahl wird im Spiel angewendet
- ✅ UI komplett auf Deutsch

---

### Agent-05: CLARITY TOOLS AGENT (Waffen)
**Status:** ⚪ WARTEND  
**Verantwortlich für:** "Waffen"-System mit Overthinking-Thematik  
**Dependencies:** Agent-04 ✅  
**Geschätzte Dauer:** 10-12 Stunden  
**Arbeitsweise:** Führt ALLE 7 Tasks in EINER Session aus

#### Tasks:

**TASK-05-01: ClarityToolData ScriptableObject**
```yaml
Datei: Scripts/ScriptableObjects/ClarityToolData.cs

Properties:
  - ToolName (string) - z.B. "Meditation"
  - ToolType (Enum: Melee, Ranged, Boost)
  - Description (string) - "Beruhigt die Gedanken"
  - Damage (float) - "Clarity Power"
  - UseRate (float) - Wie oft nutzbar
  - Range (float) - Reichweite
  - EnergyCost (int) - Energie statt Ammo
  - MaxEnergy (int)
  - RechargeTime (float)
  - ToolPrefab (GameObject)
  - Icon (Sprite)
  - UseSound (AudioClip)
```

**TASK-05-02: ClarityToolBase Class**
```yaml
Datei: Scripts/ClarityTools/ClarityToolBase.cs

Abstract Class:
  - ClarityToolData _toolData
  - float _nextUseTime
  - bool CanUse
  - virtual void Initialize(ClarityToolData data)
  - abstract void UseTool()
  - virtual void Recharge()
  - virtual void PlayUseSound()
```

**TASK-05-03: Meditation Tool (Melee)**
```yaml
Datei: Scripts/ClarityTools/MeditationTool.cs

Extends ClarityToolBase

Features:
  - Nahkampf-Angriff (OverlapSphere)
  - Beruhigungs-Animation
  - Partikel: Blaue Wellen
  - Sound: Beruhigender Gong
  - Damage: 50 (stark aber langsam)
  - Range: 2m
  
Name: "Meditation" (Deutsch)
Description: "Beruhigt selbst die wildesten Gedanken"
```

**TASK-05-04: Musik Tool (Ranged)**
```yaml
Datei: Scripts/ClarityTools/MusikTool.cs

Features:
  - Raycast-basiert
  - Musiknoten als Projektil-VFX
  - Sound: Melodie-Schnipsel
  - Damage: 30
  - Range: 25m
  - Energy: 20 (Max: 100)
  
Name: "Musik" (Deutsch)
Description: "Lenkt Gedanken mit Melodien ab"
```

**TASK-05-05: Sport Tool (Melee, High Damage)**
```yaml
Datei: Scripts/ClarityTools/SportTool.cs

Features:
  - Nahkampf, sehr stark
  - Schweiß-Partikel
  - Sound: Anstrengungs-Geräusche
  - Damage: 75
  - Range: 2.5m
  - EnergyCost hoch: 30/Nutzung
  
Name: "Sport" (Deutsch)
Description: "Kraftvoll gegen Overthinking!"
```

**TASK-05-06: Journaling Tool (Ranged, Präzise)**
```yaml
Datei: Scripts/ClarityTools/JournalingTool.cs

Features:
  - Raycast mit hoher Präzision
  - Schreib-Animation
  - Sound: Stift auf Papier
  - Damage: 40
  - Range: 30m
  - Energy: 15
  
Name: "Tagebuch" (Deutsch)
Description: "Sortiert Gedanken präzise"
```

**TASK-05-07: Clarity Tool Manager & Switching**
```yaml
Datei: Scripts/ClarityTools/ClarityToolManager.cs

Features:
  - List<ClarityToolBase> tools
  - int currentToolIndex
  - SwitchTool(int index) - Tasten 1-5
  - UseCurrent() - Linke Maustaste
  - ReloadCurrent() - R Taste (Recharge)
  - UpdateHUD() - Energy-Anzeige
  
Verbindung zu Input System
```

**TASK-05-08: ClarityToolData Assets erstellen**
```yaml
Action: ScriptableObjects für alle Tools

Create → Game → Clarity Tool Data

Meditation_Data:
  - ToolName: "Meditation"
  - ToolType: Melee
  - Damage: 50
  - UseRate: 0.8s
  - Range: 2m
  - EnergyCost: 0 (unbegrenzt)
  
Musik_Data, Sport_Data, Tagebuch_Data analog

Speichern: ScriptableObjects/ClarityTools/
```

**Fertigstellungskriterien Agent-05:**
- ✅ Alle 4 Clarity Tools funktionieren
- ✅ Tool Switching (1-4 Tasten)
- ✅ Energy-System funktioniert
- ✅ Recharge funktioniert
- ✅ Sounds & VFX (Platzhalter)
- ✅ ScriptableObject-System nutzt deutsche Namen

---

### Agent-06: OVERTHINKING-MANIFESTATIONEN AGENT (AI)
**Status:** ⚪ WARTEND  
**Verantwortlich für:** Gegner-KI mit Overthinking-Thematik  
**Dependencies:** Agent-05 ✅  
**Geschätzte Dauer:** 10-12 Stunden  
**Arbeitsweise:** Führt ALLE 7 Tasks in EINER Session aus

#### Tasks:

**TASK-06-01: NavMesh Setup**
```yaml
Action: Window → AI → Navigation

Settings:
  - Agent Radius: 0.5
  - Agent Height: 2.0
  - Max Slope: 45
  - Step Height: 0.4
  
In GameLevel_01:
  - Ground Plane auswählen → Navigation Static
  - Bake NavMesh
  - Blau = Begehbar validieren
```

**TASK-06-02: ManifestationData ScriptableObject**
```yaml
Datei: Scripts/ScriptableObjects/ManifestationData.cs

Properties:
  - ManifestationName (string) - "Die Sorge"
  - ManifestationType (Enum)
  - MaxMentalHealth (float)
  - MoveSpeed (float)
  - MentalDamage (float) - Schaden den sie verursachen
  - DetectionRange (float)
  - AttackRange (float)
  - AttackCooldown (float)
  - Sprueche (string[]) - Was sie sagen!
  - IdleSounds (AudioClip[])
  - AttackSounds (AudioClip[])
  - DefeatSound (AudioClip)
  - LootDropChance (float)
```

**TASK-06-03: Manifestation AI State Machine**
```yaml
Datei: Scripts/AI/ManifestationAI.cs

States:
  - Wandering (zufällig umherlaufen)
  - Chasing (Spieler verfolgen)
  - Attacking (Spieler angreifen)
  - Defeated (tot)

Features:
  - NavMeshAgent-basiert
  - State-Wechsel basierend auf Distanz
  - Sprüche abspielen während Chase/Attack
  - OnDefeat → Loot droppen, zurück in Pool
```

**TASK-06-04: Manifestations-Typen erstellen**
```yaml
Manifestationstypen (4 Stück):

1. DIE SORGE (Slow Walker)
   - Health: 120
   - Speed: 2.0
   - Damage: 15
   - Sprüche: "Was wenn...?", "Das geht schief!", "Bestimmt passiert was Schlimmes!"
   
2. DER ZWEIFEL (Normal Runner)
   - Health: 80
   - Speed: 3.5
   - Damage: 20
   - Sprüche: "Das schaffst du nie!", "Du bist nicht gut genug!", "Aufgeben?"
   
3. DIE PANIK (Fast Sprinter)
   - Health: 50
   - Speed: 5.5
   - Damage: 25
   - Sprüche: "ALLES IST SCHRECKLICH!", "PANIK!", "HILFE!"
   
4. DIE PROKRASTINATION (Very Slow Blocker)
   - Health: 150
   - Speed: 1.0
   - Damage: 10
   - Sprüche: "Mach ich später...", "Wozu die Eile?", "Lass uns warten..."
```

**TASK-06-05: Manifestation Prefabs erstellen**
```yaml
Action: Platzhalter-Modelle erstellen

Für jeden Typ:
  GameObject mit:
    - NavMeshAgent
    - ManifestationAI.cs
    - MentalHealth.cs
    - Capsule Collider
    - AudioSource
    - Platzhalter-Geometrie (Capsule + Farbe)
  
Farben:
  - Sorge: Grau (düster)
  - Zweifel: Dunkelrot (aggressiv)
  - Panik: Gelb-Orange (hektisch)
  - Prokrastination: Blau-Grau (träge)

Prefabs: Prefabs/Characters/Manifestationen/
```

**TASK-06-06: Manifestation Spawner System**
```yaml
Datei: Scripts/Gameplay/ManifestationSpawner.cs

Features:
  - Wave-System (Welle 1, 2, 3, ...)
  - Spawn Points (List<Transform>)
  - SpawnDelay zwischen Manifestationen
  - Wave-Progression:
      W1: 5x Sorge
      W2: 3x Sorge, 5x Zweifel
      W3: 2x Sorge, 4x Zweifel, 4x Panik
      W4+: Mix mit Prokrastination
  - OnWaveComplete Event
  - Object Pool nutzen!
```

**TASK-06-07: ManifestationData Assets erstellen**
```yaml
Action: Create → Game → Manifestation Data

4 Assets erstellen:
  - Sorge_Data
  - Zweifel_Data
  - Panik_Data
  - Prokrastination_Data

Mit Werten von TASK-06-04

Speichern: ScriptableObjects/Manifestationen/
```

**Fertigstellungskriterien Agent-06:**
- ✅ NavMesh funktioniert
- ✅ Alle 4 Manifestations-Typen vorhanden
- ✅ AI läuft zum Spieler und greift an
- ✅ Sprüche werden abgespielt
- ✅ Wave-System spawnt korrekt
- ✅ Loot-Drops funktionieren

---

### Agent-07: UI & HUD AGENT
**Status:** ⚪ WARTEND  
**Verantwortlich für:** Deutsches UI, HUD, Menüs  
**Dependencies:** Agent-06 ✅  
**Geschätzte Dauer:** 8-10 Stunden  
**Arbeitsweise:** Führt ALLE 6 Tasks in EINER Session aus

#### Tasks:

**TASK-07-01: HUD Canvas Setup**
```yaml
Scene: GameLevel_01

Canvas erstellen:
  - RenderMode: Screen Space - Overlay
  - Canvas Scaler:
      UI Scale Mode: Scale With Screen Size
      Reference Resolution: 1920x1080
      Match: 0.5 (Width/Height)
```

**TASK-07-02: HUD Elements erstellen (Deutsch!)**
```yaml
HUD Layout:

Top-Left:
  - Mental Health Bar (Rot → Grün)
    Label: "Mentale Gesundheit"
    Text: "85/100"
  - Confidence Bar (Blau)
    Label: "Selbstvertrauen"
    Text: "60/100"

Top-Right:
  - Wave Counter
    Label: "Welle:"
    Text: "3"
  - Defeated Counter
    Label: "Besiegt:"
    Text: "25"

Center:
  - Crosshair (Kreuz oder Punkt)

Bottom-Right:
  - Current Clarity Tool
    Icon: [Tool Icon]
    Name: "Meditation"
  - Energy Display
    Text: "∞" oder "75/100"
  - Hint: "[R] Aufladen"

Bottom-Center:
  - Quick Slots (1-4)
    Icons der Tools
    Highlight bei aktuellem Tool
```

**TASK-07-03: HUDManager Script**
```yaml
Datei: Scripts/UI/HUDManager.cs

Features:
  - UpdateMentalHealth(float current, float max)
  - UpdateConfidence(float current, float max)
  - UpdateWave(int waveNumber)
  - UpdateDefeated(int count)
  - UpdateClarityTool(ClarityToolData tool)
  - UpdateEnergy(int current, int max)
  - ShowHint(string hintText)
  
Event-Subscriptions zu GameEvents
Alle Texte auf Deutsch!
```

**TASK-07-04: Main Menu (Deutsch)**
```yaml
Scene: MainMenu

UI Aufbau:
  Background: Mentale Landschaft (verschwommen)
  
  Logo: "OVERTHINKING SURVIVORS" (groß, zentriert)
  
  Buttons (vertikal, zentriert):
    1. "Spielen" → LoadScene("GameLevel_01")
    2. "Charakter" → LoadScene("CharacterEditor")
    3. "Einstellungen" → OpenSettingsPanel()
    4. "Mehrspieler" → OpenMultiplayerMenu()
    5. "Beenden" → QuitGame()
  
  Version Text (unten rechts): "v0.1.0 Alpha"

Script: Scripts/UI/MainMenuController.cs
```

**TASK-07-05: Pause Menu (Deutsch)**
```yaml
Overlay in GameLevel_01:

Panel (halbtransparent schwarz):
  
  Title: "PAUSE"
  
  Buttons:
    1. "Weiterspielen" → ResumeGame()
    2. "Einstellungen" → OpenSettingsPanel()
    3. "Hauptmenü" → ReturnToMainMenu()
    4. "Beenden" → QuitGame()

Trigger: ESC-Taste
Script: Scripts/UI/PauseMenuController.cs
Time.timeScale = 0 beim Pausieren!
```

**TASK-07-06: Game Over Screen (Deutsch)**
```yaml
Overlay in GameLevel_01:

Panel (dunkler, dramatisch):
  
  Title: "MENTALER ZUSAMMENBRUCH"
  
  Stats (zentriert):
    - "Besiegte Gedanken: {count}"
    - "Überlebte Wellen: {waves}"
    - "Spielzeit: {time}"
  
  Buttons:
    1. "Nochmal" → RestartGame()
    2. "Hauptmenü" → ReturnToMainMenu()

Trigger: Player Mental Health <= 0
Script: Scripts/UI/GameOverUI.cs
```

**Fertigstellungskriterien Agent-07:**
- ✅ HUD zeigt alle Werte korrekt
- ✅ Main Menu funktioniert
- ✅ Pause Menu funktioniert
- ✅ Game Over Screen funktioniert
- ✅ Alle Texte auf Deutsch
- ✅ Navigation zwischen Szenen klappt

---

### Agent-08: AUDIO & SPRÜCHE AGENT
**Status:** ⚪ WARTEND  
**Verantwortlich für:** Sounds, Musik, Character-Sprüche (lustig!)  
**Dependencies:** Agent-07 ✅  
**Geschätzte Dauer:** 6-8 Stunden  
**Arbeitsweise:** Führt ALLE 6 Tasks in EINER Session aus

#### Tasks:

**TASK-08-01: Audio Assets sammeln**
```yaml
Quellen:
  - Freesound.org (CC0):
      - "meditation gong" → Meditation-Sound
      - "music notes" → Musik-Tool-Sound
      - "running footsteps" → Sport-Sound
      - "writing paper" → Journaling-Sound
  
  - Kenney.nl (CC0):
      - UI Sounds (Click, Hover)
      - Impact Sounds (Hit-Feedback)
  
Importieren nach:
  Audio/SFX/ClarityTools/
  Audio/SFX/Player/
  Audio/SFX/Manifestationen/
  Audio/SFX/UI/
```

**TASK-08-02: Clarity Tool Audio Implementation**
```yaml
Action: Sounds zu Tools hinzufügen

In ClarityToolData Assets:
  - Meditation_Data.UseSound = Gong-Sound
  - Musik_Data.UseSound = Musiknoten-Sound
  - Sport_Data.UseSound = Anstrengungs-Sound
  - Tagebuch_Data.UseSound = Schreib-Sound

In ClarityToolBase.cs:
  - PlayUseSound() implementieren
  - AudioSource.PlayClipAtPoint nutzen
```

**TASK-08-03: Manifestation Audio Implementation**
```yaml
Action: Sounds zu Manifestationen

Für jeden Typ Audio aufnehmen/finden:
  - IdleSounds (zufällig alle 5-10s)
  - AttackSound (beim Angriff)
  - DefeatSound (beim Tod)

Text-to-Speech nutzen für Sprüche:
  - Sorge: "Was wenn...?" (besorgte Stimme)
  - Zweifel: "Das schaffst du nie!" (spöttisch)
  - Panik: "ALLES IST SCHRECKLICH!" (hektisch)
  - Prokrastination: "Mach ich später..." (gelangweilt)

In ManifestationAI.cs einbinden
```

**TASK-08-04: Player Sprüche Audio**
```yaml
Action: Lustige Sprüche aufnehmen/generieren

CharacterSprueche.cs erweitern:

AudioClips oder Text-to-Speech:
  OnDamage:
    - "Autsch! Das tut mental weh..."
    - "Typisch ich, wieder zu empfindlich!"
    - "Das wird schon... oder?"
  
  OnKill:
    - "Einen Gedanken weniger!"
    - "Das schaffst du nie? DOCH!"
    - "Klarheit siegt!"
  
  OnLowHealth:
    - "Ich brauch 'ne Pause vom Denken..."
    - "Das wird zu viel!"
    - "Atmen... einfach atmen..."
  
  OnPickup:
    - "Das hilft!"
    - "Genau was ich brauchte!"
    - "Motivation +100!"
  
  OnWaveStart:
    - "Hier kommen sie wieder..."
    - "Ich schaff das!"
    - "Overthinking-Alarm!"

AudioSource auf Player-Prefab
Cooldown: 5 Sekunden zwischen Sprüchen
```

**TASK-08-05: Background Music**
```yaml
Action: Musik-Loops finden

Quellen:
  - Incompetech.com (CC-BY)
  - YouTube Audio Library
  
Tracks:
  - MainMenu: Ruhig, nachdenklich
  - Gameplay: Spannend aber nicht zu stressig
  - GameOver: Traurig aber hoffnungsvoll

AudioManager Integration:
  - Fade In/Out zwischen Tracks
  - Volume-Settings respektieren
```

**TASK-08-06: UI Audio**
```yaml
Action: UI-Sounds einbinden

Sounds:
  - Button Hover (subtle)
  - Button Click (befriedigend)
  - Menu Open/Close
  - Error Sound (bei invalider Aktion)

In allen UI-Scripts:
  - OnButtonClick → PlaySFX("UI_Click")
  - OnHover → PlaySFX("UI_Hover")
```

**Fertigstellungskriterien Agent-08:**
- ✅ Clarity Tools haben Sounds
- ✅ Manifestationen machen Geräusche + Sprüche
- ✅ Player sagt lustige Sprüche
- ✅ Background Music läuft
- ✅ UI hat Audio-Feedback
- ✅ AudioManager verwaltet alles

---

### Agent-09: INTEGRATION & POLISH AGENT
**Status:** ⚪ WARTEND  
**Verantwortlich für:** Level-Design, Loot, Balance, Visuals  
**Dependencies:** Agent-08 ✅  
**Geschätzte Dauer:** 10-12 Stunden  
**Arbeitsweise:** Führt ALLE 7 Tasks in EINER Session aus

#### Tasks:

**TASK-09-01: Level Design - Mentale Landschaft**
```yaml
Scene: GameLevel_01

Thema: "Im Kopf des Overthinkers"

ProBuilder nutzen:
  - Arena-Größe: 60x60 Meter
  - Boden: Gitter-Textur (Gedanken-Netzwerk)
  - Hindernisse: Abstrakte Formen (Gedankenwände)
  - Deckung: Fragmentierte Erinnerungen
  - Skybox: Stürmischer Gedankenhimmel (dunkel, wirbelnd)

Farbschema:
  - Boden: Dunkles Grau-Blau
  - Hindernisse: Neon-Akzente (Cyan, Magenta)
  - Fog: Leichter Nebel (Gedankennebel)

Lighting:
  - Directional Light: Kalt, leicht bläulich
  - Point Lights: An strategischen Punkten (warm)
```

**TASK-09-02: Loot-System implementieren**
```yaml
Datei: Scripts/Gameplay/LootDrop.cs

Loot-Typen:
  1. Motivation-Pack (Heilt Mental Health)
  2. Klarheits-Boost (Restored Confidence)
  3. Energie-Drink (Füllt Energy auf)

Features:
  - Drop-Chance: 30% bei Manifestation Defeat
  - Pickup-Trigger: OnTriggerEnter
  - Pickup-Sound + VFX
  - Auto-Despawn nach 30 Sekunden
```

**TASK-09-03: Loot Prefabs**
```yaml
Action: 3 Loot-Prefabs erstellen

1. Motivation_Pack
   - Grüner Würfel + Pulsing-Animation
   - Heilt: +30 Mental Health
   - Sound: Positiver Chime
   
2. Klarheits_Boost
   - Blauer Würfel + Rotation
   - Restored: +40 Confidence
   - Sound: Glocke
   
3. Energie_Drink
   - Gelber Würfel + Bounce
   - Energy: +50
   - Sound: Fizz

Prefabs: Prefabs/UI/Loot/
```

**TASK-09-04: Wave-Progression Balance**
```yaml
Datei: ManifestationSpawner.cs erweitern

Balancierte Wave-Struktur:

Welle 1: Tutorial
  - 5x Sorge (langsam)
  - Kein Zeitdruck
  
Welle 2: Einführung Zweifel
  - 3x Sorge
  - 5x Zweifel
  
Welle 3: Chaos
  - 2x Sorge
  - 4x Zweifel
  - 4x Panik (neu!)
  
Welle 4: Boss-Welle
  - 10x Mixed
  - 1x Prokrastination (Blocker)
  
Welle 5+: Skalierung
  - +20% Gegner pro Welle
  - +10% Health pro Welle
  - Mix aller Typen

Pause zwischen Wellen: 15 Sekunden
```

**TASK-09-05: Game Balance Pass**
```yaml
Action: Alle Werte testen und anpassen

Player Stats:
  - Mental Health: 100
  - Confidence: 100
  - Walk Speed: 5 m/s
  - Sprint Speed: 9 m/s

Clarity Tools Balance:
  Meditation: 50 Dmg, 0.8s Rate, ∞ Energy
  Musik: 30 Dmg, 0.3s Rate, 100 Energy
  Sport: 75 Dmg, 1.0s Rate, 100 Energy (30/use)
  Tagebuch: 40 Dmg, 0.5s Rate, 100 Energy

Manifestationen Balance:
  Sorge: 120 HP, 2.0 Speed, 15 Dmg
  Zweifel: 80 HP, 3.5 Speed, 20 Dmg
  Panik: 50 HP, 5.5 Speed, 25 Dmg
  Prokrastination: 150 HP, 1.0 Speed, 10 Dmg

Loot Drop Chance: 30%
Loot Heal Amounts: 30 HP, 40 Confidence, 50 Energy
```

**TASK-09-06: Skybox & Post-Processing**
```yaml
Action: Visuelle Atmosphäre

Skybox:
  - Free Skybox: "Stormy Days" oder ähnlich
  - Oder: Gradient Skybox (dunkel → hell)
  - Importieren von Unity Asset Store

Lighting:
  - Ambient: Dunkel-Blau
  - Fog aktivieren:
      Color: Blau-Grau
      Density: 0.02
      Start: 10m
      End: 80m

Post-Processing (URP):
  - Volume erstellen (Global)
  - Bloom: Intensity 0.2 (subtle)
  - Color Grading:
      Saturation: -10 (leicht entsättigt)
      Contrast: +5
  - Vignette: Intensity 0.3
  - Grain: Intensity 0.15 (für Unruhe)
```

**TASK-09-07: VFX-Partikel**
```yaml
Action: Einfache Particle Systems

1. Clarity Tool Hit VFX
   - Farbe passend zum Tool
   - Burst beim Treffer
   - Lifetime: 0.5s

2. Manifestation Defeat VFX
   - Explosion in Gegner-Farbe
   - Partikel nach außen
   - Lifetime: 1s

3. Loot Spawn VFX
   - Glitzer-Effekt
   - Pulsing
   - Loop

Prefabs: Prefabs/VFX/
Object Pool nutzen!
```

**Fertigstellungskriterien Agent-09:**
- ✅ Level ist spielbar und interessant
- ✅ Loot-System funktioniert
- ✅ Wave-Balance ist fair
- ✅ Visuals sind atmosphärisch
- ✅ VFX funktionieren
- ✅ Spiel macht Spaß!

---

### Agent-10: MULTIPLAYER AGENT
**Status:** ⚪ WARTEND  
**Verantwortlich für:** Co-op Multiplayer mit Netcode for GameObjects  
**Dependencies:** Agent-09 ✅  
**Geschätzte Dauer:** 14-16 Stunden  
**Arbeitsweise:** Führt ALLE 9 Tasks in EINER Session aus

#### Tasks:

**TASK-10-01: Netcode for GameObjects Setup**
```yaml
Action: Package bereits installiert (Agent-01)

Konfiguration:
  - Window → Package Manager → Netcode for GameObjects
  - Version: Latest (1.8+)
  
Network Manager erstellen:
  - GameObject: "NetworkManager"
  - Add Component: NetworkManager
  - Transport: UnityTransport
```

**TASK-10-02: Network Player Prefab**
```yaml
Action: Player Prefab für Multiplayer anpassen

Player_Network (Kopie von Player):
  - Add Component: NetworkObject
  - Add Component: NetworkTransform (für Position Sync)
  - PlayerMovement.cs → NetworkBehaviour ändern
  - Owner Authority aktivieren
  
Wichtig:
  - IsOwner checks in Movement
  - Nur Owner kann seinen Player steuern
  - Camera nur für Owner aktivieren
```

**TASK-10-03: Multiplayer Menu UI**
```yaml
Scene: MainMenu erweitern

Multiplayer-Panel:
  Buttons:
    - "Host starten" → StartHost()
    - "Spiel beitreten" → StartClient()
  
  Input Field:
    - IP-Adresse (für Client)
    - Port (Standard: 7777)
  
  Status Text:
    - "Warte auf Spieler..."
    - "Verbunden: 2/4 Spieler"

Script: Scripts/Multiplayer/MultiplayerMenuUI.cs
```

**TASK-10-04: Network Connection Manager**
```yaml
Datei: Scripts/Multiplayer/NetworkConnectionManager.cs

Features:
  - StartHost() → Hosting beginnen
  - StartClient(string ip) → Beitreten
  - OnClientConnected → Callback
  - OnClientDisconnected → Cleanup
  - MaxPlayers: 4
  - PlayerList: List<ulong> clientIds

Integration mit NetworkManager
```

**TASK-10-05: Synchronized Wave System**
```yaml
Datei: ManifestationSpawner.cs erweitern

Änderungen:
  - NetworkBehaviour statt MonoBehaviour
  - ServerRpc für Spawning
  - NetworkVariable<int> currentWave
  - Nur Server spawnt Gegner
  - Clients sehen synchronisierte Wellen

[ServerRpc] für Spawn-Funktionen
[ClientRpc] für Wave-Announcements
```

**TASK-10-06: Network Manifestation Sync**
```yaml
Action: Manifestationen netzwerkfähig machen

ManifestationAI.cs erweitern:
  - NetworkBehaviour
  - NetworkTransform für Movement
  - NetworkVariable<float> health
  - [ServerRpc] TakeDamageServerRpc()
  - [ClientRpc] PlaySoundClientRpc()

Manifestation Prefabs:
  - NetworkObject Component
  - In NetworkManager registrieren
```

**TASK-10-07: Shared Loot & Pickups**
```yaml
Action: Loot-System synchronisieren

Loot Prefabs:
  - NetworkObject hinzufügen
  - Pickup nur von einem Spieler
  - Despawn für alle Clients

Script: Scripts/Multiplayer/NetworkPickup.cs
  - [ServerRpc] PickupServerRpc(ulong clientId)
  - [ClientRpc] DespawnClientRpc()
  - Nur Server entscheidet über Pickup
```

**TASK-10-08: Multiplayer HUD**
```yaml
Action: HUD für Multiplayer anpassen

Neue Elements:
  - Player List (Top-Left):
      "Spieler 1: 85 HP"
      "Spieler 2: 70 HP"
  - Team Stats:
      "Gesamt besiegt: 50"
  - Ping Display: "Ping: 25ms"

Script: Scripts/UI/MultiplayerHUD.cs
NetworkVariable-Subscriptions für Updates
```

**TASK-10-09: Network Testing Scene**
```yaml
Scene: MultiplayerTest (in _Dev/)

Setup:
  - Network Manager
  - Spawn Points (4x)
  - Test-Gegner
  - HUD

Lokaler Test:
  - ParrelSync Package installieren (Clone-Editor)
  - Oder: Build + Editor gleichzeitig

Validierung:
  - 2+ Spieler können joinen
  - Bewegung synchronisiert
  - Gegner synchronisiert
  - Loot funktioniert
  - Wellen synchronisiert
```

**Fertigstellungskriterien Agent-10:**
- ✅ Multiplayer-Menu funktioniert
- ✅ Host/Client Connection klappt
- ✅ Player-Movement synchronisiert
- ✅ Gegner für alle sichtbar
- ✅ Loot funktioniert networked
- ✅ Wellen synchronisiert
- ✅ Bis zu 4 Spieler supported
- ✅ Keine groben Desync-Bugs

---

### Agent-11: TESTING & OPTIMIZATION AGENT
**Status:** ⚪ WARTEND  
**Verantwortlich für:** Bug-Fixing, Performance, Final Build  
**Dependencies:** Agent-10 ✅  
**Geschätzte Dauer:** 8-10 Stunden  
**Arbeitsweise:** Führt ALLE 6 Tasks in EINER Session aus

#### Tasks:

**TASK-11-01: Comprehensive Bug Testing**
```yaml
Action: Systematisch testen

Testing Checklist (in BUGS.md dokumentieren):

Singleplayer:
  [ ] Player Movement (WASD, Sprint, Jump, Crouch)
  [ ] Camera Look (Maus)
  [ ] Clarity Tools (alle 4 funktionieren)
  [ ] Energy System (Recharge)
  [ ] Tool Switching (1-4)
  [ ] Manifestationen spawnen
  [ ] Manifestationen verfolgen Player
  [ ] Manifestationen greifen an
  [ ] Manifestationen sterben
  [ ] Wave-Progression
  [ ] Loot-Drops
  [ ] Loot-Pickup
  [ ] Mental Health nimmt Schaden
  [ ] Confidence-System
  [ ] Sprüche werden abgespielt
  [ ] HUD zeigt korrekte Werte
  [ ] Pause funktioniert
  [ ] Game Over Screen
  [ ] Restart funktioniert

Character Editor:
  [ ] Body Parts wechseln
  [ ] Farbe ändern
  [ ] Speichern funktioniert
  [ ] Laden funktioniert
  [ ] Auswahl wird im Spiel angewendet

Multiplayer:
  [ ] Host starten
  [ ] Client beitreten
  [ ] 2-4 Spieler gleichzeitig
  [ ] Player Movement Sync
  [ ] Gegner Sync
  [ ] Loot Sync
  [ ] Wellen Sync
  [ ] Disconnect handling

UI:
  [ ] Main Menu Navigation
  [ ] Alle Buttons funktionieren
  [ ] Settings speichern
  [ ] Alle Texte auf Deutsch
  [ ] Keine Placeholder-Texte

Audio:
  [ ] Clarity Tool Sounds
  [ ] Manifestation Sounds
  [ ] Player Sprüche
  [ ] Background Music
  [ ] UI Sounds

Gefundene Bugs priorisieren:
  - Critical: Crashes, Unspielbarkeit
  - High: Wichtige Features broken
  - Medium: Kleinere Bugs
  - Low: Polish-Issues
```

**TASK-11-02: Performance Profiling**
```yaml
Action: Window → Analysis → Profiler

Targets:
  - 60 FPS konstant (Singleplayer)
  - 45+ FPS (Multiplayer mit 4 Spielern)
  - Memory: < 2GB RAM
  - Draw Calls: < 500

Bottlenecks identifizieren:
  - CPU: Scripts-Optimierung
  - GPU: Shader/Material-Reduktion
  - Memory: Object Pooling validieren
  - GC Spikes: Allocations reduzieren

Optimierungen:
  - Object Pool für Manifestationen ✓
  - Object Pool für VFX ✓
  - LOD für Modelle (falls nötig)
  - Occlusion Culling (größere Levels)
  - Batching (Static für Environment)
```

**TASK-11-03: Code Cleanup**
```yaml
Action: Scripts durchgehen

Cleanup:
  - Alle Debug.Log() entfernen oder #if UNITY_EDITOR
  - Unused Variables löschen
  - Dead Code entfernen
  - Kommentare vervollständigen (Deutsch!)
  - Naming Conventions prüfen
  - TODO/FIXME-Kommentare abarbeiten

Code-Review:
  - Null-Checks bei GetComponent
  - Try-Catch bei kritischen Stellen
  - Keine hardcoded Werte (ScriptableObjects nutzen)
```

**TASK-11-04: Build Settings & Configuration**
```yaml
Action: File → Build Settings

Platform: PC, Mac & Linux Standalone
Architecture: x86_64

Scenes in Build:
  1. MainMenu
  2. CharacterEditor
  3. GameLevel_01

Player Settings:
  - Product Name: "OverthinkingSurvivors"
  - Company Name: [DEIN NAME]
  - Default Icon: [Falls vorhanden]
  - Splash Screen: Unity-Logo OK
  - Fullscreen Mode: Fullscreen Window
  - Default Resolution: 1920x1080
  - Resizable Window: ✓

Optimization:
  - API Compatibility: .NET Standard 2.1
  - Managed Stripping Level: Low
  - IL2CPP (optional, für Performance)

Quality Settings:
  - Default: URP-Medium
  - VSync: Every V Blank
  - Anti-Aliasing: 2x (URP)
```

**TASK-11-05: Final Build erstellen**
```yaml
Action: Build ausführen

Build Location: Builds/OverthinkingSurvivors_v0.1.0/

Build Steps:
  1. File → Build Settings → Build
  2. Ordner wählen: Builds/
  3. Build starten (Dauer: 5-15 Min)
  
Testing:
  - Build außerhalb Unity starten
  - Alle Features testen (Checklist)
  - Performance messen
  - Crashlogs prüfen (falls vorhanden)

Build Validation:
  - ✓ Spiel startet
  - ✓ Main Menu lädt
  - ✓ Gameplay funktioniert
  - ✓ Audio funktioniert
  - ✓ Input funktioniert (Keyboard + Maus)
  - ✓ Multiplayer funktioniert (lokales Netzwerk)
  - ✓ Keine Crashes
```

**TASK-11-06: Dokumentation finalisieren**
```yaml
Action: Alle Docs updaten

README.md:
  - Spielbeschreibung (Deutsch)
  - Installation
  - Steuerung
  - Features-Liste
  - Credits

CHANGELOG.md:
  - Version 0.1.0 Alpha
  - Alle Features auflisten
  - Known Issues

CREDITS.md:
  - Unity Technologies
  - Asset-Quellen (Kenney, Quaternius, etc.)
  - Audio-Quellen (Freesound, etc.)
  - Netcode for GameObjects

SPIELANLEITUNG.md (NEU):
  - Wie spielt man?
  - Clarity Tools Erklärung
  - Manifestationen-Typen
  - Multiplayer-Anleitung
  - Tipps & Tricks

In Git committen:
  git add .
  git commit -m "release: v0.1.0 Alpha - OverthinkingSurvivors"
  git tag v0.1.0
```

**Fertigstellungskriterien Agent-11:**
- ✅ Alle Critical/High Bugs gefixt
- ✅ Performance-Targets erreicht
- ✅ Code ist sauber
- ✅ Build funktioniert standalone
- ✅ Dokumentation vollständig
- ✅ Projekt ist release-ready!

---

## 📝 CODE-TEMPLATES (Deutsch kommentiert!)

### LocalizationManager.cs
```csharp
using System.Collections.Generic;
using UnityEngine;

namespace OverthinkingSurvivors.Managers
{
    /// <summary>
    /// Verwaltet deutsche Lokalisierung für alle UI-Texte
    /// </summary>
    public class LocalizationManager : MonoBehaviour
    {
        public static LocalizationManager Instance { get; private set; }
        
        private Dictionary<string, string> _localizedStrings = new Dictionary<string, string>();

        private void Awake()
        {
            if (Instance != null && Instance != this)
            {
                Destroy(gameObject);
                return;
            }
            Instance = this;
            DontDestroyOnLoad(gameObject);
            
            LoadLocalizedStrings();
        }

        /// <summary>
        /// Lädt deutsche Strings aus JSON-Datei
        /// </summary>
        private void LoadLocalizedStrings()
        {
            // Placeholder - später aus JSON laden
            _localizedStrings.Add("ui_main_menu_play", "Spielen");
            _localizedStrings.Add("ui_main_menu_character", "Charakter");
            _localizedStrings.Add("ui_main_menu_settings", "Einstellungen");
            _localizedStrings.Add("ui_main_menu_quit", "Beenden");
            _localizedStrings.Add("ui_game_health", "Mentale Gesundheit");
            _localizedStrings.Add("ui_game_confidence", "Selbstvertrauen");
        }

        /// <summary>
        /// Gibt lokalisierten String zurück
        /// </summary>
        public string GetString(string key)
        {
            if (_localizedStrings.TryGetValue(key, out string value))
                return value;
            
            Debug.LogWarning($"Lokalisierung fehlt für Key: {key}");
            return $"[{key}]";
        }
    }
}
```

### MentalHealth.cs
```csharp
using UnityEngine;
using UnityEngine.Events;

namespace OverthinkingSurvivors.Core
{
    /// <summary>
    /// Mentale Gesundheit + Selbstvertrauen System
    /// Ersetzt klassisches Health/Shield
    /// </summary>
    public class MentalHealth : MonoBehaviour
    {
        [Header("Mental Health")]
        [SerializeField] private float _maxMentalHealth = 100f;
        [SerializeField] private float _maxConfidence = 100f;
        
        [Header("Events")]
        public UnityEvent<float> OnMentalHealthChanged; // Parameter: Prozent (0-1)
        public UnityEvent<float> OnConfidenceChanged;
        public UnityEvent OnMentalBreakdown; // Statt OnDeath
        public UnityEvent OnConfidenceLost;

        private float _currentMentalHealth;
        private float _currentConfidence;
        
        public float CurrentMentalHealth => _currentMentalHealth;
        public float MaxMentalHealth => _maxMentalHealth;
        public float CurrentConfidence => _currentConfidence;
        public float MaxConfidence => _maxConfidence;
        public bool IsStable => _currentMentalHealth > 0; // Statt IsAlive

        private void Awake()
        {
            _currentMentalHealth = _maxMentalHealth;
            _currentConfidence = _maxConfidence;
        }

        /// <summary>
        /// Nimmt mentalen Schaden - reduziert erst Confidence, dann Mental Health
        /// </summary>
        public void TakeMentalDamage(float damage)
        {
            if (!IsStable) return;

            // Erst Confidence reduzieren (Shield)
            if (_currentConfidence > 0)
            {
                _currentConfidence -= damage;
                if (_currentConfidence < 0)
                {
                    // Überschuss geht auf Mental Health
                    float overflow = Mathf.Abs(_currentConfidence);
                    _currentConfidence = 0;
                    OnConfidenceLost?.Invoke();
                    
                    _currentMentalHealth -= overflow;
                }
                
                OnConfidenceChanged?.Invoke(_currentConfidence / _maxConfidence);
            }
            else
            {
                // Kein Confidence mehr, direkt Mental Health
                _currentMentalHealth -= damage;
            }

            _currentMentalHealth = Mathf.Max(_currentMentalHealth, 0f);
            OnMentalHealthChanged?.Invoke(_currentMentalHealth / _maxMentalHealth);

            if (_currentMentalHealth <= 0)
            {
                MentalBreakdown();
            }
        }

        /// <summary>
        /// Heilt mentale Gesundheit
        /// </summary>
        public void Heal(float amount)
        {
            if (!IsStable) return;

            _currentMentalHealth += amount;
            _currentMentalHealth = Mathf.Min(_currentMentalHealth, _maxMentalHealth);
            
            OnMentalHealthChanged?.Invoke(_currentMentalHealth / _maxMentalHealth);
        }

        /// <summary>
        /// Stellt Selbstvertrauen wieder her
        /// </summary>
        public void RestoreConfidence(float amount)
        {
            if (!IsStable) return;

            _currentConfidence += amount;
            _currentConfidence = Mathf.Min(_currentConfidence, _maxConfidence);
            
            OnConfidenceChanged?.Invoke(_currentConfidence / _maxConfidence);
        }

        /// <summary>
        /// Setzt alles auf Maximum zurück
        /// </summary>
        public void FullRestore()
        {
            _currentMentalHealth = _maxMentalHealth;
            _currentConfidence = _maxConfidence;
            
            OnMentalHealthChanged?.Invoke(1f);
            OnConfidenceChanged?.Invoke(1f);
        }

        private void MentalBreakdown()
        {
            OnMentalBreakdown?.Invoke();
            Debug.Log("MENTALER ZUSAMMENBRUCH!");
        }
    }
}
```

### CharacterSprueche.cs
```csharp
using System.Collections.Generic;
using UnityEngine;

namespace OverthinkingSurvivors.Gameplay
{
    /// <summary>
    /// System für lustige Charakter-Sprüche mit Thematik
    /// </summary>
    public class CharacterSprueche : MonoBehaviour
    {
        public enum SpruchType
        {
            OnDamage,
            OnKill,
            OnLowHealth,
            OnPickup,
            OnWaveStart
        }

        [Header("Audio")]
        [SerializeField] private AudioSource _audioSource;
        [SerializeField] private float _spruchCooldown = 5f;
        
        private Dictionary<SpruchType, List<string>> _sprueche;
        private float _lastSpruchTime;

        private void Awake()
        {
            InitializeSprueche();
        }

        private void InitializeSprueche()
        {
            _sprueche = new Dictionary<SpruchType, List<string>>()
            {
                {
                    SpruchType.OnDamage, new List<string>
                    {
                        "Autsch! Das tut mental weh...",
                        "Typisch ich, wieder zu empfindlich!",
                        "Das wird schon... oder?",
                        "Nicht schon wieder!",
                        "Das hat wehgetan!"
                    }
                },
                {
                    SpruchType.OnKill, new List<string>
                    {
                        "Einen Gedanken weniger!",
                        "Das schaffst du nie? DOCH!",
                        "Klarheit siegt!",
                        "Und weg damit!",
                        "So viel zu deiner Meinung!"
                    }
                },
                {
                    SpruchType.OnLowHealth, new List<string>
                    {
                        "Ich brauch 'ne Pause vom Denken...",
                        "Das wird zu viel!",
                        "Atmen... einfach atmen...",
                        "Ich kann nicht mehr!",
                        "Hilfe... zu viele Gedanken!"
                    }
                },
                {
                    SpruchType.OnPickup, new List<string>
                    {
                        "Das hilft!",
                        "Genau was ich brauchte!",
                        "Motivation +100!",
                        "Danke, Universum!",
                        "Endlich was Positives!"
                    }
                },
                {
                    SpruchType.OnWaveStart, new List<string>
                    {
                        "Hier kommen sie wieder...",
                        "Ich schaff das!",
                        "Overthinking-Alarm!",
                        "Nicht schon wieder denken!",
                        "Los geht's... glaub ich..."
                    }
                }
            };
        }

        /// <summary>
        /// Spielt zufälligen Spruch des angegebenen Typs ab
        /// </summary>
        public void PlayRandomSpruch(SpruchType type)
        {
            // Cooldown check
            if (Time.time - _lastSpruchTime < _spruchCooldown)
                return;

            if (_sprueche.TryGetValue(type, out List<string> spruchList))
            {
                string spruch = spruchList[Random.Range(0, spruchList.Count)];
                Debug.Log($"[SPRUCH] {spruch}");
                
                // TODO: Text-to-Speech oder Audio-Clip abspielen
                // Für jetzt: Nur Debug-Log
                
                _lastSpruchTime = Time.time;
            }
        }

        /// <summary>
        /// Spielt spezifischen Spruch ab (für Cutscenes/Events)
        /// </summary>
        public void PlaySpruch(string spruch)
        {
            Debug.Log($"[SPRUCH] {spruch}");
            // TODO: Audio
        }
    }
}
```

---

## 📦 GIT CONFIGURATION

### .gitignore
```gitignore
# Unity-generierte Dateien
/[Ll]ibrary/
/[Tt]emp/
/[Oo]bj/
/[Bb]uild/
/[Bb]uilds/
/[Ll]ogs/
/[Uu]ser[Ss]ettings/
/[Mm]emoryCaptures/

# Visual Studio / Rider
.vs/
.idea/
*.csproj
*.unityproj
*.sln
*.suo
*.tmp
*.user
*.userprefs
*.pidb
*.booproj
*.svd
*.pdb
*.mdb
*.opendb
*.VC.db

# Unity3D Generated
sysinfo.txt
*.stackdump

# Builds
*.apk
*.aab
*.unitypackage
*.app

# macOS
.DS_Store
```

### .gitattributes
```gitattributes
# 3D Models
*.fbx filter=lfs diff=lfs merge=lfs -text
*.obj filter=lfs diff=lfs merge=lfs -text
*.blend filter=lfs diff=lfs merge=lfs -text

# Textures
*.png filter=lfs diff=lfs merge=lfs -text
*.jpg filter=lfs diff=lfs merge=lfs -text
*.jpeg filter=lfs diff=lfs merge=lfs -text
*.tga filter=lfs diff=lfs merge=lfs -text
*.psd filter=lfs diff=lfs merge=lfs -text

# Audio
*.wav filter=lfs diff=lfs merge=lfs -text
*.mp3 filter=lfs diff=lfs merge=lfs -text
*.ogg filter=lfs diff=lfs merge=lfs -text

# Video
*.mp4 filter=lfs diff=lfs merge=lfs -text
*.mov filter=lfs diff=lfs merge=lfs -text
```

---

## 📖 README.md TEMPLATE

```markdown
# 🧠 OverthinkingSurvivors

Überlebe die Manifestationen deiner eigenen Overthinking-Gedanken in diesem lustigen Co-op Survival-Spiel!

## 🎮 Spielbeschreibung
Deine Sorgen, Zweifel, Ängste und negative Gedanken haben sich verselbstständigt und greifen dich an! Nutze Klarheits-Werkzeuge wie Meditation, Sport, Musik und Journaling, um deine mentale Gesundheit zu verteidigen. Spiele alleine oder mit bis zu 3 Freunden im Co-op-Modus!

## 🕹️ Steuerung
**Bewegung:**
- `WASD` - Laufen
- `Shift` - Sprint
- `Leertaste` - Springen
- `Strg` - Ducken
- `Maus` - Umsehen

**Kampf:**
- `Linke Maustaste` - Klarheits-Tool nutzen
- `R` - Energie aufladen
- `1-4` - Klarheits-Tool wechseln

**Sonstiges:**
- `ESC` - Pause

## 🧰 Klarheits-Tools
- 🧘 **Meditation** - Nahkampf, beruhigt Gedanken, unbegrenzt nutzbar
- 🎵 **Musik** - Fernkampf, lenkt ab, mittlere Energie
- 🏃 **Sport** - Nahkampf, sehr stark, verbraucht viel Energie
- 📝 **Tagebuch** - Fernkampf, präzise, sortiert Gedanken

## 👹 Overthinking-Manifestationen
- 💭 **Die Sorge** - Langsam, viel Ausdauer, sagt: "Was wenn...?"
- 😰 **Der Zweifel** - Normal, hartnäckig, sagt: "Das schaffst du nie!"
- 🌪️ **Die Panik** - Schnell, chaotisch, sagt: "ALLES IST SCHRECKLICH!"
- 😴 **Die Prokrastination** - Sehr langsam, blockiert, sagt: "Mach ich später..."

## 🌐 Multiplayer
- **Host starten:** Hauptmenü → Mehrspieler → Host starten
- **Beitreten:** Hauptmenü → Mehrspieler → Spiel beitreten → IP eingeben
- **Spieler:** 1-4 Spieler Co-op
- **Modus:** Gemeinsam gegen Wellen überleben

## 🛠️ Technische Details
- **Engine:** Unity 6.3 LTS
- **Render Pipeline:** URP
- **Plattform:** PC (Windows, Linux)
- **Netzwerk:** Netcode for GameObjects
- **Sprache:** Deutsch

## 📦 Features
- ✅ First-Person Movement mit Sprint, Jump, Crouch
- ✅ 4 verschiedene Klarheits-Tools
- ✅ 4 Overthinking-Manifestations-Typen
- ✅ Character Editor mit Anpassungen
- ✅ Wave-basiertes Survival-System
- ✅ Loot-System (Motivation, Klarheit, Energie)
- ✅ Lustige Charakter-Sprüche
- ✅ Deutsches UI
- ✅ Co-op Multiplayer (bis 4 Spieler)

## 🚀 Installation
1. Download von [RELEASE-LINK]
2. Entpacken
3. `OverthinkingSurvivors.exe` starten
4. Viel Spaß!

## 📝 Credits
- **Entwicklung:** [DEIN NAME]
- **Assets:** Kenney.nl, Quaternius, Unity Asset Store
- **Audio:** Freesound.org, Kenney.nl
- **Engine:** Unity Technologies
- **Multiplayer:** Netcode for GameObjects

## 📄 Lizenz
[DEINE LIZENZ]

---

**Version:** 0.1.0 Alpha  
**Entwicklungszeit:** [DATUM]  
**Kontakt:** [DEIN KONTAKT]
```

---

## 🎯 WICHTIGE ERINNERUNGEN FÜR CLAUDE

### Autonome Arbeitsweise:
1. **ALLE Tasks eines Agenten in EINER Session abarbeiten**
2. **NICHT für jeden Task fragen**
3. Status nach jedem Task updaten
4. Erst wenn Agent 100% fertig ist, nächsten Agenten vorschlagen

### Deutsche Lokalisierung:
- Alle UI-Texte auf Deutsch
- Code-Kommentare auf Deutsch
- Variablennamen können Englisch bleiben (Best Practice)
- Debug.Log auch auf Deutsch

### Overthinking-Thematik konsequent:
- Keine "Zombies" → "Overthinking-Manifestationen"
- Keine "Waffen" → "Klarheits-Tools"
- Keine "Health" → "Mentale Gesundheit"
- Keine "Shield" → "Selbstvertrauen"
- Lustige, selbstironische Sprüche

### Multiplayer-Besonderheiten:
- Netcode for GameObjects nutzen
- ServerRpc/ClientRpc für Synchronisation
- Nur Server spawnt Gegner
- NetworkTransform für Bewegung
- NetworkVariable für wichtige Werte

---

## 📊 PROGRESS TRACKING

```yaml
Agent-01 (Project Setup): ⬜⬜⬜⬜⬜⬜⬜⬜⬜⬜ 0/10 Tasks
Agent-02 (Core Systems): ⬜⬜⬜⬜⬜⬜⬜ 0/7 Tasks
Agent-03 (Player Mechanics): ⬜⬜⬜⬜⬜⬜ 0/6 Tasks
Agent-04 (Character Editor): ⬜⬜⬜⬜⬜⬜⬜⬜ 0/8 Tasks
Agent-05 (Clarity Tools): ⬜⬜⬜⬜⬜⬜⬜⬜ 0/8 Tasks
Agent-06 (Manifestationen): ⬜⬜⬜⬜⬜⬜⬜ 0/7 Tasks
Agent-07 (UI & HUD): ⬜⬜⬜⬜⬜⬜ 0/6 Tasks
Agent-08 (Audio & Sprüche): ⬜⬜⬜⬜⬜⬜ 0/6 Tasks
Agent-09 (Integration): ⬜⬜⬜⬜⬜⬜⬜ 0/7 Tasks
Agent-10 (Multiplayer): ⬜⬜⬜⬜⬜⬜⬜⬜⬜ 0/9 Tasks
Agent-11 (Testing): ⬜⬜⬜⬜⬜⬜ 0/6 Tasks

GESAMT: 0/75 Tasks (0%)
```

---

**PROJEKT START READY! 🚀**

**Nächster Schritt:**
1. Diese MasterPlan.md ins Unity-Projektverzeichnis kopieren
2. Claude aktivieren mit: "Mach dich mit dem Projekt vertraut und starte Agent-01"
3. Claude arbeitet ALLE 10 Tasks von Agent-01 ab
4. Danach Agent-02 starten, usw.

**Viel Erfolg mit OverthinkingSurvivors! 🧠💪**