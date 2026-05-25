# Art Valuation Master Thesis

This repository contains the empirical code and prepared tabular data used for a master's thesis on art price prediction. The project applies machine learning and deep learning methods to predict artwork prices using tabular metadata and image-based information.

The repository is mainly intended for reproducibility of the thesis workflow rather than as a polished software package.


## Repository Structure

```text
Art-valuation-master-thesis/
│
├── data_divided/
│   ├── training_full.csv
│   ├── validation_full.csv
│   ├── test_full.csv
│   ├── training_cleaned.csv
│   ├── validation_cleaned.csv
│   └── test_cleaned.csv
│
├── thesisdata_cleaned_fullsample1.csv
│
├── division.ipynb
├── modeling.ipynb
├── tree-based models_full.ipynb
├── tree-based_cleaned_dataset.ipynb
├── SHAP_visuals_tabular.ipynb
├── SHAP_visuals_image.ipynb
├── clustering.ipynb
└── visuals.ipynb
```


## Data

The repository contains the prepared tabular datasets in the `data_divided/` folder. These files are already divided into training, validation, and test samples.

The image files are not stored directly in the repository because of their size. They should be downloaded separately from Google Drive:

https://drive.google.com/file/d/1vnH_vPcQxftc2cdxXXBq0S9E0Z7U_6G1/view?usp=drivesdk

After downloading the archive:

1. Unzip it.
2. Place the unzipped image folder inside the main project folder.
3. Make sure the folder is named:

```text
images_thesis
```

The final structure should look like this:

```text
Art-valuation-master-thesis/
│
├── images_thesis/
│   ├── image_1.jpg
│   ├── image_2.jpg
│   └── ...
│
├── data_divided/
├── modeling.ipynb
└── ...
```

This is important because the datasets contain image paths pointing to the `images_thesis` folder.


## Recommended Workflow

The recommended order of using the notebooks is the following.

### 1. Data Division

```text
division.ipynb
```

This notebook was used to divide the data into training, validation, and test samples.

Running this notebook is not compulsory for the standard workflow because the prepared divided datasets are already available in the `data_divided/` folder.

Use it only if you want to recreate the data split from the original dataset.

### 2. Deep Learning Models

```text
modeling.ipynb
```

This notebook contains the deep learning modelling part. It uses the already divided datasets from `data_divided/`.

The notebook includes models based on tabular data, image data, and their combination. Before running it, make sure that the image folder `images_thesis/` is placed in the main project directory.


### 3. Tree-Based Models

```text
tree-based models_full.ipynb
tree-based_cleaned_dataset.ipynb
```

These notebooks contain tree-based regression models used for art price prediction.

The full-sample notebook uses the full divided datasets, while the cleaned-dataset notebook uses the cleaned version of the divided data.

The models include standard tree-based approaches such as Decision Tree, Random Forest, and XGBoost.

### 4. SHAP Visualisations

```text
SHAP_visuals_tabular.ipynb
SHAP_visuals_image.ipynb
```

These notebooks are used for model interpretation and visualisation of feature importance with SHAP values.

The tabular SHAP notebook is related to models based on metadata variables, while the image SHAP notebook is related to models using image-derived features.

### 5. Clustering

```text
clustering.ipynb
```

This notebook contains additional exploratory clustering analysis of the artworks.

### 6. General Visualisations

```text
visuals.ipynb
```

This notebook contains descriptive plots and exploratory visualisations used during the analysis.


## Installation

The project was developed in Python using Jupyter Notebook.

The main libraries used in the repository include:

```text
pandas
numpy
matplotlib
seaborn
scikit-learn
tensorflow
xgboost
opencv-python
scikit-image
shap
joblib
```

A typical installation command is:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow xgboost opencv-python scikit-image shap joblib
```

It is recommended to use a virtual environment or Anaconda environment.


## Important Notes

Some notebooks may contain local paths or intermediate outputs created during the thesis work. If the project is moved to another computer, paths may need to be adjusted manually.

The repository is organised according to the actual research workflow of the thesis. Therefore, the code is intended mainly for transparency and reproducibility of the empirical results, not as a general-purpose production pipeline.

## Author

Kostiantyn Okhrimenko