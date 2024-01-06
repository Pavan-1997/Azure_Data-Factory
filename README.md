# Azure_Data-Factory

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


## Implementation to Check Components:


1. Go to portal.azure.com


2. Search and open Data Factory ->

	Select your Subscription
	
	Select your Resource group
	
	Give name 
	
	Click on Review + Create


3. Click on Launch studio 

	Go to Manage -> Connections -> Integration runtimes -> (By default Auto-Resolve Integration runtime is created which can't be customized)
	
	Click on New -> Azure, Self-Hosted -> Click on Continue -> (Here you can either use Azure or Self-Hosted)
	
	We create Linked services for every Integration Runtime
	
	We create Datasets for every Linked Service by going to Author -> Datasets -> 3 dots -> Select the data type with Linked service associated with it 
	
	We then create pipelines on the same way 
	
	We later schedule them using Add Trigger

![image](https://github.com/Pavan-1997/Azure_Data-Factory/assets/32020205/636bff12-632f-46ee-99cf-75efb0d4969c)
