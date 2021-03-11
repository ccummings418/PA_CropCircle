# Useful Precision Ag Tools
These are the useful tools and coding tricks I have developed for PA management in corn. 

Created by Cadan Cummings

## Crop Circle Phenom Excel Macro
#### About the Sensor
The Holland Scientific Crop Circle Phenom is a multiparameter active sensing instrument capable of measuring red, NIR, and red-edge bands as well as climatic and physiological measurements, including upwelling and downwelling PAR, air / canopy temperature and atmospheric pressure.

The readings are measured approximately once per second for each band and are stored in a CSV file. 

#### Use Case for VBA Macro
Since the Crop Circle Phenom instrument combines ACS-430 and DAS43X measurements into one CSV file per log measurement, several pre-processing steps are needed to organize the data. The steps I found useful were: 1.) Combine all the RAW CSV files from each sensing date/ field, 2.) organize the readings by sensor, and 3.) summarize the date by plot / treatment.

##### Step 1 - Combining RAW CSV Files
-Create a new folder with field and sensor date (i.e. Borlaug_06102020)
-Inside the folder create another file named RAW files
-Copy and paste the CC-Phenom measurements into the RAW folder


##### Step 2 - Organize Readings Per Sensor (ACS-430 and DAS43X)

##### Step 3 - Organize Readings Per Sensor (ACS-430 and DAS43X)


## Machine Learning - XGBoost with Hyperparameter Tuning
