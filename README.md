# Useful Precision Ag Tools
*These are some useful tools and coding tricks I have developed for PA management in corn.* 

Created by Cadan Cummings

## Crop Circle Phenom Excel Macro
#### About the Sensor
The Holland Scientific Crop Circle Phenom is a multiparameter active sensing instrument capable of measuring red, NIR, and red-edge bands as well as climatic and physiological measurements, including upwelling and downwelling PAR, air / canopy temperature and atmospheric pressure.

The readings are measured approximately once per second for each band and are stored in a CSV file. 

#### Use Case for VBA Macro
Since the Crop Circle Phenom instrument combines ACS-430 and DAS43X measurements into one CSV file per log measurement, several pre-processing steps are needed to organize the data. The steps I found useful were: 1.) Combine all the RAW CSV files from each sensing date/ field, 2.) organize the readings by sensor and order by measurement number, and 3.) create new variables such as fPAR and DELTA_TMP.

_Sample Phenom Measurement With Alternating Sensor Readings_
![PhenomLog0](https://user-images.githubusercontent.com/80427122/110829379-abc02d80-825d-11eb-9d12-517efd8796d6.png)


##### Step 1 - Combining RAW CSV Files
* Create a new folder with field and sensor date (i.e. Borlaug_06102020) and inside the folder create another file named RAW files
* Copy and paste the CC-Phenom measurements into the RAW folder

* Download Excel Macro Enabled File and place into the new parent folder (i.e. Borlaug_06102020)

* Open file and view macro by navigating in the Excel ribbon -> View -> Macros -> CC-Phenom
* Replace the path name with the path of the RAW folder created (i.e. C:\Users\Computer\Desktop\Borlaug_06102020\RAW\ ) <br/>
**Ensure the path ends with a \ otherwise it will not work**

* Run CCPhenom Processor Step 1 to combine all the CSV log measurements into one Excel Workbook

_Now all the Phenom log files are in one Excel file, however, the measurements still need to be separated per sensor and ordered by log number_
![PhenomLog1](https://user-images.githubusercontent.com/80427122/110877761-894f0400-829f-11eb-8951-84569797e611.png)

##### Step 2 - Organize Readings Per Sensor (ACS-430 and DAS43X) and Order Worksheets in Ascending Order
* Double check all measurements have been imported and run CCPhenom Processor Step 2 

##### Step 3 - Create New Columns for DELTA_TMP and fPAR as well as a summary sheet
* Adds Delta Temp (Canopy-Air Temp) and fractional PAR columns in place of unused CH1 and CH2 bands
* Creates a summary sheet at beginning where plot measurements can be summarized

* Summary sheet comes in handy for summarizing average band readings per plot
![PhenomLog3](https://user-images.githubusercontent.com/80427122/110879529-c5d02f00-82a2-11eb-9b23-4af7d48744be.png)

## Machine Learning - XGBoost with Hyperparameter Tuning
