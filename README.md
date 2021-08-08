
# MINTS Solar Irradiance Estimation


## Environment Requirements

	conda env create -f environment.yml
	conda activate geo_env



# Run the Codes from the Raw Data Files

If you are researchers in our MINTS team, and want to repeat all the work from the raw data file, please follow these steps:

## File Path:

Place the codes in this Repository into ./src/ folder, for example:

	./src/spatial.m

Data of Minolta sensor:

	./Minolta/node_id/year/month/day/...,  where node_id = '10004098'

Data of GPS sensor:

	./Minolta/node_id/year/month/day/...,  where node_id = '001e0610c2e9'

Create this folder to save the preprocessed data files:

	./data/

Create this folder to save figures:

	./figures/

Create this folder to save the trained models:

	./models/

## Data Preprocessing:

To prepare the data of Minolta sensor, run:

	python data_minolta.py

To prepare the data of GPS with Minolta sensor, run:

	python data_gps.py

After the above 2 steps, to add solar angles (Zenith angle and Azimuth angle), run:

	data_driving.py

To visualize the spatial and temporal variation of the irradiance, run:

	matlab spatial.m


To merge the NEXRAD data,

	spatial.ipynb

To merge the Landsat-8 data,

	matlab spatial_merge_landsat.m




## Run the model

in jupyter notebook, run:

	model_spatial.ipynb

if you are running the model for the default node '001e06305a6b' with data file '10004098_001e06305a6b.csv', you don't need to do any modification in the codes;

Otherwise, you might need to manually pick up appropriate datetimes in the testing dataset to "Compare Actual Spectrum and Estimated Spectrum" in a typical weather condition, like sunny or cloudy.



[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.5125484.svg)](https://doi.org/10.5281/zenodo.5125484)

# Neighborhood-Scale-Solar-Irradiance-Estimation
