# Environment setup

Run these commands from the project root:

```sh
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python -m ipykernel install --prefix "$VIRTUAL_ENV" --name transporttech --display-name "Python (TransportTech)"
python -m jupyterlab notebooks/Ayna_IsmatSamadov.ipynb
```

Select **Python (TransportTech)** and run all cells. Keep the original KMZ filenames in `data/`. Dependencies are listed in [requirements.txt](../requirements.txt).
