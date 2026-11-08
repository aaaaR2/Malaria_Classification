# Malaria cell image classification

Clone this repository into a folder named `malaria_classification`.

## Dataset

Download and extract the [NLM cell images](https://data.lhncbc.nlm.nih.gov/public/Malaria/cell_images.zip). Place the two class folders beside the notebook as shown below; avoid an extra nested `cell_images` folder.

```text
malaria_classification/
├── pipeline.ipynb
├── cell_images/
│   ├── Parasitized/
│   └── Uninfected/
└── metadata/
    ├── patientid_cellmapping_parasitized.csv
    └── patientid_cellmapping_uninfected.csv
```

The patient mappings are included. The dataset, `.venv/` is excluded from Git.

## Run

From `malaria_classification`, use Python 3.13:

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

Open `pipeline.ipynb` in VS Code, select `.venv/Scripts/python.exe` as the kernel, and run the cells in order. The notebook prepares images and model inputs; it does not train the models. Split manifests are in `artifacts/`; other preprocessing outputs are regenerated there.

If the kernel is not listed, register it, reload VS Code, and select **Malaria project (malaria_classification/.venv)**:

```powershell
.\.venv\Scripts\python.exe -m ipykernel install --user --name malaria-project --display-name "Malaria project (malaria_classification/.venv)"
```
