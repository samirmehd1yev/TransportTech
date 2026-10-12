# TransportTech

[TransportTech_analysis.ipynb](TransportTech_analysis.ipynb) answers the AYNA hackathon brief using the two supplied KMZ files. It includes executed calculations, data checks, interactive maps, all 185 parking results, and a 65-word proposal in Azerbaijani.

Results from the supplied files:

- **1.1:** `57.14, 8 Noyabr pr.` — total lane length in EPSG:32639; 8 Noyabr contributes 13.856291 km.
- **1.2:** `87` parking points are within 50 metres of existing lanes.
- **1.3:** `4: MPV-144-2, MPV-145-2, MPV-146-2, MPV-147-2` fall outside the specified Baku bounds.

The analysis uses only the requested layers. One empty lane record is excluded and documented. The proposed northern extension along Azadlıq prospekti is a preliminary priority based on the parking distribution; the files do not establish construction costs or times.

## Run the notebook

From this project directory:

```sh
source .venv/bin/activate
python -m jupyterlab TransportTech_analysis.ipynb
```

Select **Python (TransportTech)** as the kernel and choose **Restart Kernel → Run All**. Keep both KMZ files in the notebook's directory with their original filenames. Map rendering needs internet access; calculations use local files.

The local `.venv` contains the required packages and its own Jupyter kernel. It is excluded from Git. The notebook has been checked with Python 3.14.7.

## Re-create the environment

```sh
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python -m ipykernel install --prefix "$VIRTUAL_ENV" --name transporttech --display-name "Python (TransportTech)"
```

For submission, rename the notebook to the brief's `Team_Leader.ipynb` format and submit only the notebook.
