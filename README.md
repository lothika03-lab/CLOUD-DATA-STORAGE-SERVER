# CLOUD-DATA-STORAGE-SERVER

### NAME: Stephen raj Y
### REG NO: 212223230217

## Aim

To create and configure an Amazon Relational Database Service (Amazon RDS) instance as a cloud data storage server, configure the required security settings, connect it to a web application, and perform database operations using the application.

## Algorithm / Steps

1. Create a Security Group for the RDS database.
2. Add an inbound rule to allow MySQL (Port 3306) access from the Web Security Group.
3. Create a DB Subnet Group using two Availability Zones.
4. Launch an Amazon RDS MySQL database instance.
5. Configure the database with the required identifier, username, password, storage, and instance class.
6. Associate the database with the created Security Group and Subnet Group.
7. Wait until the database status becomes **Available**.
8. Copy the RDS endpoint.
9. Open the web application using the provided Web Server IP address.
10. Enter the RDS endpoint, database name, username, and password.
11. Connect the application to the database.
12. Verify the connection by adding, editing, and deleting records in the Address Book application.


## Program

### Security Group Configuration

* Security Group Name: **DB Security Group**
* Inbound Rule: **MySQL/Aurora (3306)**
* Source: **Web Security Group**

### DB Subnet Group

* Name: **DB-Subnet-Group**
* VPC: **Lab VPC**

### Amazon RDS Configuration

* Engine: **MySQL**
* Template: **Dev/Test**
* Availability: **Multi-AZ**
* DB Instance Identifier: **lab-db**
* Username: **main**
* Password: **lab-password**
* Instance Class: **db.t3.micro**
* Storage: **20 GB (General Purpose SSD)**

### Connect the Application

```text
Endpoint : <RDS Endpoint>
Database : lab
Username : main
Password : lab-password
```

After submitting the above details, perform Add, Edit, and Delete operations on the Address Book application.

### Output:
<img width="1917" height="918" alt="Screenshot 2026-11-16 104736" src="https://github.com/user-attachments/assets/9a2ebb41-514f-4bca-9633-54509703a8e8" />
<img width="1917" height="907" alt="Screenshot 2026-11-18 083006" src="https://github.com/user-attachments/assets/ff481140-2b9f-4616-a1b0-91cc15b2f24b" />
<img width="1535" height="780" alt="Screenshot 2026-11-18 091754" src="https://github.com/user-attachments/assets/b1c49da6-be4e-4aa4-90f6-24b7d4dc5306" />
<img width="1917" height="922" alt="Screenshot 2026-11-18 092200" src="https://github.com/user-attachments/assets/fee525ef-2bb2-495f-a9a3-5dc598043ee4" />

### Result:
Thus, an Amazon RDS database instance was successfully created and configured as a cloud data storage server. The database was securely connected to a web application, and data operations such as inserting, updating, and deleting records were successfully performed through the application.


