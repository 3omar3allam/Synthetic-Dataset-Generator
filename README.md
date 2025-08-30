# Synthetic Dataset Generator

Synthetic Dataset Generator is a simple tool for generating artificial datasets for experimentation, testing, and prototyping. It allows users to specify the type of dataset and number of records, and then outputs the generated data.  

The app runs on [Gradio](https://gradio.app) in Google Colab and uses the open-source model **meta-llama/Meta-Llama-3.1-8B-Instruct** locally.  

---

## Quick Start

Launch the app directly in Google Colab:  

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/synthetic-dataset-generator/synthetic-dataset-generator/blob/main/notebook.ipynb)

---

## Features

- **Dataset Generation**
  - Enter a dataset type (e.g., "customer data", "sales records", "IoT sensor logs") and number of records.
  - The app generates the requested synthetic data with no external data sources involved.

- **Custom Attributes**
  - Optionally specify the attributes (columns) of the dataset.
  - If no attributes are provided, the model automatically decides suitable columns.

- **CSV Export**
  - Download the generated dataset as a CSV file for reuse.

- **Caching on Google Drive**
  - The model is cached in your Google Drive to prevent re-downloading across sessions.
  - Saves both time and bandwidth in repeated runs.

---

## Requirements

- Google Colab account  
- Python 3.9+  
- Installed dependencies (handled automatically in Colab):
  - `gradio`
  - `transformers`
  - `torch`
  - `pandas`

---

## How It Works

1. Clone or open the Colab notebook containing the app.
2. Mount your Google Drive (for model caching).
3. Launch the Gradio interface in Colab.
4. Enter:
   - Dataset type (mandatory).
   - Number of records (mandatory).
   - Attributes/columns (optional).
5. View and interact with the generated dataset in the Gradio UI.
6. Export the dataset as a CSV file if desired.

---

## Example Usage

- **Generate random user data**
  ```
  Dataset type: User Profiles
  Records: 100
  Attributes: name, age, email, country
  ```

- **Generate without specifying attributes**
  ```
  Dataset type: Online Orders
  Records: 50
  Attributes: (leave empty)
  ```

---

## Notes

- This app generates **synthetic data only**. It does not rely on or fetch from any external or real-world data source.
- Model caching in Google Drive is optional but recommended for efficiency.
- Since the app runs in Colab, performance may vary depending on GPU availability.
