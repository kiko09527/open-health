# 🚀 **OpenHealth**

**KI-Gesundheitsassistent | Betrieben mit Ihren Daten, Lokal ausgeführt**

---

<div align="center">

### 🌍 Wählen Sie Ihre Sprache
[English](../../README.md) | [Français](README.fr.md) | [Deutsch](README.de.md) | [Español](README.es.md) | [한국어](README.ko.md) | [中文](README.zh.md) | [日本語](README.ja.md)

</div>

---

<p align="center">
  <img src="/intro/openhealth.avif" alt="OpenHealth Demo">
</p>

## 🌟 Überblick

> OpenHealth hilft Ihnen, **die Kontrolle über Ihre Gesundheitsdaten zu übernehmen**. Durch den Einsatz von KI und Ihren persönlichen Gesundheitsinformationen
> bietet OpenHealth einen privaten und lokal ausgeführten Assistenten, der Ihnen hilft, Ihre Gesundheit besser zu verstehen und zu verwalten.

## ✨ Projektfunktionen

<details open>
<summary><b>Hauptfunktionen</b></summary>

- 📊 **Zentralisierte Gesundheitsdateneingabe:** Konsolidieren Sie alle Ihre Gesundheitsdaten einfach an einem Ort.
- 🛠️ **Intelligentes Parsing:** Analysiert automatisch Ihre Gesundheitsdaten und generiert strukturierte Datendateien.
- 🤝 **Kontextbezogene Gespräche:** Nutzen Sie die strukturierten Daten als Kontext für personalisierte Interaktionen mit GPT-gestützter KI.

</details>

## 📥 Unterstützte Datenquellen & Sprachmodelle

<table>
  <tr>
    <th>Verfügbare Datenquellen</th>
    <th>Unterstützte Sprachmodelle</th>
  </tr>
  <tr>
    <td>
      • Bluttestergebnisse<br>
      • Gesundheitscheck-Daten<br>
      • Persönliche Körperinformationen<br>
      • Familiengeschichte<br>
      • Symptome
    </td>
    <td>
      • LLaMA<br>
      • DeepSeek-V3<br>
      • GPT<br>
      • Claude<br>
      • Gemini
    </td>
  </tr>
</table>

## 🤔 Warum Wir OpenHealth Entwickelt Haben

> - 💡 **Ihre Gesundheit liegt in Ihrer Verantwortung.**
> - ✅ Echtes Gesundheitsmanagement kombiniert **Ihre Daten** + **Intelligenz** und verwandelt Erkenntnisse in umsetzbare Pläne.
> - 🧠 KI fungiert als unvoreingenommenes Werkzeug, um Sie bei der effektiven Verwaltung Ihrer langfristigen Gesundheit zu unterstützen.

## 🗺️ Projektdiagramm

```mermaid
graph LR
    A[Datenerfassung] --> B[Datenverarbeitung]
    B --> C[Strukturierte Daten]
    C --> D[Kontextanalyse]
    D --> E[KI-Interaktion]
    E --> F[Personalisierte Erkenntnisse]
    
    style A fill:#ff7eb6,stroke:#ff2d7e,stroke-width:2px
    style B fill:#7afcff,stroke:#00b4ff,stroke-width:2px
    style C fill:#98fb98,stroke:#32cd32,stroke-width:2px
    style D fill:#ffa07a,stroke:#ff4500,stroke-width:2px
    style E fill:#dda0dd,stroke:#9370db,stroke-width:2px
    style F fill:#f0e68c,stroke:#daa520,stroke-width:2px
```

Gesundheitsdaten-Eingabe --> Parsing-Modul --> Strukturierte Datendateien --> GPT-Integration

> **Hinweis:** Die Datenanalyse-Funktionalität ist derzeit in einem separaten Python-Server implementiert und soll in Zukunft zu TypeScript migriert werden.

## ⚙️ OpenHealth ausführen

1. **Repository klonen:**
   ```bash
   git clone https://github.com/OpenHealthForAll/open-health.git
   cd open-health
   ```

2. **Einrichtung und Ausführung:**
   ```bash
   # Umgebungsdatei kopieren
   cp .env.example .env

   # API-Schlüssel zur .env-Datei hinzufügen:
   # UPSTAGE_API_KEY - Für das Parsing (Erhalten Sie $10 Guthaben ohne Kartenregistrierung bei https://www.upstage.ai)
   # OPENAI_API_KEY - Für erweiterte Parsing-Funktionen

   # Anwendung mit Docker Compose starten
   docker compose --env-file .env up
   ```

   Für bestehende Benutzer:
   ```bash
   docker compose --env-file .env up --build
   ```

3. **Zugriff auf OpenHealth:**
   Öffnen Sie Ihren Browser und navigieren Sie zu `http://localhost:3000`, um OpenHealth zu nutzen.

> **Hinweis:** Das System besteht aus zwei Hauptkomponenten: Parsing und LLM. Derzeit verwendet das Parsing Upstage- und OpenAI-APIs (die in unseren Tests die beste Leistung zeigten), wobei ein lokaler Parser in Kürze hinzugefügt wird. Die LLM-Komponente kann mit Ollama vollständig lokal ausgeführt werden.

> **Hinweis:** Wenn Sie Ollama mit Docker verwenden, stellen Sie sicher, dass der Ollama-API-Endpunkt auf `http://docker.for.mac.localhost:11434/` eingestellt ist.

---
