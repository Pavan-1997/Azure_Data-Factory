# Azure_Data-Factory_Basic

ETL TOOLS - AZURE DATA FACTORY (NO-CODE), AZURE DATA BRUCKS (CODE)

• ADF - Is an ETL tools available in AZ 

• Before this we had MSBI tools (SSIS - ETL like ADF, SSRS - Reports like PowerBI, SSAS -Analysis)  

• SSIS is local or on-prem 

• ADF is cloud-based ETL tool
	
	
## Components of ADF :


- ### Integration Runtimes - 
	
	- We require computation to Move data for On-prem we have Self-hosted Integration Runtime or if cloud we require Auto resolve (default we create ADF) Azure Integration Runtime or SSIS Integration Runtime (To lift and shift of SSIS project from on-prem to cloud)
	- Integration Runtime provides compute infra to DF to connect diff network and execute the activities
		
- ### Linked Services -  

  	- Establishing connections to the data sources for every Integration Runtime by storing connection information
	
- ### Data Sets -

	- Preparation of data based on activity 
		
- ### Activities - 
	
	- Copy Data Activity, Delete 
		
- ### Pipelines -

	- Collection of activities and designing of flow
	
- ### Triggers - 

	- Scheduling of pipelines to run daily at specific time
	
 	- There are 3 types - Scheduling Trigger, Event-Based Trigger, Tumbling Window Trigger 


## Implementation of Copy Acitivity:


1. Go to portal.azure.com


2. Search and open Data Factory ->

	Select your Subscription
	
	Select your Resource group
	
	Give name
	
	Click on Review + Create
	
	Click on Launch studio


3. Search and open Storage accounts -> Click on Create

	Select your Subscription
	
	Select your Resource group
	
	Give Storage account name
	
	Click on Review + Create
	
	Click on Containers -> Click on + Conatiner -> Name - source -> Click on Create -> Upload the Folder along with file
	
	Click on Containers -> Click on + Conatiner -> Name - sink -> Click on Create -> Upload the Folder  


4. Now go back to the ADF Studio 

	Click on Author -> Pipelines -> 3 dots -> New pipeline -> Activity - Copy data
	
	Source -> Ciick on + New -> Select Azure Blob Storage -> Format - Binary -. Click on Continue -> Give it a name -> Click + New Linked service -> 
	
	Give it name
	
	Select your subscription account
	
	Now select your Storage account created earlier
	
	Click on Test connection 
	
	Click on Create
	
	Browse the test.txt file and click on OK


5. Similarly do it for Sink folder by using the same Linked service  but different dataset name


6. Now click on Publish all -> 	Click on Publish


7. Now click on Add trigger - Click on Trigger now 


8. Now the file is copied to the sink container from the source container 
