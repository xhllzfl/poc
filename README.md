# Using Python to Stream Real Time Stock Data in Azure Event Hubs & Azure Stream Analytics
STEP 1:
Creat a Event Hubs Namespace

![image](https://user-images.githubusercontent.com/114129103/192590365-d387bc44-b342-495b-89c6-83f2db17f1a6.png)
![image](https://user-images.githubusercontent.com/114129103/192591255-c33ad579-58b6-41c8-95dc-e675a410122a.png)

STEP 2:
Creat Event Hub
![image](https://user-images.githubusercontent.com/114129103/192592083-8bd0dfb9-704a-4095-b6f2-b5a94caac0bd.png)
![image](https://user-images.githubusercontent.com/114129103/192592234-2e0ad0bf-21b3-4107-85e7-f585249c2866.png)
![image](https://user-images.githubusercontent.com/114129103/192592277-8eb77790-cd91-45af-99e7-eff63262b72a.png)

STEP 3:
Creat Shared access policies
![image](https://user-images.githubusercontent.com/114129103/192593007-6df121db-f679-4b5d-b21c-1c3aff3cb6f2.png)
![image](https://user-images.githubusercontent.com/114129103/192593090-979cb4e2-38b1-4e95-be21-ee7ce5d35868.png)
![image](https://user-images.githubusercontent.com/114129103/192593294-3767e244-e6d9-4f65-ac8f-98604ac085f5.png)
![image](https://user-images.githubusercontent.com/114129103/192593407-acb8d29a-059b-43cd-bcbd-73de38d4a942.png)

STEP 4:
Creat Stream Analytics jobs
![image](https://user-images.githubusercontent.com/114129103/192593619-463817ab-7d64-4583-8d95-5bf588931c14.png)
![image](https://user-images.githubusercontent.com/114129103/192593830-0c9c916d-42f2-4d2d-b3eb-f4d88e872892.png)

STEP 5:
Add streaming inputs
![image](https://user-images.githubusercontent.com/114129103/192594523-8572b4e0-43e4-4620-aee6-8e3feb24e178.png)
![image](https://user-images.githubusercontent.com/114129103/192594889-90dabbc8-30c7-4f69-9a21-23af8550845d.png)

STEP 6:
Creat Python file to get realtime stock data and do the data manipulation
See: AzureStreamAnalyticsJob-StockFeed.ipynb

STEP 7:
Link the python with Azure: Send events to or receive events from event hubs by using Python (azure-eventhub)
https://learn.microsoft.com/en-us/azure/event-hubs/event-hubs-python-get-started-sendimport asyncio
![image](https://user-images.githubusercontent.com/114129103/192595948-aacab7e7-d9e5-4c0a-bd67-0cc79097ce70.png)
Change the conn_str="EVENT HUBS NAMESPACE - CONNECTION STRING", eventhub_name="EVENT HUB NAME"
to: connection_str = 'Endpoint=sb://stockfeeddatademoxhll.servicebus.windows.net/;SharedAccessKeyName=RootUserAccessPolicy;SharedAccessKey=HqI4+Cq0l6h4RLQ/iINmgQZ6+SWK0/W/q1aRqI+tq60=;EntityPath=pythonfeeddata'
eventhub_name = 'pythonfeeddata'

STEP 8:
Go to Query and test the Stream Analytics Job
![image](https://user-images.githubusercontent.com/114129103/192596887-e3cb21bd-d3fb-4e03-8827-2c055f7dff14.png)

Step 9:
Creat Output
![image](https://user-images.githubusercontent.com/114129103/192597580-f7c2a8b1-0c88-48e2-ac23-0ca3061722b9.png)
Save the table to your container
![image](https://user-images.githubusercontent.com/114129103/192598078-95717371-8a43-4cfb-b5dc-75dec66f2b98.png)

Finally you can get the .json file you need.

