# Lviv Stops Analysis

An exploratory analysis of public-transport stop locations in and around Lviv. The project uses a Jupyter notebook to inspect the supplied stop dataset and visualize stop counts by street and settlement, as well as their geographic distribution.

## Project files

- `analysis.ipynb` — the analysis notebook.
- `stops.csv` — the input dataset. It includes stop names, latitude and longitude, settlement names, street names, and other stop-related fields.

The notebook expects `stops.csv` to be in the project root.

## Analysis

The notebook:

1. Loads and inspects the CSV data.
2. Filters records geographically for the Lviv area.
3. Plots the ten streets with the most stops.
4. Plots stop locations using their longitude and latitude.
5. Summarizes stops by settlement, including a chart of the top seven.

## Findings

- The analysis includes 1,034 stops in the Lviv area.
- 254 stops (about 25%) are outside the main city, distributed across 19 other settlements.
- 1,007 stops have a street name recorded, so street-level counts exclude 27 records without that information.

## Requirements

- Python 3
- Jupyter support
- pandas
- Matplotlib
- NumPy

## Setup on Windows

Open PowerShell in the project directory and create a virtual environment:

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
```

Install the dependencies:

```powershell
python -m pip install --upgrade pip
python -m pip install pandas matplotlib numpy ipykernel
```

In VS Code, open `analysis.ipynb`, select the `.venv` Python environment as the notebook kernel, and run the cells from top to bottom (or choose **Run All**). The notebook loads `stops.csv` using a relative path, so run it with the project root as the working directory.

## Data Source & License

The dataset used in this project is provided by the Lviv City Council and LCE "City Center of Information Technologies" via the [Lviv Open Data Portal](https://opendata.city-adm.lviv.ua/).

The data is publicly available and licensed under the [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) license.
