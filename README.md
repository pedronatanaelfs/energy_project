# Wind Energy Demand Forecasting in Brazil

## Introduction

This project aims to forecast wind energy demand in Brazil based on historical generation data. The data used in this project is sourced from the following URL: [ONS Dataset](https://dados.ons.org.br/dataset/geracao-usina-2). 

The project follows the CRISP-DM methodology and is being developed by Pedro and Morgan, students of the Graduate Program in Computer Engineering at the University of Pernambuco (PPGEC - UPE).

## Reproducing the Project

To reproduce this project, follow the steps below:

1. **Clone the repository:**
    ```bash
    git clone https://github.com/username/wind-energy-demand-forecast.git
    cd wind-energy-demand-forecast
    ```

2. **Create a virtual environment and activate it:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. **Install the required packages:**
    ```bash
    pip install -r requirements.txt
    ```

## Project Structure

- **data/**: Contains the raw data used for the analysis.
- **data_dict/**: Contains the data dictionary which explains the dataset.
- **notebooks/**: Contains Jupyter notebooks used for the analysis and modeling.

## Data Understanding

The dataset provides hourly generation data from various wind power plants in Brazil. Here are the key attributes:

- **din_instante**: Reference date and time (YYYY-MM-DD HH:MM:SS)
- **id_subsistema**: Subsystem ID (3 positions)
- **nom_subsistema**: Subsystem name (20 positions)
- **id_estado**: State ID (2 positions)
- **nom_estado**: State name (30 positions)
- **cod_modalidadeoperacao**: Operation modality (20 positions, allows null)
- **nom_tipousina**: Plant type (30 positions)
- **nom_tipocombustivel**: Fuel type (50 positions)
- **nom_usina**: Plant name (60 positions)
- **id_ons**: ONS identifier (up to 32 positions)
- **ceg**: Unique generation enterprise code established by ANEEL (30 positions, allows null)
- **val_geracao**: Generation value in MWmed (20 positions, allows zero values)

### Data Description

- The dataset includes verified generation data from individual plants, groups of plants, and small plant clusters on an hourly basis.
- The groups consist of plants classified under Type II-C, as per Submodule 7.2 of the Network Procedures, established in Operational Adjustments available in the MPO.
- Small plant clusters are composed of Type III plants, which are not directly connected to the ONS, and the data includes generation forecasts.

## Methodology: CRISP-DM

### 1. Business Understanding
Define the objectives and requirements from a business perspective, focusing on forecasting wind energy demand in Brazil to optimize energy distribution and grid management.

### 2. Data Understanding
Initial data collection and exploration. This includes understanding the dataset's structure, attributes, and potential data quality issues.

### 3. Data Preparation
Process the raw data to prepare it for modeling. This involves cleaning, transforming, and integrating data from various sources.

### 4. Modeling
Select and apply appropriate modeling techniques. In this case, time series forecasting models will be used.

### 5. Evaluation
Evaluate the models to ensure they meet the business objectives. This involves validating the model's accuracy and performance.

### 6. Deployment
Deploy the model to a production environment where it can be used for making predictions in real-time.

## Authors

This project is being developed by:
- Pedro
- Morgan

Graduate Program in Computer Engineering, University of Pernambuco (PPGEC - UPE)

---

By following the above steps and understanding the project structure, you will be able to reproduce and contribute to the project effectively.
