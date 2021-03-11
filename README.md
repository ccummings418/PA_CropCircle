# Useful Precision Ag Tools
*These are some useful tools and coding tricks I have developed for PA management in corn.* 

Created by Cadan Cummings

## Crop Circle Phenom Excel Macro
#### About the Sensor
The Holland Scientific Crop Circle Phenom is a multiparameter active sensing instrument capable of measuring red, NIR, and red-edge bands as well as climatic and physiological measurements, including upwelling and downwelling PAR, air / canopy temperature and atmospheric pressure.

The readings are measured approximately once per second for each band and are stored in a CSV file. 

#### Use Case for VBA Macro
Since the Crop Circle Phenom instrument combines ACS-430 and DAS43X measurements into one CSV file per log measurement, several pre-processing steps are needed to organize the data. The steps I found useful were: 1.) Combine all the RAW CSV files from each sensing date/ field, 2.) organize the readings by sensor, and 3.) summarize the date by plot / treatment.

![PhenomLog0](https://user-images.githubusercontent.com/80427122/110829379-abc02d80-825d-11eb-9d12-517efd8796d6.png)


##### Step 1 - Combining RAW CSV Files
* Create a new folder with field and sensor date (i.e. Borlaug_06102020) and inside the folder create another file named RAW files
* Copy and paste the CC-Phenom measurements into the RAW folder

* Download Excel Macro Enabled File and place into field / sensor date folder

* Open file and view macro by navigating in the Excel ribbon -> View -> Macros -> CC-Phenom
* Replace the path name with the path of the RAW folder created (i.e. C:\Users\Computer\Desktop\Borlaug_06102020\RAW\ ) <br/>
**Ensure the path ends with a \ otherwise it will not work**

* Run CCPhenom Processor Step 1 to combine all the CSV log measurements into one Excel Workbook

##### Step 2 - Organize Readings Per Sensor (ACS-430 and DAS43X) and Order Worksheets in Ascending Order


##### Step 3 - Create New Columns for DELTA_TMP and FPAR



## Machine Learning - XGBoost with Hyperparameter Tuning
