# Useful Precision Ag Tools - Crop Circle Phenom
*These are some useful tools and coding tricks I have developed for PA management in corn using the multiparameter Crop Circle Phenom sensor.* 

## Crop Circle Phenom Excel Macro
### About the Sensor
The Holland Scientific Crop Circle Phenom is a multiparameter active sensing instrument capable of measuring red, NIR, and red-edge bands as well as climatic and physiological measurements, including upwelling and downwelling PAR, air / canopy temperature and atmospheric pressure.

The readings are measured approximately once per second for each band and are stored in a CSV file. 

### Use Case for VBA Macro
Since the Crop Circle Phenom instrument combines ACS-430 and DAS43X measurements into one CSV file per log measurement, several pre-processing steps are needed to organize the data. The steps I found useful were: 1.) Combine all the RAW CSV files from each sensing date/ field, 2.) organize the readings by sensor and order by measurement number, and 3.) create new variables such as fPAR and DELTA_TMP.

_Sample Phenom Measurement With Alternating Sensor Readings_
![PhenomLog0](https://user-images.githubusercontent.com/80427122/110829379-abc02d80-825d-11eb-9d12-517efd8796d6.png)


#### Step 1 - Combining RAW CSV Files
* Create a new folder with field and sensor date (i.e. Borlaug_06102020) and inside the folder create another file named RAW files
* Copy and paste the CC-Phenom measurements into the RAW folder

![Folders](https://user-images.githubusercontent.com/80427122/112680869-4d41a480-8e44-11eb-93ae-59ce79da5eb9.png)


* Download the Crop Circle Phenom Template Excel Macro Enabled File and place into the new parent folder (i.e. Borlaug_06102020)

![Folders](https://user-images.githubusercontent.com/80427122/112681218-c3460b80-8e44-11eb-9738-c23bf25bf448.png)

* Open file and view macro by navigating in the Excel ribbon -> View -> Macros -> CC-Phenom

![steps](https://user-images.githubusercontent.com/80427122/112681888-b1b13380-8e45-11eb-8e69-dcd41a488c26.png)

* Replace the path name with the path of the RAW folder created (i.e. C:\Users\Computer\Desktop\Borlaug_06102020\RAW\ ) <br/>

![path](https://user-images.githubusercontent.com/80427122/112682123-06ed4500-8e46-11eb-86c9-69daa1c10239.png)

**Make sure the path ends with a \ otherwise it will not work**

* Run CCPhenom Processor Step 1 to combine all the CSV log measurements into one Excel Workbook

_Now all the Phenom log files are in one Excel file, however, the measurements still need to be separated per sensor and ordered by log number_
![PhenomLog2A](https://user-images.githubusercontent.com/80427122/110880129-bdc4bf00-82a3-11eb-972f-7373ca268e1e.png)

#### Step 2 - Organize Readings Per Sensor (ACS-430 and DAS43X) and Order Worksheets in Ascending Order
* Double check all measurements have been imported and run CCPhenom Processor Step 2 

_All the sensor 1 and sensor 2 readings are now sorted_
![PhenomLog1](https://user-images.githubusercontent.com/80427122/110877761-894f0400-829f-11eb-8951-84569797e611.png)

#### Step 3 - Create New Columns for DELTA_TMP and fPAR as well as a summary sheet
* Adds Delta Temp (Canopy-Air Temp) and fractional PAR columns in place of unused CH1 and CH2 bands
![PhenomLog2](https://user-images.githubusercontent.com/80427122/110880303-0d0aef80-82a4-11eb-98a5-c8457eb23a06.png)


* Creates a summary sheet at beginning where plot measurements can be summarized
* Summary sheet comes in handy for summarizing average band readings per plot

![PhenomLog3](https://user-images.githubusercontent.com/80427122/110880251-f2d11180-82a3-11eb-86b2-a9e0cd58468b.png)

