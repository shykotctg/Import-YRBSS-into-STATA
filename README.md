# Import YRBSS ASCII into STATA
This repo contains dictionary and do files for importing and labeling YRBSS ASCII data into Stata.

## Dictionary File (yrbs.dct)

This is Dictionary to read-in fixed format ASCII data into STATA. The dictionary
is made using the column width and variable names. This is coming from the 
sas input file (same as spss input file). Although, q* variables are coded as 
string in sas/spss, I coded them as numeric. 

Put this file to raw_data folder along with all raw ASCII .dat files in the same folder
 
To read-in, change the file name after "using" to the file you want to read-in.

## Read Raw Data (read_raw_data.do)
							
This do file is for read-in raw ASCII data into stata and save it as .dta file. 

We need yrbs.dct dictionary file to read in. This yrbs.dct file is in raw_data 
forlder. Place all the raw ASCII .dat files in raw_data folder alonside yrbs.dct 

At first, we need to change the data file name in yrbs.dct file, and run this 
do file, and export it as STATA .dta file in intermediate_data folder. 
For example, to read-in "sadc_2023_state_a_d.dat", 
first open yrbs.dct and change the first line 
from "infix dictionary using sadc_2023_state_x_x.dat" 
to   "infix dictionary using sadc_2023_state_a_d.dat"

Secondly, change the last line of the code similarly.

The raw data are in "raw_data" folder. Some examples are:
A. State data
	-sadc_2023_state_a_d.dat
	-sadc_2023_state_e_h.dat
	-sadc_2023_state_i_l.dat
	-sadc_2023_state_m.dat
	-sadc_2023_state_n_p.dat
	-sadc_2023_state_q_t.dat
	-sadc_2023_state_u_z.dat

B. National and district data
	-sadc_2023_national.dat
	-sadc_2023_district.dat

## Append and label

This do file append all data you have created (change the names of the data you have created) and
label them as per the YRBSS documentation.


  
