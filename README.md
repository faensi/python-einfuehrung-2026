# Python Basics

Course materials and Jupyter notebooks for the three-day introductory course **Python Basics**. The course is aimed at scientists and researchers (and other interested parties) with no prior knowledge of Python.

## Installing Miniforge (Conda Forge) on Windows

**Miniforge** is recommended for the course (Conda with conda-forge as the default channel).

1. **Download installer**: [Miniforge Releases](https://github.com/conda-forge/miniforge/releases) - for Windows 64-bit use e.g. `Miniforge3-Windows-x86_64.exe`.
2. **Run installer**: Double-click the `.exe`, follow the instructions. Enable the option "Add Miniforge3 to my PATH" so that `conda` is available in the terminal.
3. **Restart terminal**: After installation, open a new terminal (PowerShell or Command Prompt) and verify:
   ```bash
   conda --version
   ```

4. **Conda in other terminals (e.g. Git Bash)**: If you use Git Bash or another Bash terminal, `conda` may not be available there initially. Run once in a terminal where `conda` already works (e.g. Miniforge Prompt or PowerShell):
   ```bash
   conda init bash
   ```
   Then restart Git Bash (or the other Bash terminal) - after that, `conda` will work there too.

## Setup

Set up the course environment with Miniforge/Conda:

```bash
conda env create -f environment.yml
conda activate python_basics
```

Update an existing environment:

```bash
conda env update -n python_basics -f environment.yml --prune
```

## Directory Structure

```
python_basics/
├── day1/                          # Day 1: Python basics and data structures
│   ├── 00_python_overview.ipynb
│   ├── 01_data_types_variables_objects.ipynb
│   ├── 02_strings.ipynb
│   ├── 03_dictionaries_sets.ipynb
│   └── Day1_Summary.md
├── day2/                          # Day 2: Control structures, I/O, modules
│   ├── 04_conditions_branches.ipynb
│   ├── 05_loops.ipynb
│   ├── 06_functions.ipynb
│   ├── 07_input_output_files.ipynb
│   ├── 08_modules_libraries.ipynb
│   └── Day2_Summary.md
├── day3/                          # Day 3: Error handling, OOP, outlook
│   ├── 09_errors_exceptions.ipynb
│   ├── 10_oop_classes_basics.ipynb
│   ├── 11_oop_inheritance.ipynb
│   ├── 12_outlook_libraries.ipynb
│   └── Day3_Summary.md
├── data/                          # Datasets (CSV, logs, text) for exercises
├── environment.yml
└── README.md
```

### Notebook Numbering

Notebooks are numbered continuously across all days:

- Day 1: 00-03
- Day 2: 04-08
- Day 3: 09-12

## Important Files

- **environment.yml**: Conda environment (Python 3.13, Jupyter, NumPy/Matplotlib for Day 3)
- **00_overview.md**: Course overview, learning objectives, schedule per day
- **DayN_Summary.md**: Per-day summary of topics and concepts

## Usage

### Order

1. Work through notebooks in numerical order (00, 01, 02, ...).
2. Each day builds on the previous one.

### Tasks and Solutions

Each notebook contains theory, examples, and optionally tasks. Model solutions are under the heading **#### Solution:** and are collapsed by default. Click the heading to expand the solution.

### Technical Details

- Python 3.13
- Jupyter Notebook (.ipynb)
- Conda environment: `python_basics`

## Support

- Day summaries (`dayN/DayN_Summary.md`) for review
- Model solutions in the notebooks
- Official Python documentation: https://docs.python.org/3/
