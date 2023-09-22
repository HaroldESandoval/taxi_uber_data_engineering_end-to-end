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
10) Go to the instance and in a new page put the External IP address plus localhost before you want to get in to this page you have to clic the name of network interfaces (instances) and after go to the firewall, after create a firewll rule and select in target All instances in the network and Source IP 0.0.0.0/0 and in TCP select the port 
11) In that address you have to create a new project, create a data loader (Python / API) because we're gonna put the link where is url ='' then we run the app
12) After we need to transform the data we have to choose Generic (no template) then we need to import pandas in firts line, under the #specify line we have to write all the python code at the final you have to write the formula return what you have to become the tables in dictionaries 
13) Then you have to create a data exporter choise python plus bigquery, then we need to connect the data expoter with BigQuery API, so we have to go the console and search APIs & Services, the we choose the choise credential, then create credentials, like that we're gonna ensure that the date is connect with all GCP services althoght you can choose whatever you want in that case I chose Role BidQuery admnin. then you choose the credential then the key and create the new key with JSON in that downloaded a file with that information  
14) After in Mage you have to go to io_config.yaml and change the Google_Service_ACC_KEY for the credential information when you replace all you have to clic in View pipeline 
15) Then we need to go to BigQuery and create a dataset, then that is created we copy the title and after in Mage data Exporte in the line  
table_id = 'your-project.your_dataset.your_table_name' //replace// table_id = 'my-test-project-399616.uber_data_enginnering_yt.fact_table' (this is important because is the address)
def export_data_to_big_query(df, **kwargs) -> None: //replace// def export_data_to_big_query(data, **kwargs) -> None:
df, //replace// DataFrame(data['fact_table'])
and run de application
16) It's apper a error we need to go to GCP instances clic in SSH while is running one in the other we can put more code to install cloud and bigquery
17) run again mage and then the export the fact_table you have to export the other tables 
18) then you have to use other code to bring the other tables that is in [Uber Export the other files to BigQuery]
