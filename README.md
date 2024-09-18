# COVID Bayesian Network Project

This repository contains the development of a Bayesian Network model for analyzing COVID-19 data in U.S. counties. The goal of this project is to provide a probabilistic model that estimates various outcomes related to COVID-19 spread and control measures in different regions.

## Table of Contents

- [Introduction](#introduction)
- [Project Structure](#project-structure)
- [Data](#data)
- [Usage](#usage)
- [Dependencies](#dependencies)
- [Future Work](#future-work)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The **COVID Bayesian Network Project** aims to create a probabilistic model that captures dependencies between different variables influencing the spread of COVID-19 across U.S. counties. Using a Bayesian Network approach, the model infers the likelihood of infection rates, hospitalizations, and other related metrics, given certain observed data.

The model is built using historical COVID-19 data and geographic information related to U.S. counties, as well as key factors such as population density and public health measures. The goal is to help better understand the relationships between different factors affecting the pandemic's spread and provide predictions based on those relationships.

## Project Structure

├── UScounties.dbf # Geographic data files for U.S. counties ├── UScounties.prj # Projection information for county data ├── UScounties.shp # Shapefile containing U.S. county boundaries ├── UScounties.shx # Index of the .shp file ├── UScounties.sbn # Spatial index for the shapefile ├── UScounties.sbx # Spatial index for the shapefile ├── covidData2021-2022.csv # COVID-19 data (2021-2022) ├── bayesianNetworkCovidFINALDEMO.ipynb # Final Bayesian Network demonstration notebook └── README.md # This README file


## Data

- **Geospatial Data**: U.S. counties' geographic information is provided in the form of shapefiles (.shp), projection files (.prj), and database files (.dbf).
- **COVID-19 Data**: The dataset `covidData2021-2022.csv` contains COVID-19 infection rates, hospitalizations, and other health-related metrics for different U.S. counties between 2021 and 2022.

## Usage

To use this project:

1. Clone the repository:
    ```bash
    git clone https://github.com/ZachariahAlzubi/COVID-BAYESIAN-NETWORK.git
    ```

2. Install the required dependencies (see below).

3. Open the Jupyter notebook `bayesianNetworkCovidFINALDEMO.ipynb` for a complete demonstration of the Bayesian Network model. The notebook provides a step-by-step guide on how the model is built, trained, and tested using the provided data.

4. Run the cells in the notebook to generate the probabilistic relationships between the variables and visualize the output.

## Dependencies

This project requires the following dependencies:

- Python 3.x
- Jupyter Notebook
- Pandas
- NumPy
- PyShp
- PyBN (for Bayesian Network implementation)

To install the necessary packages, you can use the following command:

(bash)
'pip install pandas numpy pyshp pybn'

## Future Work

Add more detailed COVID-19 data, including vaccine distribution and effectiveness.
Improve the Bayesian Network by adding more variables related to social behavior and economic impact.
Expand the model to predict other health outcomes and policy effectiveness.
Contributing

Contributions are welcome! If you'd like to contribute, please fork the repository and create a pull request. For major changes, please open an issue first to discuss what you'd like to change.

