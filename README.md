# Python Basics

Course materials and Jupyter notebooks for the three-day introductory course **Python Basics**. The course is aimed at scientists and researchers (and other interested parties) with no prior knowledge of Python.

## Setup: Miniforge and IDE

### 1. Installing Miniforge (Python + Conda)

**Miniforge** is a minimal installer that provides **Conda** (package and environment manager) with **conda-forge** as the default package channel. It is the preferred way to get Python for this course.

1. **Download**: Go to [conda-forge.org/download](https://conda-forge.org/download/) and download the installer for your system:
   - **Windows**: `Miniforge3-Windows-x86_64.exe` (64-bit)
   - **macOS**: Choose ARM64 (Apple Silicon) or x86_64 (Intel)
   - **Linux**: Choose the appropriate architecture

2. **Install**: Run the installer. On Windows, enable **"Add Miniforge3 to my PATH"** so that `conda` is available in any terminal.

3. **Verify**: Open a new terminal (PowerShell, Command Prompt, or Miniforge Prompt) and run:
   ```bash
   conda --version
   ```

4. **Conda in Git Bash** (optional): If you use Git Bash, run once in a terminal where `conda` works:
   ```bash
   conda init bash
   ```
   Then restart Git Bash.

### 2. Installing VS Code (IDE)

**VS Code** (Visual Studio Code) is a free **text and code editor** with many useful extensions. It supports Python, Jupyter notebooks, debugging, and integrated terminals.

1. **Download**: [code.visualstudio.com](https://code.visualstudio.com/)
2. **Install**: Run the installer and follow the steps.
3. **Extensions** (recommended for this course):
   - **Python** (by Microsoft) – Python support, IntelliSense, debugging
   - **Jupyter** (by Microsoft) – run and edit Jupyter notebooks inside VS Code

### 3. Course environment

Set up the course environment with Conda (run in a terminal from the course folder):

```bash
conda env create -f environment.yml
conda activate python_basics
```

Update an existing environment when `environment.yml` has changed (e.g. new packages added):

```bash
conda env update -n python_basics -f environment.yml --prune
```

Use your actual environment name instead of `python_basics` if you created it differently (e.g. `python_grundlagen`):

```bash
conda env update -n python_grundlagen -f environment.yml --prune
```

`--prune` removes packages that are no longer listed in the yml file.

### 4. Using VS Code with a notebook (.ipynb)

1. **Open the course folder**: In VS Code, go to **File → Open Folder** and select the folder containing this README.
2. **Open a notebook**: In the file explorer (left sidebar), open a `.ipynb` file (e.g. `day1/00_python_overview.ipynb`).
3. **Select the kernel**: At the top right of the notebook, click **Select Kernel** (or the kernel name). Choose **Python Environments** → `python_basics` (or your environment name).
4. **Run a cell**: Click the play button next to a cell, or press **Shift+Enter** to run the cell and move to the next one.

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
├── day4/                          # Day 4: Logging, lambdas, NumPy, Pandas, APIs, tools, TIFF
│   ├── 13_logging.ipynb
│   ├── 14_lambda_functions.ipynb
│   ├── 15_numpy.ipynb
│   ├── 16_pandas_matplotlib.ipynb
│   ├── 17_using_apis.ipynb
│   ├── 18_python_tools_overview.ipynb
│   └── 19_tiff.ipynb
├── data/                          # Datasets (CSV, logs, text) for exercises
├── environment.yml
└── README.md
```

### Notebook Numbering

Notebooks are numbered continuously across all days:

- Day 1: 00-03
- Day 2: 04-08
- Day 3: 09-12
- Day 4: 13-19

## Important Files

- **environment.yml**: Conda environment (Python 3.13, Jupyter, NumPy, Pandas, Matplotlib, requests, tifffile)
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
