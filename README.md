# stream2-planning
Jupyter Notebooks that estimate the data volumes in Stream 2 and also analyse 
the data that has been accessed during the project.

### vars_retrieved_20200626.ipynb

This notebook calculates the number of variables that have been requested for 
retrieval from tape to disk at JASMIN by the PRIMAVERA project using data from 
the DMT. The number is the number of times that this variable has been 
requested. A value of 1 means that this variable has been requested once from 
a single model for a single experiment. 7 could mean that this variable had 
been requested from all models for a single experiment, or that the same 
variable from one model and experiment has been requested by seven different 
people. The name is in the form "var-name_table-name" and the table name 
includes the frequency of that variable. The variable's standard name is 
included in the third column.

### vars_retrieved.ipynb

The same as `vars_retrieved_20200626.ipynb` but run in November 2018 while 
developing the data request for the Stream 2 simulations.

### esgf_vars_downloaded.ipynb

This notebook looks at the number of downloads of CMIP6.HighResMIP variables 
that have been downloaded from CEDA's ESGF node via HTTP between 25th March 
2019 and 14th May 2020. The variables have been sorted by frequency and table
name. The number shows the number of times that unique datasets (e.g. a unique 
combination of institute, model, experiment, variant label, table and variable)
have been downloaded from a unique IP address. 

PRIMAVERA was given access to access logs of the THREDDS Tomcat server from 
CEDA's ESGF node. All of the PRIMAVERA data has been published to this ESGF 
server. Data can be downloaded over the HTTP protocol from THREDDS or via 
Globus and so these logs do not show all of the data that has been downloaded, 
although some of the Globus downloads will have been replication of the data 
to other ESGF nodes and so may not be representative of actual usage of the 
data. The data may have been replicated to other ESGF nodes and so these logs 
only show downloads from CEDA's ESGF node and not the total global downloads. 

The logs had been anonymised by replacing the IP address in them with a hash of
the IP address. Some institutes will operate a web proxy so that all users at 
that institute will appear to come from the same IP address. Because some 
datasets from some institutes have a single variable spread over several files,
a download has been counted as a download of that variable from that IP address
hash. 

### d9_6.ipynb

Identify the Stream 1 and 2 data in the DMT and calculate the proportion of 
data that had been retrieved in terms of the number of datasets and the storage 
space.

### stream1_volumes.ipynb

Look at the actual and planned volumes of Stream 1 highresSST-present data.

### file_density.ipynb

Look at the desnity of data in files to see how many bytes are required to store 
each data point.

### stream1_high_freq.ipynb

Estimate the volume required to store the Stream 2 proposed simulations for 
different models.

### Sommar_data_volumes.ipynb

Looking at the data request and storage required for a MOHC Stream 2 simulation
and extrapolating these values for a 10 km model run over a longer period of
time.
