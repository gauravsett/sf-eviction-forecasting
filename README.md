# Forecasting Eviction in San Francisco with Spatial Methods

_By:_ Daniel Basman and Gaurav Sett

_Abstract:_ We employ tax assessor data to forecast evictions in San Francisco. Using the proximate measure of eviction notices filed with the San Francisco Rent Board, we train a machine learning model to predict the likelihood of a filing on a given block in the city. The dataset analyzed includes a wide range of containing property characteristics, ownership information, and tax payment history of land parcels aggregated at the block level We investigate the usefulness of spatial features for this task. We compute averages of our tax data across neighborhoods as well as metrics representing each blocks position in a spatial network. Identifying these factors can help us gain a better understanding of the relationship between property characteristics and eviction likelihood for further research or more effective policy. This in turn can lead to more stable and affordable housing options for residents of San Francisco.

### Setup

To run the code in this repository, you will need to install the packages in our     file. We recommend using a virtual environment to do this. To do so, run the following commands in your terminal:

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### Data

The data used in this project is available on the [San Francisco Open Data Portal](https://data.sfgov.org/). The raw files are very large and are not saved in the respository.
The first dataset we use is the [Eviction Notices](https://data.sfgov.org/Housing-and-Buildings/Eviction-Notices/5cei-gny5) dataset. In our code, it is referenced as `data/evictions.csv`.
The second dataset we use is the [Assessor Historical Secured Property Tax Rolls](https://data.sfgov.org/Housing-and-Buildings/Assessor-Historical-Secured-Property-Tax-Rolls/wv5m-vpq2) dataset. In our code, it is referenced as `data/parcels.csv`.
The preprocessed data is saved in the `data/` directory under `parcels.parquet`. Our training input is saved in `input.parquet`.

### Demo

To run the demo, see the `src/analysis.ipynb` notebook. This notebook contains the code used to preprocess the data, train the model, and evaluate the forecasts. The notebook also contains the code used to generate the figures in the report.