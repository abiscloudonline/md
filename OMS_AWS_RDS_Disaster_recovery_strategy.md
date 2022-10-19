## Amazon RDS:
Collection of managed services that makes it simple to set up, operate, and scale databases in the cloud.
## What is Multi-AZ:
 * In Multi-AZ deployment, Amazon RDS automatically creates a primary database (DB) instance and synchronously replicates the data to an
instance in a different availability zone.
 * When it detects a failure, Amazon RDS automatically fails over to a standby instance without manual intervention.
## Read Replica:
 The read replica operates as a DB instance that allows only read-only connections;
  Applications can connect to a read replica just as they would to any DB instance.
  Amazon RDS replicates all databases in the source DB instance.
## Disaster Recovery:
## Advantages of DR in cloud over traditional environments:
Recover quickly from a disaster with reduced complexity
Simple and repeatable testing allow you to test more easily and more frequently
Lower management overhead decreases operational burden
Opportunities to automate decrease chances of error and improve recovery time
## Disaster recovery of RDS
Amazon RDS creates and saves automated backups of your DB instance during the backup window of your DB instance. 
Creates a storage volume snapshot of your DB instance, backing up the entire DB instance and not just individual databases
![image](https://user-images.githubusercontent.com/107330427/196693686-55e7f49a-684d-4cf1-a522-b018084efa2d.png)
