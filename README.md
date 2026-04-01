# Konverter von Word/ODT in eine HTML-Website (MkDocs)

🔗 **[Zur generierten Demo-Website](https://stahe.github.io/de-word-odt-vers-html-janv-2026/)**

---

## 📝 Beschreibung

In diesem Projekt möchten wir dem Leser einen Python-Konverter zur Verfügung stellen, der Word- oder ODT-Dokumente in eine statische HTML-Website umwandelt.

Wenn das ODT- oder DOCX-Dokument geeignet ist, erzeugt der Konverter über **MkDocs** eine HTML-Website von sehr guter Qualität.

## 🤖 Entstehungshintergrund

Dieser Konverter wurde ursprünglich von der KI **Gemini 3** erstellt. Er ist das Ergebnis aufeinanderfolgender Iterationen zur Feinabstimmung der Struktur von ODT-Dokumenten (OpenDocument Text).
Anschließend wurde er durch die KI **ChatGPT 5.2** verbessert, die den Konverter für Word-Dokumente erstellt hat.

## ✨ Funktionen

Das Skript `convert.py` führt folgende Aktionen aus:

* **Konvertierung von ODT/DOCX nach Markdown**: Analysiert die Quelldatei, um deren Struktur zu extrahieren.
* **Verwaltung von Überschriften**: Erzeugt automatisch das Inhaltsverzeichnis (TOC) und die seitliche Navigation.
* **Code-Blöcke**: Automatische Spracherkennung, Syntaxhervorhebung und **präzise Verwaltung der Zeilennummerierung** (Attribute `start-value`).
* **Listen**: Unterstützung für verschachtelte und gemischte Aufzählungs- und Nummerierungslisten mit korrekter Einrückung.
* **Formatierung**: Unterstützung von *Fettdruck*, *Kursivschrift*, *Unterstreichung* und *Hervorhebung* (unter Beibehaltung der Originalfarben).
* **Bilder**: Automatische Extraktion und Einbindung der im Dokument enthaltenen Bilder.
* **Links**: Hyperlinks oder Verweise aus dem Quelldokument werden zu Hyperlinks im HTML-Dokument.
* **Fußnoten**: Fußnoten werden unterstützt.
* **Konfiguration**: Anpassung über eine `config.py`-Datei (Fußnoten, Google Analytics usw.).

## 🚀 Installation

### Voraussetzungen

* Python 3.x
* Die folgenden Bibliotheken:

```bash
pip install odfpy unidecode mkdocs mkdocs-material

```

### Projektstruktur

Stellen Sie sicher, dass Sie über die folgenden Dateien verfügen:

* `convert.py`: Das Konvertierungsskript.
* `config.py`: Ihre Konfigurationsdatei.
* `Ihr-Dokument.odt/docx`: Das Quelldokument.

## 💻 Verwendung

1. **Konvertierung**
Starten Sie das Skript, indem Sie die ODT-/DOCX-Quelldatei und die Konfigurationsdatei angeben:
```bash
python convert_odt_vxxx.py Ihr-Dokument.odt config.py
python convert_docx_vxx.py Ihr-Dokument.docx config.py
```


*Dadurch wird ein Ordner `docs/` erstellt, der die Markdown-Dateien und eine Datei `mkdocs.yml` enthält.*
2. **Vorschau**
So zeigen Sie die Website lokal an:
```bash
python -m mkdocs serve

```


3. **Generierung**
So erstellen Sie die statische Website (Ordner `site/`):
```bash
python build

```


## ⚙️ Konfiguration (`config.py`)

Die Datei `config.py` ermöglicht die Steuerung des Erscheinungsbilds der Website:

* **mkdocs**: Allgemeine Einstellungen der Website (Titel, Beschreibung, Material-Theme).
* **footer**: Vollständiger HTML-Code zur Anpassung der Fußzeile.
* **code**: Regeln zur Spracherkennung für die Syntaxhervorhebung.
* **extra**: Konfiguration von Google Analytics (GA4).

## 📄 Lizenz

Dieser von **Serge Tahé** verfasste Tutorial-Kurs wird der Öffentlichkeit gemäß den Bedingungen der folgenden Lizenz zur Verfügung gestellt:
*Creative Commons Attribution – Keine kommerzielle Nutzung – Weitergabe unter gleichen Bedingungen 3.0 Unported.*
