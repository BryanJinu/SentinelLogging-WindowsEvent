
# SentinelLogging-WindowsEvent
Logging Windows Event into Microsoft Sentinel from a Virtual Machine locally hosted and domain joined in a personal Azure Tenant. 

Resources: 
1. Azure tenant 
2. Windows 11 VM (Locally hosted, non-azure VM)
3. Azure Arc
4. Microsoft Sentinel
5. Data Collection Rule
6. Data Collection Endpoint

# High-Level Architecture Diagram 
<img width="829" height="221" alt="PersonalProject1 drawio" src="https://github.com/user-attachments/assets/0e8dc2c1-a483-498d-876c-5a8c5b936657" />

# Detailed Steps
The Windows 11 VM is hosted locally on my personal computer. 
In order to ingest Windows Event logs into Sentinel, we'll have to install Azure Arc. 
Azure Arc lets you manage Windows and Linux physical servers and virtual machines hosted outside of Azure on your corporate network or other cloud provider.

<img width="1908" height="315" alt="Azure ARC" src="https://github.com/user-attachments/assets/481e4dbe-0968-48d1-a1f4-77c45c12bc0a" />

We have now succesfully added our Windows 11 VM into our Azure space. 
Now we'll need to create a Data Collection Rule in order to ingest the logs. 

<img width="1912" height="379" alt="DCR" src="https://github.com/user-attachments/assets/c202cc23-cdbc-4368-99ae-31333dbfded2" />

Data Collection Rules (DCRs) determine how to collect and process telemetry sent to Azure.

Here we've established what type of data we will ingest from the "Data Source" pane and where it will be sent to. 
<img width="1894" height="570" alt="Data_Source_DCR" src="https://github.com/user-attachments/assets/15bfe5dc-4163-4732-ac39-2e162dcbb10b" />
<img width="1896" height="299" alt="DCR_Destination" src="https://github.com/user-attachments/assets/0d501288-bb6d-4c3f-b7fc-61ce6d43e948" />

# Final
From here, if everything is setup properly, you will see logs in Sentinel
<img width="1603" height="840" alt="Microsoft_Sentinel_Logs" src="https://github.com/user-attachments/assets/0ffbeb87-f6f0-41be-989f-b2bc2d81c676" />




