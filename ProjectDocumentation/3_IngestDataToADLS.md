## Ingest Data from Multiple Sources

### ADF Configuration

1. Linked Services
1.1 Key Vault
![image](https://github.com/Subramanian-Thiagarajan/Azure_Flight_Analysis_Project/assets/96657323/0887dbd8-aefd-41d7-8292-d519603b2165)

1.2 ADLS Gen 2

- Create Client Secret with SPN ID and SPN Secret
![image](https://github.com/Subramanian-Thiagarajan/Azure_Flight_Analysis_Project/assets/96657323/d3aabc83-d838-4916-bad7-00cdb5888a81)

- Create Access Policy with List and Get permission for the SPN in Key Vault connection with ADF
![image](https://github.com/Subramanian-Thiagarajan/Azure_Flight_Analysis_Project/assets/96657323/6cc6015f-a55d-47cb-a960-2a5e5d08a6e3)

- Create IAM Role access for the SPN in ADLS Gen 2
![image](https://github.com/Subramanian-Thiagarajan/Azure_Flight_Analysis_Project/assets/96657323/f1d55cc1-bf81-4d1b-a5ce-62bee52a6ebe)

- In ADF, add the Linked Service
![image](https://github.com/Subramanian-Thiagarajan/Azure_Flight_Analysis_Project/assets/96657323/7a0d7444-4a04-46c5-ab20-1de9b6cd3225)

![image](https://github.com/Subramanian-Thiagarajan/Azure_Flight_Analysis_Project/assets/96657323/24ca51ec-b1ae-4f59-8c15-a178be485744)

2. Create DataSets
2.1 ADLS Gen 2 Source and Sink
   ![image](https://github.com/Subramanian-Thiagarajan/Azure_Flight_Analysis_Project/assets/96657323/a659ee61-2e4d-44d1-b38d-0b1ea46d5305)

2.2 Create JSON DataSet for file containing metadata of file details
  ![image](https://github.com/Subramanian-Thiagarajan/Azure_Flight_Analysis_Project/assets/96657323/bbd63df7-a5f2-427c-bd3f-9c7a61a7989f)

2.3 Zip File Dataset
   ![image](https://github.com/Subramanian-Thiagarajan/Azure_Flight_Analysis_Project/assets/96657323/38cf1b65-22fd-4d46-bee3-13170ee564de)


3. Create Pipeline to iterate metadata json and copy files from source to sink
   ![image](https://github.com/Subramanian-Thiagarajan/Azure_Flight_Analysis_Project/assets/96657323/2887996f-520b-42c8-bb66-e8d69eefe649)
   ![image](https://github.com/Subramanian-Thiagarajan/Azure_Flight_Analysis_Project/assets/96657323/47e606e2-6524-4065-a457-eb1ab19c2543)
   ![image](https://github.com/Subramanian-Thiagarajan/Azure_Flight_Analysis_Project/assets/96657323/622adb64-8437-4c67-8db5-ad6b23636754)


Debugging Results
![image](https://github.com/Subramanian-Thiagarajan/Azure_Flight_Analysis_Project/assets/96657323/1cede207-8078-4e0a-88e2-74d4a9a6241b)


