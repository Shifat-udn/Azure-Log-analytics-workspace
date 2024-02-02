# Azure-Log-analytics-workspace
Azure Log analytics workspace -  Web server access monitoring

 - Login Azure portal 
 - Create new log analytics or click on the existing one. 

![image](https://github.com/Shifat-udn/Azure-Log-analytics-workspace/assets/141313925/c88129fc-8e4c-4de1-a675-d05f5acfc332)

- Go to virtual machines > click on the Server (Ubuntu-01)
![image](https://github.com/Shifat-udn/Azure-Log-analytics-workspace/assets/141313925/46db0a60-53d2-423e-bbdd-c8a33e3b0dca)

- Connect with the virtual machines.
- 
![image](https://github.com/Shifat-udn/Azure-Log-analytics-workspace/assets/141313925/b3e64512-faf3-4b32-8600-dcdaafe641e4)

- Select Tables then Create > New custom log (MMA-based)
![image](https://github.com/Shifat-udn/Azure-Log-analytics-workspace/assets/141313925/b2688850-424d-4d88-99f7-59165bf5da1a)
- Upload a sample log file , Define collection path for Apache2 log /var/log/apache2/access.log . then give it a name and create
![image](https://github.com/Shifat-udn/Azure-Log-analytics-workspace/assets/141313925/83cb2cb4-799d-4b2d-8342-546a1a04be8f)

- Now login to the linux VM and check if Apache server logs are generating
  ![image](https://github.com/Shifat-udn/Azure-Log-analytics-workspace/assets/141313925/4e5e7775-8d4c-469a-a9a4-d2a01fda93bc)

- Set the log file read only for others with chmod 644 /var/log/apache2/access.log
 ![image](https://github.com/Shifat-udn/Azure-Log-analytics-workspace/assets/141313925/4fb7aa6e-959f-47f8-ae1d-8afc4a2eb79c)
 - Now Go to Azure Workbooks . Create a new or click on existing one. And open the workbook
![image](https://github.com/Shifat-udn/Azure-Log-analytics-workspace/assets/141313925/f11b809d-f0e9-42e8-9d7e-0746831cb40e)
- On the workbook add > Add query
  ![image](https://github.com/Shifat-udn/Azure-Log-analytics-workspace/assets/141313925/185373bd-33e9-4683-92a3-4b08647ee726)

- Now write the KQL Query according to the log. In this case we want IP address from apache access log
  ![image](https://github.com/Shifat-udn/Azure-Log-analytics-workspace/assets/141313925/a8356fca-7453-4426-9587-d73e8c5524f4)

- Run the Query and save it. The graph will be displayed
  ![image](https://github.com/Shifat-udn/Azure-Log-analytics-workspace/assets/141313925/9fbb2d8b-b31d-4d98-97c7-2489a1954495)



