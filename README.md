# Country Clustering Analysis

This repository contains data collection and analysis notebooks used to cluster countries by sector (economy, education, health, infrastructure, social, etc.) and to inspect feature importance for those clusters. Project carried out as part of classes at the Wrocław University of Science and Technology in Polish.

**Purpose:** gather and prepare socio-economic indicators, run clustering per sector, and analyze which features drive cluster assignments.

---

**Key files and directories**
- `Analiza_Klastracji.ipynb` — main analysis notebook with visualizations and results.
- `Collect_data.ipynb` — notebook that downloads indicators (World Bank) and prepares datasets.
- `Combine.ipynb`, `Merge.ipynb`, `Main.ipynb`, `Most_recent_data.ipynb` — helper notebooks for merging and preparing data.
- `analiza.py` — utility script for running per-sector analyses (not imported elsewhere; kept as reference).
- `data/` — processed output data (subfolders: `economy`, `education`, `healthcare`, `infrastructure`, `social`).
- `dane/` — raw source data files (e.g., GDP, Gini).
- `requirements.txt` — Python dependencies for the project.
- `venv/` — local virtual environment (do not remove unless intentional).

---

**Quick start (Windows / PowerShell)**

1. Create and activate a virtual environment:

```powershell
python -m venv venv
.\\venv\\Scripts\\Activate.ps1
```

2. Install dependencies:

```powershell
pip install -r requirements.txt
```

3. Start Jupyter Lab and open the notebooks:

```powershell
pip install jupyterlab
jupyter lab
```

4. Run `Collect_data.ipynb` to download and prepare datasets in `data/`.

5. Run `Analiza_Klastracji.ipynb` to reproduce visualizations and feature-importance analyses.

---

**Notes & troubleshooting**
- If you get an error like `TypeError: '<' not supported between instances of 'float' and 'str'` when sorting cluster names, ensure the `Cluster_Name` column has a consistent type (e.g., `df['Cluster_Name'] = df['Cluster_Name'].astype(str)`) or use `sorted(..., key=str)`.
- `analiza.py` is not imported by other project files — keep it as a helper script or move it to an archive if unused.
- You can safely remove or archive `.ipynb_checkpoints/` directories (these are automatic notebook checkpoints).

---

**Recommended next steps**
- Archive temporary/duplicate notebooks to `.archive/` before permanent deletion.
- Add a `CLEANUP_LOG.md` recording moved/deleted files.

---

If you want, I can now create a `.archive/` folder and move selected files there (keeps a safe copy), or permanently delete files you confirm.
