A simple end-to-end project that predicts movie box-office revenue from metadata and provides an interactive Tkinter GUI for live predictions.
This repository contains a Jupyter notebook and a stand-alone script version of the pipeline: data cleaning → feature engineering → model training (Random Forest by default) → evaluation → GUI.

## Contents:

notebook.ipynb — recommended: notebook broken into cells (Imports, Data Cleaning, Feature Engineering, Model Training & Evaluation, GUI).

app.py — optional script version that runs the entire pipeline and launches the GUI (if provided).

movies_metadata.csv — dataset (place in repository root). Not included — you must provide this file.

README.md — this file.

## Running the code:

Place movies_metadata.csv in the notebook folder.

Open the notebook (notebook.ipynb) in JupyterLab / Jupyter Notebook.

Run cells in order:

Cell 1: Imports & constants

Cell 2: Data loading & cleaning

Cell 3: Feature engineering

Cell 4: Model training & evaluation — choose model & dataset fraction here

Cell 5: GUI — run this last to launch the Tkinter app

In Cell 4 you can change:
SAMPLE_FRAC (e.g., 0.05, 0.5, 1.0) to use more data
Hyperparameters: n_estimators, max_depth, min_samples_split, min_samples_leaf

## GUI Usage:

### Click Show Training Stats to view:

  Top 10 movies by revenue (original units)
    
   Summary statistics
   
   Correlation with revenue
   
   Model evaluation metrics (log & USD)

### Fill form:

   Budget (USD)
    
   Runtime (min)
    
   Popularity
    
   Vote Average
    
   Vote Count
    
   Cast Count
    
   Select genres (top 12)

### Click Predict — app displays:

   Predicted Revenue (USD)
   
   Input summary (original units)
   
   Prediction status vs median revenue (SUCCESS / NOT SUCCESSFUL)
