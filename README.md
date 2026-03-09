# Python Grundlagen

Kursmaterialien und Jupyter-Notebooks fuer den dreitaegigen Einstiegskurs **Python Grundlagen**. Der Kurs richtet sich an Wissenschaftlerinnen und Wissenschaftler (und andere Interessierte) ohne Vorkenntnisse in Python.

## Miniforge (Conda Forge) unter Windows installieren

Fuer den Kurs wird **Miniforge** empfohlen (Conda mit conda-forge als Standard-Channel).

1. **Installer herunterladen**: [Miniforge Releases](https://github.com/conda-forge/miniforge/releases) – fuer Windows 64-Bit z.B. `Miniforge3-Windows-x86_64.exe`.
2. **Installer ausfuehren**: Doppelklick auf die `.exe`, den Anweisungen folgen. Option "Add Miniforge3 to my PATH" aktivieren, damit `conda` im Terminal verfuegbar ist.
3. **Terminal neu oeffnen**: Nach der Installation ein neues Terminal (PowerShell oder Eingabeaufforderung) oeffnen und pruefen:
   ```bash
   conda --version
   ```

4. **Conda in anderen Terminals (z.B. Git Bash)**: Wenn du Git Bash oder ein anderes Bash-Terminal nutzt, ist `conda` dort zunaechst oft nicht verfuegbar. Einmalig in einem Terminal ausfuehren, in dem `conda` schon funktioniert (z.B. Miniforge Prompt oder PowerShell):
   ```bash
   conda init bash
   ```
   Anschliessend Git Bash (oder das andere Bash-Terminal) neu starten – danach funktioniert `conda` auch dort.

## Setup

Kursumgebung mit Miniforge/Conda einrichten:

```bash
conda env create -f environment.yml
conda activate python_grundlagen
```

Bestehende Umgebung aktualisieren:

```bash
conda env update -n python_grundlagen -f environment.yml --prune
```

## Verzeichnisstruktur

```
python_grundlagen/
├── day1/                          # Tag 1: Python-Grundlagen und Datenstrukturen
│   ├── 00_python_ueberblick.ipynb
│   ├── 01_datentypen_variablen_objekte.ipynb
│   ├── 02_strings_zeichenketten.ipynb
│   ├── 03_dictionaries_sets.ipynb
│   └── Tag1_Zusammenfassung.md
├── day2/                          # Tag 2: Kontrollstrukturen, E/A, Module
│   ├── 04_bedingungen_verzweigungen.ipynb
│   ├── 05_schleifen.ipynb
│   ├── 06_funktionen.ipynb
│   ├── 07_ein_ausgabe_dateien.ipynb
│   ├── 08_module_bibliotheken.ipynb
│   └── Tag2_Zusammenfassung.md
├── day3/                          # Tag 3: Fehlerbehandlung, OOP, Ausblick
│   ├── 09_fehler_ausnahmen.ipynb
│   ├── 10_oop_klassen_grundlagen.ipynb
│   ├── 11_oop_vererbung.ipynb
│   ├── 12_ausblick_bibliotheken.ipynb
│   └── Tag3_Zusammenfassung.md
├── data/                          # Datensatze (CSV, Logs, Text) fuer Ubungen
├── environment.yml
└── README.md
```

### Nummerierung der Notebooks

Die Notebooks sind fortlaufend uber alle Tage nummeriert:

- Tag 1: 00-03
- Tag 2: 04-08
- Tag 3: 09-12

## Wichtige Dateien

- **environment.yml**: Conda-Umgebung (Python 3.13, Jupyter, ggf. NumPy/Matplotlib fuer Tag 3)
- **00_uebersicht.md**: Kursuberblick, Lernziele, Ablauf pro Tag
- **TagN_Zusammenfassung.md**: Pro Tag eine Zusammenfassung der Themen und Konzepte

## Nutzung

### Reihenfolge

1. Notebooks in numerischer Reihenfolge durcharbeiten (00, 01, 02, ...).
2. Jeder Tag baut auf dem vorherigen auf.

### Aufgaben und Losungen

Jedes Notebook enthalt Theorie, Beispiele und ggf. Aufgaben. Die Musterlosungen stehen unter der Uberschrift **#### Losung:** und sind standardmaessig eingeklappt. Auf die Uberschrift klicken, um die Losung anzuzeigen.

### Technische Details

- Python 3.13
- Jupyter Notebook (.ipynb)
- Conda-Umgebung: `python_grundlagen`

## Support

- Tag-Zusammenfassungen (`dayN/TagN_Zusammenfassung.md`) zur Wiederholung
- Musterlosungen in den Notebooks
- Offizielle Python-Dokumentation: https://docs.python.org/3/
