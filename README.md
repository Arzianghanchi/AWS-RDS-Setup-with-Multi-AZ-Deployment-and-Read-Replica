# AWS-RDS-Setup-with-Multi-AZ-Deployment-and-Read-Replica
 1. Create an RDS Instance with Multi-AZ Deployment

 Step 1: Sign in to the AWS Management Console
- Open the [AWS Management Console](https://aws.amazon.com/console/) and sign in with your credentials.

 Step 2: Navigate to RDS
- In the AWS Management Console, type RDS in the search bar and select RDS under "Services."
 ![image](https://github.com/user-attachments/assets/07fcd37e-16c2-43c0-802d-09948a126af7)

 Step 3: Create a New Database
- Click on Create database.
 ![image](https://github.com/user-attachments/assets/c7d00b20-c030-4d61-8606-1965c611cf54)
- Choose a database creation method. You can select either:
  - Standard Create: Offers more configuration options.
 ![image](https://github.com/user-attachments/assets/9faef690-af8d-4fd5-bc89-d36685e6425e)
  - Easy Create: AWS sets up the RDS instance with default settings (not recommended for production).

 Step 4: Select the Database Engine
- Choose a database engine (e.g., MySQL, PostgreSQL, MariaDB, etc.).
- Select the version of the database engine.   
![image](https://github.com/user-attachments/assets/e57f7b31-dae8-401e-80a8-a7e2ba6b3b28)
![image](https://github.com/user-attachments/assets/8cfb3912-75aa-42fd-9805-d7b52c8c6a27)

 Step 5: Configure Database Settings
- DB Instance Identifier: Provide a name for your DB instance.
- Master Username: Enter a username for the database administrator.
- Master Password: Set a strong password and confirm it.
![image](https://github.com/user-attachments/assets/cc8fc696-9c34-4ac8-842e-47a8ab0f97dd)
 ![image](https://github.com/user-attachments/assets/e16b3343-a663-4aa6-9dc0-5760034dab9c)
 
 Step 6: Choose Instance Specifications
- Under DB instance size, select the appropriate instance class (e.g., db.t3.xLarge).
 ![image](https://github.com/user-attachments/assets/25d8a729-f397-4145-8056-70f694bbb13c)

- Choose Multi-AZ deployment by checking the box. This option creates a standby instance in a different Availability Zone for failover.
 ![image](https://github.com/user-attachments/assets/d0e67ec3-8db5-44b6-885a-32c77aa9c60c)

 Step 7: Storage Configuration
- Set the storage type (e.g., General Purpose (SSD)).
- Choose the Allocated storage (e.g., 20 GiB).
 ![image](https://github.com/user-attachments/assets/3db93117-137f-4ac9-b8ee-df69f79ead8c)

- Enable Storage Auto-scaling if needed.
- Ensure Enable automated backups is checked.
  - Retention period: Choose how long backups should be retained (e.g., 7 days).

 Step 9: Additional Configuration
- Initial Database
 ![image](https://github.com/user-attachments/assets/771695bc-9acd-4026-8461-ba984431d205)

- Monitoring
 ![image](https://github.com/user-attachments/assets/e9de0e7a-f4f5-439c-ab97-16f97ef85d78)

- Enable Encryption if needed.

 Step 10: Launch the RDS Instance
- Review your settings and click Create database.
 ![image](https://github.com/user-attachments/assets/7541a68a-6e62-4d1f-8cc2-276ac99b10ed)

- The RDS instance will take a few minutes to be provisioned with Multi-AZ deployment.

 2. Create a Read Replica

 Step 1: Navigate to the RDS Console
- In the RDS dashboard, locate your primary RDS instance under Databases.
 ![image](https://github.com/user-attachments/assets/59294a48-19a9-41d5-b933-52a3ab1b15d4)

 Step 2: Create a Read Replica
- Click on the Actions dropdown menu next to your primary instance and select Create read replica.
 ![image](https://github.com/user-attachments/assets/b3a5b772-e581-459c-8815-73e0f6ed8a65)

 Step 3: Configure the Read Replica
- DB Instance Identifier: Provide a unique name for the read replica.
- Source DB Instance: Your primary instance should already be selected.
- Multi-AZ Deployment: Choose whether you want Multi-AZ for the read replica.
- Instance specifications: Select the instance class and storage as needed.
 ![image](https://github.com/user-attachments/assets/8c1298c1-900e-477c-8d98-803d4973e091)
![image](https://github.com/user-attachments/assets/6b311582-f289-4424-80df-cf172e16fb0d)
![image](https://github.com/user-attachments/assets/c8690d32-ded7-4022-a733-b27b39ecbbf9)

 Step 5: Launch the Read Replica
- Review your settings and click Create read replica.
- The Read Replica will take a few minutes to be created.
 ![image](https://github.com/user-attachments/assets/899751b1-2b26-484d-b645-d19f9c89f19f)

By following these steps, We have successfully created an RDS instance with Multi-AZ deployment, automated backups, and a Read Replica. This setup ensures high availability, durability, and scalability for our database workloads.
