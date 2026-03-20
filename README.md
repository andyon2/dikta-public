<p align="center">
  <b>Dikta</b>
</p>

# Dikta

<p align="center">
  <a href="https://github.com/andyon2/dikta-public/releases/latest"><img src="https://img.shields.io/badge/Version-0.4.6-emerald?style=for-the-badge" alt="Version 0.4.6"></a>
  <img src="https://img.shields.io/badge/Windows-blue?style=for-the-badge&logo=windows" alt="Windows">
  <img src="https://img.shields.io/badge/Android-green?style=for-the-badge&logo=android" alt="Android">
</p>

**Freie Alternative zu Wispr Flow — Sprachdiktat mit KI-Text-Cleanup.** Dikta wandelt Sprache in jedem Textfeld systemweit in bereinigten Text um. Kein Abo, keine Cloud-Abhängigkeit — du entscheidest ob Cloud oder komplett offline.

## Inhaltsverzeichnis

- [Quick Start](#quick-start)
- [Was Dikta kann](#was-dikta-kann)
- [Windows](#windows)
- [Android](#android)
- [Provider-Übersicht](#provider-übersicht)
- [Tech-Stack](#tech-stack)
- [Feedback](#feedback)

---

## Quick Start

### 1. Wähle deinen Modus

Dikta funktioniert in zwei Modi — du entscheidest beim ersten Start:

**☁️ Cloud (empfohlen)** — Beste Qualität, schnellste Ergebnisse.

Du brauchst mindestens einen **Groq API-Key** — damit funktioniert sowohl Spracherkennung als auch Text-Bereinigung. Groq ist kostenlos nutzbar; bei intensiver Nutzung kann ein kurzes Limit greifen.

Für bessere Cleanup-Qualität empfehlen wir zusätzlich einen **DeepSeek API-Key** (~0,001 € pro Diktat). Weitere Provider (OpenAI, OpenRouter) lassen sich in den Settings konfigurieren.

| Was du brauchst | Key holen |
|----------------|-----------|
| **Groq** (Pflicht) — Spracherkennung + Cleanup, kostenloses Free-Tier mit Limit | [console.groq.com](https://console.groq.com) |
| **DeepSeek** (empfohlen) — Besseres Cleanup, ~0,001 € pro Diktat | [platform.deepseek.com](https://platform.deepseek.com) |

Deine Sprache geht direkt an die Provider — kein Dikta-Server dazwischen. Bei normalem Gebrauch (30-60 Diktate/Tag) unter 0,10 € am Tag.

**🔒 Offline (nur Windows)** — Kein Account, kein API-Key, keine Daten verlassen deinen Rechner.

Spracherkennung läuft lokal über whisper.cpp (~500 MB Modell-Download beim ersten Start). Text-Cleanup wird übersprungen — du bekommst den Rohtext direkt. Ideal zum Ausprobieren ohne Registrierung oder für datenschutz-sensible Umgebungen.

### 2. Installieren

➡️ **[Aktuellen Release herunterladen](https://github.com/andyon2/dikta-public/releases/latest)**

| Plattform | Datei | Installation |
|-----------|-------|-------------|
| **Windows** | `Dikta_x64-setup.exe` | Herunterladen, ausführen |
| **Android** | `Dikta-v0.4.6.apk` | Herunterladen, "Aus unbekannten Quellen" erlauben, installieren |

### 3. Einrichten und loslegen

Beim ersten Start führt dich ein **Einrichtungs-Wizard** durch alles: Cloud oder Offline wählen, API-Keys eingeben (mit Validierung), Test-Diktat ausprobieren. Danach: Hotkey drücken und diktieren.

---

## Was Dikta kann

<table>
<tr><td><b>End-to-End Pipeline</b></td><td>Aufnehmen → Transkribieren → Bereinigen → Einfügen ins aktive Fenster. Ein Hotkey, ein Ergebnis.</td></tr>
<tr><td><b>3 Schreibstile</b></td><td><b>Polished</b> (Füllwörter weg, Grammatik, Profi-Text), <b>Verbatim</b> (nur Satzzeichen), <b>Chat</b> (locker, Emojis erlaubt).</td></tr>
<tr><td><b>Live-Übersetzung</b></td><td>Deutsch sprechen, Englisch einfügen — oder umgekehrt. 13 Output-Sprachen konfigurierbar.</td></tr>
<tr><td><b>Custom Dictionary</b></td><td>Fachbegriffe die STT und LLM beibehalten sollen (Produktnamen, Abkürzungen, Eigennamen).</td></tr>
<tr><td><b>App Profiles</b></td><td>Stil, Sprache und Prompt pro App automatisch anpassen. Slack = Chat-Stil, Word = Polished.</td></tr>
<tr><td><b>Command Mode</b></td><td>Text selektieren, Sprachbefehl geben ("Mach das kürzer", "Übersetze auf Englisch"). Strg+Shift+E.</td></tr>
<tr><td><b>History</b></td><td>Alle Diktate durchsuchbar, nachträglich bearbeitbar.</td></tr>
<tr><td><b>Kosten-Dashboard</b></td><td>Zeigt STT- und LLM-Kosten pro Session. Vergleich: "Du sparst X € vs. Wispr Flow".</td></tr>
</table>

---

## Windows

<table>
<tr><td><b>Globaler Hotkey</b></td><td>2 konfigurierbare Hotkey-Slots mit je eigenem Modus: Hold (halten), Toggle (drücken/drücken), Auto-Stop und Auto (experimental).</td></tr>
<tr><td><b>Floating Bar</b></td><td>Schwebende Leiste am Bildschirmrand — zeigt Echtzeit-Waveform während der Aufnahme, Verarbeitungsstatus und Ergebnis.</td></tr>
<tr><td><b>System Tray</b></td><td>Schnellzugriff über das Tray-Icon. Dikta läuft im Hintergrund.</td></tr>
<tr><td><b>Paste überall</b></td><td>Ergebnis wird automatisch per Ctrl+V ins aktive Fenster eingefügt — Browser, Editor, Chat, Terminal.</td></tr>
<tr><td><b>Whisper Mode</b></td><td>Audio-Verstärkung für leises Diktieren (z.B. im Büro).</td></tr>
<tr><td><b>Offline-Modus</b></td><td>Spracherkennung lokal über whisper.cpp — kein Internet nötig, keine Daten verlassen den Rechner.</td></tr>
</table>

## Android

<table>
<tr><td><b>Floating Bubble</b></td><td>Erscheint automatisch wenn eine Texteingabe aktiv ist — nicht dauerhaft sichtbar. Tap = Aufnahme starten/stoppen, Long-Press = Push-to-Talk.</td></tr>
<tr><td><b>Unter 1 Sekunde</b></td><td>Gesamter Prozess (Aufnahme → Transkription → Cleanup → Einfügen) in unter einer Sekunde.</td></tr>
<tr><td><b>Paste überall</b></td><td>Einfügen über AccessibilityService in jedes Textfeld — WhatsApp, Mail, Browser, Notizen.</td></tr>
<tr><td><b>Per-Geste konfigurierbar</b></td><td>Tap und Long-Press haben jeweils eigenen Modus und eigene Einstellungen.</td></tr>
</table>

---

## Provider-Übersicht

Dikta unterstützt mehrere Provider für Spracherkennung (STT) und Text-Bereinigung (LLM). Du wählst in den Settings, welche du nutzen möchtest.

### Spracherkennung (STT)

| Provider | Plattform | Kosten | Besonderheit |
|----------|-----------|--------|-------------|
| **Groq Whisper** | Windows, Android | Kostenloses Free-Tier (mit Limit) | Schnell, empfohlen |
| **OpenAI Whisper** | nur Windows | ~0,006 €/min | Alternative bei Groq-Limit |
| **whisper.cpp (lokal)** | nur Windows | Kostenlos | Offline, ~500 MB Modell |

### Text-Bereinigung (LLM)

| Provider | Plattform | Kosten | Besonderheit |
|----------|-----------|--------|-------------|
| **DeepSeek** | Windows, Android | ~0,001 €/Diktat | Beste Qualität/Preis, empfohlen |
| **Groq (Llama)** | Windows, Android | Kostenloses Free-Tier (mit Limit) | Reicht als einziger Key |
| **OpenAI** | Windows, Android | ~0,01 €/Diktat | Premium-Alternative |
| **OpenRouter** | Windows, Android | variabel | Zugang zu vielen Modellen (experimentell) |

Wenn der gewählte Provider keinen Key hat, schaltet Dikta automatisch auf den nächsten verfügbaren um.

---

<details>
<summary><b>Tech-Stack</b></summary>

<br>

| Schicht | Technologie | Warum |
|---------|-------------|-------|
| Desktop-Framework | Tauri v2 | Ein Codebase für Windows + Android, Rust-Backend, kleine Binaries |
| Frontend | React + TypeScript + Tailwind CSS | Typsicherheit, schnelles Styling |
| Backend | Rust | Niedrige Latenz, native OS-APIs, whisper.cpp-Integration |
| Mobile | Tauri v2 Android + Kotlin | Floating Bubble, native Audio, AccessibilityService |
| STT | Groq Whisper API, whisper.cpp (offline) | Schnell, kostenlos / offline-fähig |
| Text-Cleanup | DeepSeek, Groq, OpenAI, OpenRouter | Multi-Provider, Auto-Fallback |
| Speicherung | JSON (Config), SQLite (History, Stats) | Einfach, kein Server nötig |

</details>

---

## Lizenz

Noch nicht festgelegt. Der Quellcode ist öffentlich einsehbar.

## Feedback

Bugs und Wünsche gerne als [GitHub Issue](https://github.com/andyon2/dikta-public/issues) melden.
