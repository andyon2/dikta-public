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

### Einmal zahlen, für immer nutzen

Kein Abo, keine monatlichen Kosten für die App selbst. Du zahlst nur die API-Nutzung deiner eigenen Keys — bei normalem Gebrauch unter 3 € im Monat. Das Kosten-Dashboard zeigt dir live, was du gegenüber Wispr Flow ($12/Monat) sparst.

### Kernfunktionen

<table>
<tr><td><b>End-to-End Pipeline</b></td><td>Aufnehmen → Transkribieren → Bereinigen → Einfügen ins aktive Fenster. Ein Hotkey, ein Ergebnis.</td></tr>
<tr><td><b>3 Schreibstile</b></td><td><b>Polished</b> (Füllwörter weg, Grammatik, Profi-Text), <b>Verbatim</b> (nur Satzzeichen), <b>Chat</b> (locker, Emojis erlaubt).</td></tr>
<tr><td><b>Post-Diktat Reformate</b></td><td>Nach jedem Diktat: One-Click-Buttons für <b>Email</b>, <b>Aufzählung</b> oder <b>Zusammenfassung</b> — Text sofort umstrukturieren.</td></tr>
<tr><td><b>Live-Übersetzung</b></td><td>Deutsch sprechen, Englisch einfügen — oder umgekehrt. 13 Output-Sprachen konfigurierbar.</td></tr>
<tr><td><b>Command Mode</b></td><td>Text selektieren, Sprachbefehl geben ("Mach das kürzer", "Übersetze auf Englisch"). Strg+Shift+E.</td></tr>
<tr><td><b>BYOK — Bring Your Own Key</b></td><td>Deine eigenen API-Keys für Groq, DeepSeek, OpenAI oder OpenRouter. Kein Proxy, kein Vendor Lock-in. Du wählst Provider und Modell.</td></tr>
<tr><td><b>Offline-Modus</b></td><td>Spracherkennung lokal über whisper.cpp mit GPU-Beschleunigung — keine Daten verlassen deinen Rechner. Ideal für sensible Umgebungen.</td></tr>
</table>

### Produktivitäts-Features

<table>
<tr><td><b>Dual Hotkeys</b></td><td>2 unabhängige Hotkey-Slots mit je eigenem Modus. Slot 1 = Hold für kurze Chat-Nachrichten, Slot 2 = Toggle für lange Dokumente — kein Umkonfigurieren nötig.</td></tr>
<tr><td><b>Insert-and-Send</b></td><td>Drückt automatisch Enter nach dem Einfügen — diktierter Text wird direkt abgeschickt (z.B. in Slack, WhatsApp Web, Teams).</td></tr>
<tr><td><b>App Profiles</b></td><td>Stil, Sprache und Prompt pro App automatisch anpassen. Slack = Chat-Stil, Word = Polished.</td></tr>
<tr><td><b>Custom Dictionary</b></td><td>Fachbegriffe die Dikta beibehalten soll (Produktnamen, Abkürzungen, Eigennamen).</td></tr>
<tr><td><b>Voice Notes</b></td><td>Diktate als Notizen speichern statt einzufügen — für Ideen, Memos, Gedankenprotokolle.</td></tr>
<tr><td><b>Text Snippets</b></td><td>Häufig genutzte Textbausteine per Klick einfügen.</td></tr>
</table>

### Tracking & Integrationen

<table>
<tr><td><b>Kosten-Dashboard</b></td><td>Trackt STT- und LLM-Kosten pro Diktat. Zeigt live: "Du sparst X € vs. Wispr Flow diesen Monat".</td></tr>
<tr><td><b>Füllwort-Analyse</b></td><td>Zeigt deine häufigsten Füllwörter — nützlich für Presenter, Coaches, alle die besser formulieren wollen.</td></tr>
<tr><td><b>History</b></td><td>Alle Diktate gespeichert und durchsuchbar. Roher Transkript-Text jederzeit einsehbar.</td></tr>
<tr><td><b>Cross-Device Sync</b></td><td>Diktat-History zwischen Windows und Android synchronisieren (über Turso Cloud-DB).</td></tr>
<tr><td><b>Webhook</b></td><td>Jedes Diktat-Ergebnis automatisch an eine URL senden — für Zapier, n8n oder eigene Automationen.</td></tr>
</table>

---

## Windows

<table>
<tr><td><b>Dual Hotkeys</b></td><td>2 konfigurierbare Hotkey-Slots mit je eigenem Modus: Hold (halten), Toggle (drücken/drücken), AutoStop (Stille erkennen), Auto-Loop (Endlos-Diktat).</td></tr>
<tr><td><b>Floating Bar</b></td><td>Schwebende Pill-Leiste — zeigt Echtzeit-Waveform während der Aufnahme, Verarbeitungsstatus, aktiven Modus. Frei positionierbar.</td></tr>
<tr><td><b>Paste überall</b></td><td>Ergebnis wird automatisch ins aktive Fenster eingefügt — Browser, Editor, Chat, Terminal. Clipboard-Fallback wenn Paste fehlschlägt.</td></tr>
<tr><td><b>Insert-and-Send</b></td><td>Optional: Enter nach Paste — diktierte Nachricht wird direkt abgeschickt. Pro Hotkey-Slot konfigurierbar.</td></tr>
<tr><td><b>Command Mode</b></td><td>Text selektieren, Sprachbefehl geben, LLM schreibt die Selektion um. Eigener Hotkey (Strg+Shift+E).</td></tr>
<tr><td><b>Whisper Mode</b></td><td>Audio-Verstärkung für leises Diktieren im Büro. Konfigurierbare Gain-Stufe.</td></tr>
<tr><td><b>Offline-Modus</b></td><td>Whisper.cpp lokal mit GPU/CUDA. Modell-Manager zum Download (small/medium/large-v3). Kein Internet nötig.</td></tr>
<tr><td><b>System Tray</b></td><td>Schnellzugriff über das Tray-Icon. Dikta läuft im Hintergrund, Autostart konfigurierbar.</td></tr>
</table>

## Android

<table>
<tr><td><b>Floating Bubble</b></td><td>Erscheint automatisch wenn eine Texteingabe aktiv ist. 5 animierte Zustände: Idle, Recording (Waveform), Push-to-Talk (roter Kreis), Processing (Spinner), fertig.</td></tr>
<tr><td><b>Unter 1 Sekunde</b></td><td>Gesamter Prozess (Aufnahme → Transkription → Cleanup → Einfügen) in unter einer Sekunde.</td></tr>
<tr><td><b>Per-Geste konfigurierbar</b></td><td>Tap und Long-Press haben jeweils eigenen Modus (Hold, Toggle, AutoStop, Auto-Loop) und eigene Silence-Dauer.</td></tr>
<tr><td><b>Paste überall</b></td><td>Einfügen über AccessibilityService in jedes Textfeld — WhatsApp, Mail, Browser, Notizen.</td></tr>
<tr><td><b>Bubble anpassbar</b></td><td>Größe, Transparenz und Position frei konfigurierbar. Position wird gespeichert.</td></tr>
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
