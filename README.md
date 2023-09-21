# taxi_uber_data_engineering_end-to-end
Basically, end-to-end data engineering project with information from NYC Taxi &amp; Limousine Commission. 

Tools 
GCP Services: Cloud Storage, Compute Engine, BigQuery, Looker, also worked with an open-source tool [Mage] for transformation and integrating data. Mage is a pipeline tool that is almost the same as Airflow but better. Mage is much easier and more interactive. The last but not least is the Lucid Chart to create a data model structure. 

Process Description
01) Analyzed the information from the dataset (documentation, dictionary, arrays)
02) Open Jupyter / Open Python / Export Pandas / upload the file
03)  Convert the flat file into data model structure
04) Identified the fact table and the subsets and the principal keys and foreing keys
05) Create the code in Jupiter to let the flat file in a model structure, in that moment we applied the next formulas: pd.read_csv  / df.head() / df.info  / pd.to_datetime(df[' ']) / drop_duplicates().reset_index(drop=True) / .dt.hour / .dt.day / .dt.month / .dt.year / .dt.weekday / .index / datetime_dim = datetime_dim[[ ' ', ' ', ' ']] #It's just for organizing / .map /  df.merge
06) Create a bucket in Google Store (GCP) and upload the file, also it's key become the file in public (route: permissions/fine-grained) after access and set up like public with that the file has a URL
07) Create a VM instances in Compute Engine (GCP) it's key choose Firewall HTTP and HTTPS
08) Connect with the instance, it just clics on SSH
09) Write the code that is in [Active and install programs in Instance]
10) hs
   

