# Azure_Data-Factory

ETL TOOLS - AZURE DATA FACTORY (NO-CODE), AZURE DATA BRUCKS (CODE)

• ADF - Is an ETL tools available in AZ 
• Before this we had MSBI tools (SSIS - ETL like ADF, SSRS - Reports like PowerBI , SSAS -Analysis)  
• SSIS is local or on-prem 
• ADF is cloud-based ETL tool
	
	
Components of ADF :

	- Integration Runtimes - 
	
		○ We require computation to Move data for On-prem we have Self hosted Integration Runtime or if cloud we require Auto resolve (default we create ADF) Azure Integration Runtime or SSIS Integration Runtime (To lift and shift of SSIS project from on-prem to cloud)
		○ Integration Runtime provide compute infra to DF to connect diff network and execute the activities
		
	- Linked Services -  

		○ Establishing connections to the data sources for every Integration Runtime by storing connection information
	
	- Data Sets -
	
		○ Preparation of data based on activity 
		
	- Activities - 
	
		○ Copy Data Activity , Delete 
		
	- Pipelines -

		○ Collection of activities and designing of flow
	
	- Triggers - 

		○ Scheduling of pipelines to run daily on specific time
		○ Scheduling Trigger, Event Based Trigger, Tumbling Window Trigger 
