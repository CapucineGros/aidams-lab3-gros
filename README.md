# aidams-lab3-gros

# Lab 3: **Bottom-Up Steel Emissions with Uncertainty** (AIDAMS).

The notebook `lab3.ipynb` has two parts:

- **Part A:** emissions pipeline built from plant-level data (operating plants 2020-2030, utilisation by technology, plant and company emissions, projection to 2030).
- **Part B:** uncertainty quantification (reality check against worldsteel statistics, matched utilisation, bootstrap, Monte Carlo simulation, scenarios, communication of results).

## Author

Capucine GROS

## Requirements

- Python 3.10 or later
- Jupyter (Notebook or JupyterLab)
- Python packages: `numpy`, `pandas`, `matplotlib`, `scipy`, `openpyxl`

```bash
pip install numpy pandas matplotlib scipy openpyxl notebook
```

## Data

The notebook uses the Global Energy Monitor file
**"Plant-level data - Global Iron and Steel Tracker - September 2026 (V1).xlsx"**
(download from the Global Iron and Steel Tracker page of Global Energy Monitor).

Put the file in the **same folder as `lab3.ipynb`**. To use another location or file name, set the `GIST_PATH` environment variable before starting Jupyter:

```bash
export GIST_PATH="/path/to/Plant-level data - Global Iron and Steel Tracker - September 2026 (V1).xlsx"
```

## How to run

1. Clone the repository and open a terminal in its folder.
2. Install the requirements (see above) and place the data file next to the notebook.
3. Start Jupyter and open `lab3.ipynb`:
   ```bash
   jupyter notebook lab3.ipynb
   ```
4. Run **Kernel -> Restart & Run All**. The cells must be run in order, because later cells use variables created earlier. Random seeds are fixed (`SEED = 42`), so results are reproducible.

## Notes

- This version of the dataset (September 2026) differs from the one mentioned in the lab (September 2025): some column names differ (`GEM plant ID`, `Country/area`) and are renamed in the notebook. China has no crude steel production reported after 2024, so the observed years are 2020-2024. Results may therefore differ slightly from the expected ones; see the note at the top of the notebook.
- Official crude steel figures for China come from worldsteel (*World Steel in Figures*); the source is given in the notebook (section B1).
